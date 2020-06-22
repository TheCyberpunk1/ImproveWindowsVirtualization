# improveWindowsVirtualization
mejorar la virtualización de una maquina Windows 7 en sistema operativo Ubuntu  11.10 - 11.04

Mejorar virtualización de maquina virtual windows, en un sistema operativo Linux ubuntu 11.10 - 11.04.
Un fin especifico, como seguridad o maquinas para invitados..

# EMPECEMOS
1 - creamos un nuevo usuario aparte del que ya tengas, como lo quieras llamar, por mi estuvo bien
colocarle w7, asignale un password para poder escojer una opcion mas adelante.

2 – dentro de ese usario, descarga e instala la virtual box

3- dentro de la virtual comienza a crear y a configurar la maquina virtual de w7, por preferencia a mi
maquina virtual le coloque “windows 7”, recomiendo que se le de una buena configuracion a tu
maquina virtual.

4- cundo ya hayas creado la virtual de w7. Vamos a crear algunas configuraciones.

# 5-pasos:
1-abrir el terminal.

2- teclear sudo su para darle permisos de administrador.

3- nos posicionamos en la carpeta necesaria, tecleamos cd /usr/share/xsessions.

4- tecleamos gedit w7.desktop como lo quieras llamar pero antes del punto.

5- se nos abrira gedit con el archivo creado.

6- dentro de gedit teclearemos lo siguiente tal y como esta, modifica lo que creas que se puede
modificar

[Desktop Entry]

Name=Microsoft Windows 7

Comment=This session logs you into GNOME

Exec=sh /home/w7/w7.sh

TryExec=sh

Icon=

Type=Application

X-Ubuntu-Gettext-Domain=gnome-session-2.0

Name[es_CO]=ubuntu

(esta linea Exec=sh /home//w7/w7.sh es la ruta del otro archivo que vamos a crear. esta es el nombre del escritorio Name=Microsoft Windows 7).

7 - ahora le damos guardar.

8 - despues de guardado vamos a crear el archivo de la linea 7.

9 - abrir un terminal nuevo.

10 - tecleamos cd /home/w7 para posicionarnos en nuestro usuario

11 – despues de eso teclamos gedit w7.sh que es el script que necesito de arranque de la virtual.

12 - como se te abre el archivo creado tecleamos en el lo siguiente.

#!/bin/bash

gnome-wm &

VirtualBox -startvm windows\ 7

13 - lo guardamos

(VirtualBox -startvm aqui el nombre de la maquina la mia es windows 7, como en consola no me acepta espacios coloco esta barra inclinada \ )

14 - por ahora todo esta listo , como estas dentro del usuario que creastes te recomiendo, que ejecutes esta linea para saber si la maquina virtual te le el comando.

VirtualBox -startvm windows\ 7

si te inicia la virtual todo estaria bien.

15 - cierras sesion. Cuando cierras sesion te debe aparecer, un usuario que es el w7 que ya has creado. acuerdate
que debe tener contrasenia almenos al principio, despues se la puedes quitar desde otro usuario.
Si inicias el usuario w7 en este momento, va a parecer igual sin iniciar nada, eso es por que se debe
configurar el escritorio para cada usuario.

16 - seleciona el usuario w7 si estas en ubuntu 11.10, y en el recuadro del usuario en la esquina superior
debe aparecer un iconito de configuracion, le das click, y debe aparecer, ubuntu, ubuntu 3d, y por
ultimo el mas importante, es el windows 7. ese lo selecionas, ahora inicia el usuario, y ya debe estar
completo.

17 - por ultimo que debes hacer, es que para que te de pantalla completa, debes instalar las guest additions virtualbox, y listo.
