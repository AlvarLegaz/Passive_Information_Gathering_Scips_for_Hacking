# Linux_Scips_for_Hacking
Repositorio con scrips básicos para *hacking ético*.


## Qué es el hacking ético.

El hacking ético es un término utilizado para englobar el conjunto de actividades que realizan los hackers éticos para mejorar la seguridad de los sistemas informáticos de las empresas que les contratan, con el fin de evitar un posible ataque cibernético que conlleve, entre otros peligros, el robo de información.[referencia](https://www.obicex.es/blog/aprende-con-obicex/que-significa-ser-un-hacker-etico#:~:text=El%20hacking%20%C3%A9tico%20es%20un,peligros%2C%20el%20robo%20de%20informaci%C3%B3n)


Hay que distinguir entre tres formas de obtener información.
1. **Pasiva:** es el proceso de obtención de información subceptible a ser usada en ataques valiendose de información sobre pesonas, organizaciones o dispositivos que se encuentran indexadas en buscadores. Este método de detección no implica la interactuación del hacker con el objetivo. *Por ejemplo, podemos encontrar email de los miembros de una compañía y usar ese mail como vector de ataque, para phising, etc.*
2. Semi-activa
3. Activa

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
Shodan es un motor de búsqueda que le permite encontrar diferentes equipos (host) conectados a Internet a través de una variedad de filtros. El funciononamiento básico es que Shodan hace peticiones a todas las ips conectadas a internet para detectar los puertos y servicios que están ejecutando e indexan en su buscador. 

Las busquedas se realiza mediante comandos específicos introducidos al buscador. A continuación se detallan algunos de ellos, los cuales han sidos extraidos de https://hackingparanovatos.wordpress.com/2017/08/23/buscar-en-shodan-filtros/
```
country: Para buscar en un país en específico. country:py
city: Filtro por ciudad. city:»Los Angeles»
port: Para buscar dispositivos que tengan un puerto abierto. port:3306
net: Búsqueda de una ip específica o rangos de ip. ip:182.93.44.0/24
hostname: Busca el texto que le indiquemos en el nombre del host. hostname:iplocal
geo: Buscar dispositivos mediante coordenadas. geo:32.9775,-70.1293
os: Para listar un sistema operativo determinado. os:Linux
after: Dispositivos agregados después de la fecha.
before: Lo mismo, pero antes de la fecha. after/before:27/03/2015
has_screenshot: Nos muestra dispositivos de los cuales hay una captura. has_screenshot:true

```
