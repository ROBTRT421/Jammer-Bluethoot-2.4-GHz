# :warning::warning::warning: ATENCION! :warning::warning::warning:
La producción, reproducción y el uso que se le dé a este repositorio, así como al dispositivo que a continuación se presenta, es responsabilidad de quien lo produce y usa, este repositorio es solamente con fines informativos, educativos y de demostración técnica, cualquier responsabilidad legal, residirá en quien decida replicarlo, 
el desconocimiento de la ley, no te exime de tus responsabilidades, se recomienda discreción y una amplia investigación sobre las leyes de tu país.

# Video: https://youtu.be/uYrIfBi0Qlg

# Prologo
El siguiente tutorial no es muy diferente a cualquiera que podremos encontrar en la plataforma, quizás la única diferencia es que esta echo en español y no omite ningún tipo de información para la realización del proyecto, no tiene ningún fin de lucro, al contrario, tiene la finalidad de nutrir el conocimiento y la curiosidad de las personas y cualquiera que llegue hasta aquí. Disfrútalo y Diviértete, todos los derechos reservados a quienes inspiraron y de quien es el código fuente, a continuación, dejamos los links para más información. 

https://github.com/smoochiee/Noisy-boy-esp32-Bluetooth-jammer

https://github.com/smoochiee/Bluetooth-jammer-esp32/tree/main

# Partes
Part Name            |      Amazon link       | Note
:------------------- | ---------------------- | :------------------------------------------------
ESP32 ESP-WROOM-32   | https://a.co/d/06vSPVuQ | Procura que sea este modelo, si cuentas con un modelo similar o distinto, documéntate y ajusta las conexiones 
NRF24                | https://a.co/d/09LNizxz | Existen muchos tipos y modelos, normalmente son las mismas terminales, documéntate y ajusta las conexiones
Placa Felonica 3cm x 5cm | https://a.co/d/0iKTH4Kn | procura cortarla a la medida para que todo embone perfecto, esto ya es a gustos y preferencias 
Tira Header Macho    | https://a.co/d/07ljQCwV | 
Capacitor 10uf 50 V  | https://a.co/d/0bNZ5SrL | 
Capacitor cerámico 100nf | https://a.co/d/0b53Ifid | 
Cables Puente            | https://a.co/d/06hiqdK2 |

# Tutorial
1. Adquiere las piezas usando la tabla anterior como referencia.

2. Realiza las debidas conexiones basándote en el siguiente diagrama:
![wiring diagram]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Diagrama.png "wiring diagram")

    2.1. Paso 1.
    ![Step1]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Paso%201..jpg "Paso 1.")

    2.2. Paso 2.
    ![Step2]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Paso%202..jpg "Paso 2.")

    2.3. Paso 3.
    ![Step3]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/paso%203..jpg "Paso 3.")

    2.4. Paso 4.
    ![Step4]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/paso%204..jpg "Paso 4.")

    2.5. Paso 5.
    ![Step5]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Paso%205..jpg "Paso 5.")

    2.6. Paso 6.
    ![Step6]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Paso%206..jpg "Paso 6.")

    2.7. Paso 7.
    ![Step7]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Paso%207..jpg "Paso 7.")


3. Una vez tengamos la base de nuestro dispositivo, continuamos con el flasheo de nuestro ESP32 por medio de la plataforma [IDE de Arduino](https://www.arduino.cc/en/Main/Software), ingresa a la página oficial y descarga la última versión del software, posteriormente asegúrate de descargar las librerías necesarias [RF24](https://github.com/nRF24/RF24) y [ezButton](https://arduinogetstarted.com/tutorials/arduino-button-library), sin olvidarnos de hacer los ajustes necesarios para que el IDE de Arduino, reconozca nuestra placa ESP32, carguemos [El Codigo](https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/FOR%20VSPI%20PIN.ino) en nuestro IDE y ahora si, estamos listos para el FLASHEO! :warning:

   ![Prepare]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/IDE%20Preparado.png "Prepare.")


# FLASHEO
![Flasheo]( https://github.com/ROBTRT421/Jammer-Bluethoot-2.4-GHz/blob/main/Flasheo%20ESP32%20(1).gif "Flasheo")

# TODO LISTO! D I S F R U T A L O :smile:

# :warning: NOTAS IMPORTANTES :warning:
El código y el proyecto esta echo para 2 módulos de NRF24 y un "switch" de encendido, sin embargo aquí solo utilizamos 1 módulo NRF24 sin "switch" de encendido, si quisieras utilizar 2 módulos NFR24 controlados por 1 solo ESP32 la conexiones se muestran en la siguiente tabla 

Módulo 1             |      ESP32             |Módulo 2             |      ESP32             |
:------------------- | ---------------------- | ------------------- | ---------------------- |
VCC                  | 3.3V                   | VCC                 | 3.3V                   |
GND                  | GND                    | GND                 | GND                    |
SCK                  | PIN 14                 | SCK                 | PIN 18                 |
MISO                 | PIN 12                 | MISO                | PIN 19                 |
MOSI                 | PIN 13                 | MOSI                | PIN 23                 |
CS/CSN               | PIN 15                 | CS/CSN              | PIN 21                 |
CE                   | PIN 16                 | CE                  | PIN 22                 |
