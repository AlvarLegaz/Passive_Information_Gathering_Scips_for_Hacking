# Linux_Scips_for_Hacking
Scrip básico para recolección de información pasiva para análisis de vulnerabilidades.

### Hay que distinguir entre dos formas de obtener información.
1. **Pasiva:** es el proceso de obtención de información subceptible a ser usada en ataques valiendose de información sobre pesonas, organizaciones o dispositivos que se encuentran indexadas en buscadores. Este método de detección no implica la interactuación del hacker con el objetivo. *Por ejemplo, podemos encontrar emails de miembros de una compañía y usar ese mail como vector de ataque, para phising, etc.*
2. Activa

## Búsqueda de información pasiva.
### Google:
```
* comodin para incluir cualquier valor en busqueda.	
 -"Liga de * femenino"
site:dominio > busca solo en las páginas perteneciende a un determinado dominio
  site:google.es
filetype:txt > busca solo en archivos con una determinada extensión
and operador logico y
or operador lógico o
  site:google.es and filetype:txt

```
### Shodan
https://www.shodan.io/
Shodan es un motor de búsqueda que le permite encontrar diferentes equipos (host) conectados a Internet a través de una variedad de filtros. El funciononamiento básico es que Shodan hace peticiones a todas las ips conectadas a internet para detectar los puertos y servicios que están ejecutando e indexan en su buscador. 

Las busquedas se realiza mediante comandos específicos, conocidos como filtros o queries, introducidos al buscador. A continuación se detallan algunos de ellos, los cuales han sidos extraidos de https://hackingparanovatos.wordpress.com/2017/08/23/buscar-en-shodan-filtros/

Para más filtros https://github.com/jakejarvis/awesome-shodan-queries
```
country: Para buscar en un país en específico. country:py
city: Filtro por ciudad. city:»Los Angeles»
port: Para buscar dispositivos que tengan un puerto abierto. port:3306
net: Búsqueda de una ip específica o rangos de ip. ip:182.93.44.0/24
"Server: yawcam" 
hostname: Busca el texto que le indiquemos en el nombre del host. hostname:iplocal
geo: Buscar dispositivos mediante coordenadas. geo:32.9775,-70.1293
os: Para listar un sistema operativo determinado. os:Linux
after: Dispositivos agregados después de la fecha.
before: Lo mismo, pero antes de la fecha. after/before:27/03/2015
has_screenshot: Nos muestra dispositivos de los cuales hay una captura. has_screenshot:true
```
### Censys
https://search.censys.io/
Se trata de otro motor de búsqueda de dispositivos conectados a internet, al estilo de Shodan. La diferencia es como se indexa la info. Lo que hace es escanear todos los dias internet con zmap y zgrab. Esto permite realizar una indexación diferente a shodam. Esto permite acceder a info más actualizada.

También funciona con comandos y disponemos en el apartado deocumentacion de muchos ejemplos: https://search.censys.io/search/examples?resource=hosts 

```
ip: 0.0.0.0/0 Hosts with an IP address in the IPv4 range.
services.port: {21, 22, 23, 24, 25} Hosts with any of the following port numbers open: 21, 22, 23, 24, 25
labels: {remote-access, file-sharing} and location.continent:Europe  Hosts with a service that enables remote access or file sharing in Europe
services.http.response.html_title: dashboard Hosts with a page title on an HTTP service containing the word "dashboard"
("Index of") and services.service_name:SSH Hosts with the phrase "Index of" anywhere that also have an SSH service exposed

```

### DNSdumpster
https://dnsdumpster.com/

Herramienta totalmente gratuita diseñada para facilitarnos el análisis de cualquier dominio y poder obtener en segundos todo tipo de información relacionada con este. Esta herramienta no utiliza la fuerza bruta como pueden usar otras similares, sino que recurre a la Open Source Intelligence para encontrar más rápidamente toda la información relacionada con el dominio que nos interese analizar.

Esta herramienta va mucho más allá de una simple consulta DNS lookup. Con DNSdumpster podemos descubrir todos los subdominios relacionados con un dominio concreto, además de todos los hosts web. Los datos se obtienen a través de consultas en plataformas como Alexa Top 1 Million, motores de búsqueda (Google, Bing, etc), Common Crawl, Certificate Transparency, Max Mind, Team Cymru, Shodan y scans.io.
[![Imagen de la busqueda](https://www.redeszone.net/app/uploads-redeszone.net/2019/01/analisis-DNSdumpster-Google-655x330.png)

### Have I Been Pwned?
[haveibeenpwned.com](https://haveibeenpwned.com/)
Have I Been Pwned? es un sitio web que permite a los usuarios de Internet comprobar si sus datos personales se han visto comprometidos por violaciones de datos.

El servicio recopila y analiza cientos de ficheros de bases de datos que contienen información sobre miles de millones de cuentas filtradas, y permite a los usuarios buscar su propia información introduciendo su nombre de usuario o dirección de correo electrónico. Los usuarios también pueden inscribirse para que se les notifique si su dirección de correo electrónico aparece en futuros volcados. 
