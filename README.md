# Informe-Lab-3 Problema del coctel 
## Introducción
En entornos sociales donde hay multiples fuentes sonoras, como en este caso una fiesta de coctel es donde se pone a prueba el procesamiento de señales frentea aislar una sola voz dentro de una mezcla de diferentes sonidos, por esta razon el objetivo de este laboratorio es recrear la situacion problema utilizando tres microfonos que nos permitan evidenciar diferentes fuentes para aplicar tecnicas de analisis en frecuencia para separar la señal de interes. Todo esto a partir de herramientas comola transformada rapida de fourier y metodos de separacion de fuentes.
## Tratamiento de la señal
Para lograr separar una voz especifica de una mezcla de fuentes sonoras que se captaron a partir de microfonos, es necesario recurrir a metodos matematicos que nos permitan anakizar, transformar y extraer informacion fundamental de la señal. Por esta razon la transformada de fourier discreta nos permite descomponer la señal en sus componentes de frecuencia y ser analizada espectralmente, la transfromada rapida de fourier permite un analisis de la señal en tiempo real y donde se ubica la misma.

SNR de MICROFONO_CARLOS.mp3: 21.88 dB

SNR de MICROFONO_DIEGO.mp3: 20.44 dB

SNR de MICROFONO_GABY.mp3: 20.66 dB

Por medio del analisis de componentes independientes se busca separar separar las fuentes para encontrar las señales independientes del conjunto de audio; cada señal tiene carcterisiticas estadisticas unicas, lo que permite encontrar la voz original eliminando inetrferencias de otras voces.

![](https://github.com/gaby2804/Lab-3-Coctel/blob/main/ica.png)
