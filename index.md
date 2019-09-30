Bienvenido al AIoT /Edge Computing.

Para comenzar a utilizar tu Maixduino y encontrar toda la información técnica, te recomendamos la siguiente información:

*Conceptos básicos:  
Maixduino es una placa con dos procesadores/SoCs:

1.  ESP32: Procesador general con WiFi y BLE, optimizado para IoT.
2.  K210: Procesador general RISC-V con acelerador de CNNs, optimizado para AI.  
    Ambos están interconectados en el PCB por SPI.  
    Cada procesador se programa a través de un puerto serial propio. Para ello la placa tiene un convertidor USB a TTL de dos puertos.

Sipeed es el fabricante de la placa, Espressif del ESP32 y Kendryte del K210. Los tres tienen información relevante y complementaria para usar tu Maixduino.

El K210 puede programarse:

1.  Micropython (maixpy es la variante del fabricante).  _RECOMENDADO_
2.  C++ con un SDK open source.
3.  Arduino IDE (o PlatformIO).

El ESP32 puede programarse:

1.  Arduino IDE (o PlatformIO).  _RECOMENDADO_
2.  C++ con el ESP-IDF.
3.  Micropython y otros wrappers.

En nuestras pruebas y varios tutoriales se usa como ambiente de desarrollo Ubuntu 18.04 LTS. Te recomedamos que lo utilices, sin embargo OSX/MacOS o Windows también pueden funcionar si estás familiarizado con ellos.

Los puertos GPIO son configurables a 1.8 o 3.3v, dependiendo del SoC que estés usando. MUY IMPORTANTE: aunque puede ser compatible con shields/hats para Arduino UNO físicamente, debes asegurarte que el voltaje es compatible. Maixduino NO TOLERA niveles lógicos de 5V, si los usas dañaras irreversiblemente los puertos o el SoC.

La alimentación puede ser por el puerto micro USB C  @5V o con una fuente en el barril con voltajes de 6 a 12 V.

*Tutorial para iniciar.  
El siguiente tutorial (inglés) explica cómo empezar con el uso básico de la cámara y face tracking. La explicación es muy buena e incluye un proceso de “prueba y error” con las versiones de maixpy. Para agilizarlos te recomendamos que uses la versión de maixpy (24/08/2019) maixpy_v0.4.0_46_gf46e4c4.bin que puedes descargar directamente aquí:  
[http://dl.sipeed.com/MAIX/MaixPy/release/master/maixpy_v0.4.0_46_gf46e4c4](http://dl.sipeed.com/MAIX/MaixPy/release/master/maixpy_v0.4.0_46_gf46e4c4)  y que personalmente hemos probado que funciona con MaixPyIDE y el ejemplo de face tracking.

El tutorial:  
[https://www.cnx-software.com/2019/08/21/getting-started-with-sipeed-m1-based-maixduino-board-grove-ai-hat-for-raspberry-pi](https://www.cnx-software.com/2019/08/21/getting-started-with-sipeed-m1-based-maixduino-board-grove-ai-hat-for-raspberry-pi)

Otro tip que podemos darte, es que el IDE de MaixPy (MaixPy IDE, se menciona en el tutorial) puede servirte para transferir el ejemplo al K210 y así no es necesario copiar línea por línea el código como lo sugiere el tutorial. Lo único que se requiere es que el archivo sea nombrado  [boot.py](http://boot.py/)  y ése será el primer archivo que se ejecute. Se puede hacer desde MaixPyIDE desde el menú Tools->Save open script to board ([boot.py](http://boot.py/)).

*Otros ejemplos interesantes:  
MaixPy Run 20-classes object detection based on tiny-yolov2:  
[https://bbs.sipeed.com/t/topic/683](https://bbs.sipeed.com/t/topic/683)

Transformada Rápida de Fourier (El K210 tienen un acelerador de FFT por hardware). Usa el micrófono integrado en la placa:  
[https://maixpy.sipeed.com/en/libs/Maix/fft.html](https://maixpy.sipeed.com/en/libs/Maix/fft.html)

Convertir modelo TensorFlow Lite .tflite a K210 .kmodel:  
[https://github.com/kendryte/nncase/tree/master/examples/iris](https://github.com/kendryte/nncase/tree/master/examples/iris)  
Basado en el modelo de clasificación de Iris de Tensor Flow:  
[https://www.tensorflow.org/guide/premade_estimators](https://www.tensorflow.org/guide/premade_estimators)

*Documentación oficial:  
Sipeed.  
foro:  [https://bbs.sipeed.com/](https://bbs.sipeed.com/)  
wiki:  [https://wiki.sipeed.com/en/maix/board/maixduino.html](https://wiki.sipeed.com/en/maix/board/maixduino.html)  
github:  [https://github.com/sipeed?utf8=✓&q=maix&type=&language=](https://github.com/sipeed?utf8=%E2%9C%93&q=maix&type=&language=)

Kendryte:  
foro:  [https://forum.kendryte.com/](https://forum.kendryte.com/)  
github:  [https://github.com/kendryte](https://github.com/kendryte)

*Documentación ESP32:  
[https://cosismo.github.io/esp32-devkit/](https://cosismo.github.io/esp32-devkit/)

*Grupo de Facebook en español sobre Internet de las Cosas:  
[https://www.facebook.com/groups/724628401049648/](https://www.facebook.com/groups/724628401049648/)

*Grupo de Facebook en inglés sobre AI /Deep Learning:  
[https://www.facebook.com/groups/DeepNetGroup/](https://www.facebook.com/groups/DeepNetGroup/)

Quedamos a tus órdenes por esta vía.

¡Suerte!  
Equipo Cosismo
