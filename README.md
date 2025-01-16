# PASOS PARA INYECTAR UNA REVERSESHELL EN UN EQUIPO DESDE UN FLIPPER ZERO.

1.Entra en Kali linux y ponlo en modo escucha con la aplicación NetCat con el comando "nc -lvnp <"Número de Puerto">".






2.Descarga el archivo REVERSE_SHELL.txt que hay alojado en el proyecto, y modifica el apartado de ip, por la ip de tu máquina atacante, y el puerto, por el puerto que hayas seleccionado previamente en NetCat.






3.Conecta el Flipper con USB a tu ordenador y descarga la aplicación qFlipper. Una vez dentro, entra en la opción de READ FILE, selecciona la tarjeta sd previamente colocada, y pega el REVERSE_SHELL.txt en la carpeta BADUSB.






4.Una vez conectado el flipper al pc, navega por el menú de este, selecciona bad usb y ejecuta el REVERSESHELL previamente subido. (Asegurate de que el teclado esta en Español) 


















