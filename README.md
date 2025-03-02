# Informe-Lab-3 Problema del coctel 
## Introducción
En entornos sociales donde hay multiples fuentes sonoras, como en este caso una fiesta de coctel es donde se pone a prueba el procesamiento de señales frentea aislar una sola voz dentro de una mezcla de diferentes sonidos, por esta razon el objetivo de este laboratorio es recrear la situacion problema utilizando tres microfonos que nos permitan evidenciar diferentes fuentes para aplicar tecnicas de analisis en frecuencia para separar la señal de interes. Todo esto a partir de herramientas comola transformada rapida de fourier y metodos de separacion de fuentes.

## Procedimiento
### Tratamiento de la señal
Para lograr separar una voz especifica de una mezcla de fuentes sonoras que se captaron a partir de microfonos, es necesario recurrir a metodos matematicos que nos permitan analizar, transformar y extraer informacion fundamental de la señal. Por esta razon la transformada de fourier discreta (DFT) nos permite descomponer la señal en sus componentes de frecuencia y ser analizada espectralmente, la transfromada rapida de fourier (FFT) permite un analisis de la señal en tiempo real y donde se ubica la misma.

SNR de MICROFONO_CARLOS.mp3: 21.88 dB

SNR de MICROFONO_DIEGO.mp3: 20.44 dB

SNR de MICROFONO_GABY.mp3: 20.66 dB

Por medio del analisis de componentes independientes (ICA) se busca separar separar las fuentes para encontrar las señales independientes del conjunto de audio; cada señal tiene carcterisiticas estadisticas unicas, lo que permite encontrar la voz original eliminando inetrferencias de otras voces.

![](https://github.com/gaby2804/Lab-3-Coctel/blob/main/ica.png)

Donde se extraen 4 fuentes que corresponden a los tres microfonos y al ruido. 

Para seleccionar la fuente correspondiente a la voz de Carlos se planteo lo siquiente:

![](https://github.com/gaby2804/Lab-3-Coctel/blob/main/correlacion.png)

Alli se calcula la correlacion entre cada fuente extraida y la señal emitida por el microfono de Carlos, se normaliza el coeficiente de correlación para que esté entre 0 y 1, por ultimo se selecciona la fuente con la mayor correlación (microfono de carlos), asumiendo que es la voz de Carlos.

La tecnica de Beamforming es util en arreglos para los microfonos, donde se centra el sonido en una direccion mientras atenua el resto, aprovechando las diferencias de fase y tiempo, ya que enfoca el audiohacia una persona mejorando asi la legibilidad en el entorno ruidoso.

![](https://github.com/gaby2804/Lab-3-Coctel/blob/main/beamforming)

Se utiliza solo el primer valor singular porque suele representar la señal más fuerte (la voz de Carlos), esto ayuda a eliminar el ruido y otras voces, en otros modos contienen más interferencias.



## Analisis de graficas

