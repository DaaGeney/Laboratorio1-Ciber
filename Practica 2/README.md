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
Al ejecutar el comando anterior se presentaon un sin número de errores que nos obligaron a realizar modificaciones a este; aún así, el comando anterior no nos dió resultado satisfactorio. 
#### Imagenes de evidencia: 

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


