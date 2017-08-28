### Taller 1

**Nombre:** Julián David González Jiménez  
**Código:** A00315288

## Descripción
El primer taller del curso sistemas operativos trata sobre el sistema operativo Linux, la estructura de sus directorios y virtualización 

## Soluciones

1. La función de los directorios de raíz es agrupar los archivos de forma estructurada. El directorio principal es llamado “raíz” y se representa con “/”. A partir de la raíz se encuentras los siguientes directorios: 

![][1] 

  A demás, estos directorios contienen a su vez archivos, estos son algunos ejemplos:
*	/bin/gzip Reduce el tamaño de los archivos utilizando la codificación Lempel-Ziv (LZ77).
*	/boot/grub Gestor de arranque, es lo primero que se carga cuando inicia el PC.
*	/dev/hda Disco primario
*	 /etc/x11 Archivos de configuración de X Window
*	 /home/userx Contiene diferentes carpetas para la clasificación.
*	/lib Bibliotecas esenciales que son necesarios para que se puedan ejecutar correctamente todos los binarios que se encuentran en los directorios /bin y /sbin.
*	/media/userx Punto de montaje de todos los volúmenes lógicos que se montan temporalmente, ya sean unidades externas USB, otras particiones de disco, entre otras. 
*	/mnt/ Directorio vacío, no se suele utilizar, similar a /media. 
*	/opt/ Se utiliza para instalar software opcional.
*	/sbin/ Comandos para iniciar, reparar y recuperar el sistema. 
*	/srv/www Almacena archivos dentro de un servidor web.
*	/tmp/Donde se almacenan los archivos temporales de todo tipo.
*	/usr/doc Documentación general del sistema.
*	/var/lib Información variable de configuración.

2. 

| Comando   | Usuario | Descripción   |
|------|------|------|
|mount | column –t |Cualquiera|Muestra los sistemas de ficheros montados de una forma ordenada|
|[space] command|Cualquiera|Ejecuta un comando sin guardarlo en el historial|
|ffmpeg –f x11grab –s wxga –r 25 –I :0.0 –sameq /tmp/out.mpg|Cualquiera|Captura el video de un escritorio Linux|
|mtr google.com|Cualquiera|mtr combina la funcionalidad de traceroute y ping|
|du -h --max-depth=1|Cualquiera|Lista el tamaño de todos los subdirectorios desde la posición actual|
|man ascii|Cualquiera|Acceso rápido a la tabla ascii|
|ps –aux | sort –nk + 4 | tail|root|Muestra el top 10 de procesos ordenados por uso de memoria|
|ping –i 60 –a IPAddr|root|Configura una alarma sonora cuando la dirección IP se pone en línea|
|lsof –i|root|Ver la actividad del servicio de red en tiempo real|
|cat /etc/issue|root|Muestra la distribución Linux instalada|

3. printenv: Su función es imprimir todo o parte del entorno, si se le especifica la variable imprime sus valores, si no imprime nombres y pares de valores para todos. 

![][2] 

Creación de una variable de ambiente
Se utilizará el comando export y seguido de este se coloca el nombre de la variable:

![][3] 

Verificación de que si se creó la variable: 

![][4] 

Hacer permanente una variable
Ir al archivo /etc/environment, este será el sitio donde se ubicarán las variables permanentes. 

![][5] 

Se podrá ver que este archivo existe y ocupa 0 bytes, pero al existir, el sistema lo procesará al inicio, por ende, si se edita y se colocan ahí las variables, serán procesadas. 

![][6] 

Se coloca la variable:

![][7] 

Se reinicia el sistema y se verifica que la variable sigue: 

![][8] 
![][9] 

## Referencias

* https://github.com/ICESI/so-commands/tree/master/centos7
* https://cmdchallenge.com  
* https://www.gutenberg.org
*	http://docencia.udea.edu.co/cci/linux/dia4/directorio.htm
*	https://help.ubuntu.com/kubuntu/desktopguide/es/directories-file-systems.html
*	https://computernewage.com/2015/06/14/el-arbol-de-directorios-de-linux-al-detalle-que-contiene-cada-carpeta/
*	https://blog.desdelinux.net/estructura-de-directorios-en-linux/
*	http://www.sysadmit.com/2016/04/linux-variables-de-entorno-permanentes.html

[1]: Imagen1.png
[2]: Imagen2.png
[3]: Imagen3.png
[4]: Imagen4.png
[5]: Imagen5.png
[6]: Imagen6.png
[7]: Imagen7.png
[8]: Imagen8.png
[9]: Imagen9.png
