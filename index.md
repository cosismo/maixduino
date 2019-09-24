<p class="has-line-data" data-line-start="0" data-line-end="1">Bienvenido al AIoT /Edge Computing.</p>
<p class="has-line-data" data-line-start="2" data-line-end="3">Para comenzar a utilizar tu Maixduino y encontrar toda la información técnica, te recomendamos la siguiente información:</p>
<p class="has-line-data" data-line-start="4" data-line-end="6">*Conceptos básicos:<br>
Maixduino es una placa con dos procesadores/SoCs:</p>
<ol>
<li class="has-line-data" data-line-start="6" data-line-end="7">ESP32: Procesador general con WiFi y BLE, optimizado para IoT.</li>
<li class="has-line-data" data-line-start="7" data-line-end="11">K210: Procesador general RISC-V con  acelerador de CNNs, optimizado para AI.<br>
Ambos están interconectados en el PCB por SPI.<br>
Cada procesador se programa a través de un puerto serial propio. Para ello la placa tiene un convertidor USB a TTL de dos puertos.</li>
</ol>
<p class="has-line-data" data-line-start="11" data-line-end="12">Sipeed es el fabricante de la placa, Espressif del ESP32 y Kendrite del K210. Los tres tienen información relevante y complementaria para usar tu Maixduino.</p>
<p class="has-line-data" data-line-start="13" data-line-end="14">El K210 puede programarse:</p>
<ol>
<li class="has-line-data" data-line-start="14" data-line-end="15">Micropython (maixpy es la variante del fabricante). <em>RECOMENDADO</em></li>
<li class="has-line-data" data-line-start="15" data-line-end="16">C++ con un SDK open source.</li>
<li class="has-line-data" data-line-start="16" data-line-end="18">Arduino IDE (o PlatformIO).</li>
</ol>
<p class="has-line-data" data-line-start="18" data-line-end="19">El ESP32 puede programarse:</p>
<ol>
<li class="has-line-data" data-line-start="19" data-line-end="20">Arduino IDE (o PlatformIO).  <em>RECOMENDADO</em></li>
<li class="has-line-data" data-line-start="20" data-line-end="21">C++ con el ESP-IDF.</li>
<li class="has-line-data" data-line-start="21" data-line-end="23">Micropython y otros wrappers.</li>
</ol>
<p class="has-line-data" data-line-start="23" data-line-end="24">En nuestras pruebas y varios tutoriales se usa como ambiente de desarrollo Ubuntu 18.04 LTS. Te recomedamos que lo utilices, sin embargo OSX/MacOS o Windows también pueden funcionar si estás familiarizado con ellos.</p>
<p class="has-line-data" data-line-start="25" data-line-end="28">*Tutorial para iniciar.<br>
El siguiente tutorial (inglés) explica cómo empezar con el uso básico de la cámara y face tracking.   La explicación es muy buena e incluye un proceso de “prueba y error” con las versiones de maixpy. Para agilizarlos te recomendamos que uses la versión de maixpy  (24/08/2019) maixpy_v0.4.0_46_gf46e4c4.bin  que puedes descargar directamente aquí:<br>
<a href="http://dl.sipeed.com/MAIX/MaixPy/release/master/maixpy_v0.4.0_46_gf46e4c4">http://dl.sipeed.com/MAIX/MaixPy/release/master/maixpy_v0.4.0_46_gf46e4c4</a> y que personalmente hemos probado que funciona con MaixPyIDE y el ejemplo de face tracking.</p>
<p class="has-line-data" data-line-start="29" data-line-end="31">El tutorial:<br>
<a href="https://www.cnx-software.com/2019/08/21/getting-started-with-sipeed-m1-based-maixduino-board-grove-ai-hat-for-raspberry-pi">https://www.cnx-software.com/2019/08/21/getting-started-with-sipeed-m1-based-maixduino-board-grove-ai-hat-for-raspberry-pi</a></p>
<p class="has-line-data" data-line-start="32" data-line-end="33">Otro tip que podemos darte, es que el IDE de MaixPy  (MaixPy IDE, se menciona en el tutorial) puede servirte para transferir el ejemplo al K210 y así no es necesario copiar línea por línea el código como lo sugiere el tutorial.  Lo único que se requiere es que el archivo sea nombrado <a href="http://boot.py">boot.py</a> y ése será el primer archivo que se ejecute. Se puede hacer desde MaixPyIDE desde el menú Tools-&gt;Save open script to board (<a href="http://boot.py">boot.py</a>).</p>
<p class="has-line-data" data-line-start="34" data-line-end="37">*Otros ejemplos interesantes:<br>
MaixPy Run 20-classes object detection based on tiny-yolov2:<br>
<a href="https://bbs.sipeed.com/t/topic/683">https://bbs.sipeed.com/t/topic/683</a></p>
<p class="has-line-data" data-line-start="38" data-line-end="40">Transformada Rápida de Fourier (El K210 tienen un acelerador de FFT por hardware). Usa el micrófono integrado en la placa:<br>
<a href="https://maixpy.sipeed.com/en/libs/Maix/fft.html">https://maixpy.sipeed.com/en/libs/Maix/fft.html</a></p>
<p class="has-line-data" data-line-start="41" data-line-end="45">Convertir modelo TensorFlow Lite .tflite a K210 .kmodel:<br>
<a href="https://github.com/kendryte/nncase/tree/master/examples/iris">https://github.com/kendryte/nncase/tree/master/examples/iris</a><br>
Basado en el modelo de clasificación de Iris de Tensor Flow:<br>
<a href="https://www.tensorflow.org/guide/premade_estimators">https://www.tensorflow.org/guide/premade_estimators</a></p>
<p class="has-line-data" data-line-start="46" data-line-end="51">*Documentación oficial:<br>
Sipeed.<br>
foro: <a href="https://bbs.sipeed.com/">https://bbs.sipeed.com/</a><br>
wiki: <a href="https://wiki.sipeed.com/en/maix/board/maixduino.html">https://wiki.sipeed.com/en/maix/board/maixduino.html</a><br>
github: <a href="https://github.com/sipeed?utf8=%E2%9C%93&amp;q=maix&amp;type=&amp;language=">https://github.com/sipeed?utf8=✓&amp;q=maix&amp;type=&amp;language=</a></p>
<p class="has-line-data" data-line-start="52" data-line-end="55">Kendrite:<br>
foro: <a href="https://forum.kendryte.com/">https://forum.kendryte.com/</a><br>
github: <a href="https://github.com/kendryte">https://github.com/kendryte</a></p>
<p class="has-line-data" data-line-start="56" data-line-end="58">*Documentación ESP32:<br>
<a href="https://cosismo.github.io/esp32-devkit/">https://cosismo.github.io/esp32-devkit/</a></p>
<p class="has-line-data" data-line-start="59" data-line-end="61">*Grupo de Facebook en español sobre Internet de las Cosas:<br>
<a href="https://www.facebook.com/groups/724628401049648/">https://www.facebook.com/groups/724628401049648/</a></p>
<p class="has-line-data" data-line-start="62" data-line-end="64">*Grupo de Facebook en inglés sobre AI /Deep Learning:<br>
<a href="https://www.facebook.com/groups/DeepNetGroup/">https://www.facebook.com/groups/DeepNetGroup/</a></p>
<p class="has-line-data" data-line-start="66" data-line-end="67">Quedamos a tus órdenes por esta vía.</p>
<p class="has-line-data" data-line-start="69" data-line-end="71">¡Suerte!<br>
Equipo Cosismo</p>
