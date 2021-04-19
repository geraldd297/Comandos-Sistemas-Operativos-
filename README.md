# Comandos-Sistemas-Operativos 🚀
Esta es la lista de comandos de Linux vistos en el curso Sistemas Operativos ULACIT.


Se mencionarán todos los comandos vistos en este curso los cuales fueron de gran importancia y aprendí mucho de ellos en el transcurso del curso.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Estos comandos se utilizaron para gran cantidad de funcionalidades dentro del Sistema Operativo Linux.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

COMANDOS🔧:
🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️🖥️
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



top: Este comando muestra un resumen del estado del sistema y la lista de procesos que se están ejecutando en el mismo. 
Y como ejemplo este comando nos muestra en tiempo real todos los procesos ejecutados en la máquina y su consumo.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
htop: Este un visor de procesos para Linux, similar al comando top, pero más visual para el usuario. 
Por ejemplo, da la posibilidad de moverse horizontal  y verticalmente, permite una gran multitud de opciones pero de forma más gráfica.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


-e visualiza información sobre "todos" los procesos del sistema.

-j visualiza información sobre el PGID y SID.

 l visualiza "mucha" información sobre los procesos.

-f visualiza los parámetros con los que se levantó el proceso.

-a muestra también los procesos de otros usuarios.

-N niega el efecto de cualquier opción que se haya especificado.

-x enseña procesos que no están controlados por ninguna terminal.

-u pepe visualiza información de los procesos del usuario pepe.

Ejemplos:
ps -u root -N visualiza todos los procesos que no sean del usuario root.

ps -aux visualiza información detallada de todos los procesos.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
kill: Este es un comando que envía una señal de terminación. Su traducción directa es «matar» y prácticamente es lo que hace con los programas sobre los que lo ejecutamos.
Algunos de los parámetros que tiene el comando kill son:

kill -9 -1: Mata todos los procesos posibles y cierra todo.

kill -l Muestra una lista de todas las señales.

Kill 0  Para todos los procesos excepto su shell de inicio de sesión.

kill -1 Colgar, se genera cuando nos desconectamos del terminal.

kill -2 Interrupción, se genera cuando se pulsa Ctrl+C

kill %1 mata el trabajo número 1 

kill -9 $$ sale del shell actual sin guardar el historial de comandos.

kill -3 Salir.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
history: Muestra el historial de todos los comandos utilizados en la terminal. 
Algunos de sus parámetros son:

History | grep Update: Busca todos los comandos que hayan usado el término “update”.

Es posible que solo deseemos ver una cantidad determinada de comandos ejecutados, por ejemplo, los últimos 7, para ello ingresaremos lo siguiente: history 7
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Pstree: Este comando ver el árbol de procesos activos, en nuestros sistemas GNU Linux.

Con el parámetro “-a” , muestra la línea de comandos utilizada. Por ejemplo, si el comando usa la ruta a un fichero de configuración.

Utilizando el parámetro “-g”, muestra los procesos agrupados por grupo.

Los datos de salida del programa están ordenados de manera alfabética. En cambio, se puede indicar que la salida sea basada en los números de PID, utilizando el parámetro “-n”

Por defecto se inhabilita la visualización en el árbol de los nombres repetidos. Para evitar esto, podemos utilizar el parámetro “-c”

Ejemplo de un pstree: 
systemd─┬─2*[agetty]
        ├─avahi-daemon───avahi-daemon
        ├─cron
        ├─dbus-daemon
        ├─dhcpcd
        ├─fail2ban-server───2*[{fail2ban-server}]
        ├─master─┬─pickup
        │        ├─qmgr
        │        └─tlsmgr
        ├─monit───{monit}
        ├─ntpd
        ├─rsyslogd─┬─{in:imklog}
        │          ├─{in:imuxsock}
        │          └─{rs:main Q:Reg}
        ├─snmpd
        ├─sshd───sshd───bash───pstree
        ├─systemd-journal
        ├─systemd-logind
        ├─systemd-udevd
        └─thd
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Neofetch: Reunirá información el escritorio o servidor. La información que muestre la herramienta dependerá de la distribución que esté ejecutando.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Sudo/ sudo su : para permitir que el usuario creado durante la instalación pueda ejecutar todos los comandos de administración.
Ejemplo: gerald@stretch:~$sudo su - gerald
password for gerald:
gerald@stretch: ~$
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
uname es un programa de Unix y sistemas operativos de tipo Unix que imprime el nombre, versión y otros detalles de la máquina y el sistema operativo que se está ejecutando en ella.

Algunos de sus parámetros son:

uname -s	Enseña el tipo de nucleo, por ejemplo Linux
uname -p	Enseña el tipo del procesador, en caso de no conocerse mostrará “unknown”
uname -m	Enseña la arquitectura del procesador: x86 para 32 bits y x86_64 para 64 bits
uname -n	Enseña el nombre que le hemos dado al equipo para la red, si no lo cambiamos será el que le dimos en la instalación de nuestra distribución. Este nombre se toma de /etc/hostname por lo que se puede cambiar en este archivo
uname -o	Devuelve el Sistema Operativo que estamos usando, suele detectar como GNU/Linux en las distribuciones comprobadas
uname -r	Enseña la información del kernel que tenemos en uso en este mismo momento, si reiniciamos y usamos otro kernel cambiará al ejecutar este comando
uname -v	Se usa para saber la fecha en la que se publicó el kernel que tenemos en uso a este instante
uname -i	Enseña la plataforma para el hardware, siempre vi que devolviera “unknown”
uname -a	Este es el más completo de todos los parámetros ya que -a hace referencia a all mostrando toda la información de los anteriores menos -i y -p si son desconocidos.

Ejemplo: 

uname -a

Salida:

Linux ns899.servidoresadmin.com 3.14.32-xxxx-grs-ipv6-64 #9 SMP Thu Oct 20 14:53:52 CEST 2016 x86_64 GNU/Linux
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ls: Por defecto, el comando ls en solitario, listará los archivos y directorios de la ruta (path) en la que se encuentre el usuario.

Ejemplo: 0001.pcap Escritorio Descargas index.html install.log.syslog Fotos Plantillas
Documentos anaconda-ks.cfg fbcmd_update.php install.log Music Videos Públicos
ls tiene diversos tipos de parámetros:
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ls -a

Este comando enseña los archivos y directorios dentro del directorio actual, incluye los archivos y directorios ocultos.

Ejemplo: . .bashrc Documentos .gconfd Install.log .nautilus .pulse en cookies
.. .cache Descargas .gnome2 install.log.syslog .netstat.swp .recently-used.xbel
0001.pcap .config .elinks .gnome2_private .kde .opera .spice-vdagent
anaconda-ks.cfg .cshrc .esd_auth .gtk-marcadores .libreoffice Fotos .tcshrc
.bash_history .dbus .fbcmd .gvfs .local .pki Plantillas
.bash_logout escritorio fbcmd_update.php .ICEauthority .mozilla Videos Públicos
.bash_profile .digrc .gconf index.html Música .pulse .wireshark
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ls -t

 Este comando ordena los archivos por fecha de modificación.

ls -X

Ordena los archivos por extensión.

ls -l

Enseña toda la información: usuario, grupo, permisos, tamaño, fecha y hora de creación.

ls -lh

Enseña la misma información que ls -l pero con las unidades de tamaño en KB, MB, etc.

ls -R

Enseña el contenido de todos los subdirectorios de forma recursiva.

ls -S

Ordena los resultados por tamaño de archivo. 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
mkdir: Este comando es utilizado para crear un nuevo subdirectorio o carpeta en el sistema de archivos. El nombre mkdir de las palabras make subdirectory que quieren decir: crear subdirectorio en inglés.

Ejemplo:

para crear un directorio con un nombre simple se puede usar por ejemplo mkdir Gerald

[code] mkdir myfiles [/code]
Crea un nuevo directorio llamado myfiles en el directorio actual.




---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
cd:  es usado para en sistemas operativos del tipo UNIX como GNU/Linux para cambiar el directorio de trabajo.

directorio especial .. o directorio padre, dará la posibilidad de mover tantos directorios hacia atrás como directorios padres se tengan. Si el usuario se encuentra en el directorio F del ejemplo y se ejecuta cd .. el usuario se desplazará un directorio hacia atrás, en cambio si desde el directorio F ejecutamos cd ../.. el usuario se moverá 2 directorios hacia atrás.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ip: Muestra todas las interfaces asociadas a la IP address
Ejemplos: ip -4 addr Parámetros: (i)> enseña y cambia las interfacez de la red, (r): muestra y cambia la tabla de rutas, (n): enseña y cambia objetos cercanos, enseña y cambia protocolos(addr/a)>
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
exit: Se utiliza para salir de la terminal que se está ejecutando.
Parámetros: N/A  
Ejemplos: $exit
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
lsb_release: Muestra una distribución más especifica de la información.

Parámetros:-i;--id: enseña la cadena string del distribuidor.
Ejemplos:  -v: Muestra la version LSB lsb_release -a,
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
clear: Se emplea para eliminar toda la información usada en la terminal y refrescarla.

Parámetros: N/A
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
pwd: muestra los directorios de diversos archivos.

Parámetros: -L: muestra el path simbólico, -P: muestra la terminal actual

Ejemplos: /logs$ /bin/pwd
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
/home: Hace la redirección al inicio de Linux
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Touch: Este comando es empleado para crear un archivo usando un tiempo específico  es un comando usado para crear, cambiar y modificar el tiempo de un documento.  
Parámetros: -a: puede entrar a algún documento, -c: es usado para crear o no un archivo, -c-d: usado para ingresar y modificar el tiempo, -m: es usado para cambiar la modificación del tiempo.  
Ejemplos: touch Doc1 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
cat:este comando es empleado para leer archivos sin editarlos, puede  ver, crear, y concatenar documentos. 
Ejemplos: $cat file 1file2
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
pacman: Es un comando para gestionar paquetes.

parámetros:

pacman -Syu: Actualiza el sistema y el software instalado.

pacman -Syuu: Este comando forza la actualización de la base de datos y actualiza todo.

pacman -Ss [paquete]: Busca un paquete con alguna palabra clave.

pacman -Qs [paquete]: Busca un paquete ya instalado.

pacman -S [paquete1]  [paquete2]: Instala varios paquetes.

pacman -Sw paquete: Descarga un paquete sin instalarlo.

pacman -R paquete: Desintala un paquete.

pacman -Qdt: Busca archivos huérfanos.

paccache -r: Borra cache de paquetes menos los tres más recientes.

pacman -Sc: Borra cache de paquetes que ya no están instalados.

pacman -Scc: Borrar toda la cache de paquetes.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ssh: Da comunicación encriptada y segura entre dos sistemas sobre una red que no es segura.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
cat  /proc/meminfo: Sirve para ver el contenido de un archivo, como memoria total, memoria disponible, buffers, etc.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
sudo dmidecode –type 17: Funciona igual que el anterior pero no sirve en una máquina virtual.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | lesse: Busca y dice cuales son los procesos que corren al momento en el Swap y cuales utilizan espacio ahí mismo.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
free -h: Muestra memoria disponible, cuánto en uso, cuánto Swap se está utilizando.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
swapon: Dice donde está ubicado un archivo Swap y su peso.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
cat /proc/sys/vm/swappiness: Dice la cantidad de procesos que se utilizan en memoria la RAM y el porcentaje que se usará en el SWAP.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
sudo mkdir /mnt/ram_disk: Sirve para montar una unidad RAM/DISK.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
sudo mount -t tmpfs -o size=1024m new_ram_disk /mnt/ram_disk: Funciona para montar sistemas de archivos en Linux.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
df  -h: Sirve para poder todos los sistemas de archivos corriendo en el equipo.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
apt- get install volatility: Programa qué permite tomar toda la memoria RAM que se tiene,se emplea a nivel forense.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Comandos de Metados de los archivos:
du -h foto.jpg: Tamaño del archivo.
stat archivo.jpg: Fecha de creación, último acceso.
file archivo.jpg: Tipo de archivo ( Carpeta. archivo, acceso directo).
chown user1 archivo.jpg chmod 777 archivo.jpg: Propietario y grupo, lista de permisos chown.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
df -h : Mostrar el espacio en disco usado.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
/etc/fstab mount /dev/cdrom /mnt: Montaje de dispositivos en el sistema de archivos.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
sudo apt install gparted: Gparted Administra las particiones.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
sudo apt install gnome-disk-utility: Muestra información sobre el disco.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
kill -9 $PID: Matar un proceso
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ps -aux: Mostrar los procesos.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
bash –version: Sirve para observar la versión instalada de bash en la pc.
Ejemplo:GNU bash, versión 4.4.19(1)-release (x86_64-suse-linux-gnu)
Copyright (C) 2016 Free Software Foundation, Inc.
Licencia GPLv3+: GPL de GNU versión 3 o posterior <http://gnu.org/licenses/gpl.html>
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
hostname: Este se encarga de establecer o mostrar el nombre del sistema además de obtener información de este.
Ejemplo: root@halo8000:~# hostname halo8000 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Parámetros:
-	hostname --fqdn: Da información de el FQDN (Nombre de Dominio Completamente Especificado)
-	-	hostname -i: Da la información de la IP del nodo del equipo.
-	hostname -f: Da el nombre del nodo completo con dominio en el DNS.
-	hostname -a: Da información de los alias del nodo.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
apt: Gestionar paquetes en Linux.
-	list - lista los paquetes dependiendo de los nombres
-	search - este parametro busca en las descripciones de los paquetes
-	show - muestra información del paquete 
-	install - instala paquetes
-	remove - elimina paquetes
-	autoremove - Elimina automáticamente todos los paquetes sin uso.
-	update - actualiza la lista de paquetes disponibles
-	upgrade - actualiza el sistema instalando.
-	full-upgrade - actualiza el sistema eliminando/instalando/actualizando los paquetes.
-	edit-sources - este edita el fichero de información de fuentes
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
echo: para ver la versión de Shell instalada
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
cat/ = cat /etc/shells: Ver los shells instalados.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
zsh: Interprete para comandos tipo Unix.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
chmod: Chmod +x script.sh = le otorga permisos de ejecutar a script.sh
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
8.	ls -l: ver permisos otorgados
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
