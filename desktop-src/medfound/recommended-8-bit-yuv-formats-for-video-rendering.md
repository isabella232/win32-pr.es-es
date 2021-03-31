---
description: Formatos YUV de 8 bits recomendados para la representación de vídeo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formatos YUV de 8 bits recomendados para la representación de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811569"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formatos YUV de 8 bits recomendados para la representación de vídeo

Gary Sullivan y Stephen Estrop

Microsoft Corporation

2002 de abril, actualizado el 2008 de noviembre

En este tema se describen los formatos de color YUV de 8 bits que se recomiendan para la representación de vídeo en el sistema operativo Windows. En este artículo se presentan técnicas para la conversión entre formatos YUV y RGB, y también se proporcionan técnicas para el muestreo de formatos YUV. Este artículo está destinado a cualquier persona que trabaje con la descodificación o representación de vídeo YUV en Windows.

## <a name="introduction"></a>Introducción

Muchos formatos YUV se definen en todo el sector del vídeo. En este artículo se identifican los formatos YUV de 8 bits que se recomiendan para la representación de vídeo en Windows. Se recomienda a los proveedores de descodificadores y mostrar los proveedores que admitan los formatos descritos en este artículo. En este artículo no se tratan otros usos del color YUV, como la fotografía todavía.

En los formatos descritos en este artículo se usa una ubicación de 8 bits por píxel para codificar el canal Y (también denominado canal de luminancia) y usar 8 bits por muestra para codificar cada ejemplo de croma U o V. Sin embargo, la mayoría de los formatos YUV usan menos de 24 bits por píxel en promedio, ya que contienen menos muestras de usted y V que de Y. En este artículo no se tratan los formatos YUV con canales Y de 10 bits o superior.

> [!Note]  
> Para los fines de este artículo, el término U es equivalente a CB y el término V es equivalente a CR.

 

En este artículo se tratan los temas siguientes:

-   [Muestreo YUV](#yuv-sampling). Describe las técnicas de muestreo YUV más comunes.
-   [Definiciones de Surface](#surface-definitions). Describe los formatos YUV recomendados.
-   [Conversiones del espacio de colores y de la frecuencia de muestreo de croma](#color-space-and-chroma-sampling-rate-conversions). Proporciona algunas directrices para la conversión entre formatos YUV y RGB, y para la conversión entre distintos formatos YUV.
-   [Identificar formatos YUV en Media Foundation](#identifying-yuv-formats-in-media-foundation). Explica cómo describir los tipos de formato YUV en Media Foundation.

## <a name="yuv-sampling"></a>Muestreo YUV

Los canales de croma pueden tener una velocidad de muestreo inferior a la del canal de luminancia, sin ninguna pérdida dramática de calidad perceptual. Una notación denominada "A:B: C" se usa para describir la frecuencia con la que se muestrean y las V en relación con Y:

-   4:4:4 significa que no hay una disminución de la resolución de los canales de croma.
-   4:2:2 significa una disminución de la resolución horizontal de 2:1, sin disminución de la resolución vertical. Cada línea de exploración contiene cuatro ejemplos Y por cada uno de los dos ejemplos U o V.
-   4:2:0 significa disminución de la reducción horizontal de 2:1, con una disminución de resolución de 2:1.
-   4:1:1 significa una disminución de la resolución horizontal de 4:1, sin disminución de la resolución vertical. Cada línea de exploración contiene cuatro ejemplos y para cada ejemplo de cada usuario y V. el muestreo 4:1:1 es menos común que otros formatos y no se describe en detalle en este artículo.

En los diagramas siguientes se muestra cómo se muestrea el cromado para cada una de las tasas de reducción de la resolución. Los ejemplos de luminancia se representan mediante una cruz y las muestras de croma se representan mediante un círculo.

![Figura 1. muestreo de croma](images/yuv-sampling-grids.png)

La forma dominante de muestreo 4:2:2 se define en la recomendación de ITU-R BT. 601. Hay dos variantes comunes del muestreo 4:2:0. Uno de ellos se usa en vídeo MPEG-2 y el otro se usa en MPEG-1 y en las recomendaciones de ITU-T H. 261 y H. 263.

En comparación con el esquema MPEG-1, es más fácil convertir entre el esquema MPEG-2 y las cuadrículas de muestreo definidas para los formatos 4:2:2 y 4:4:4. Por esta razón, se prefiere el esquema MPEG-2 en Windows y se debe considerar la interpretación predeterminada de los formatos 4:2:0.

## <a name="surface-definitions"></a>Definiciones de Surface

En esta sección se describen los formatos YUV de 8 bits que se recomiendan para la representación de vídeo. Estas se dividen en varias categorías:

-   [formatos 4:4:4, 32 bits por píxel](#444-formats-32-bits-per-pixel)
-   [formatos de 4:2:2, 16 bits por píxel](#422-formats-16-bits-per-pixel)
-   [formatos de 4:2:0, 16 bits por píxel](#420-formats-16-bits-per-pixel)
-   [4:2:0 formatos, 12 bits por píxel](#420-formats-12-bits-per-pixel)

En primer lugar, debe tener en cuenta los siguientes conceptos para comprender lo siguiente:

-   *Origen* de la superficie. En el caso de los formatos YUV descritos en este artículo, el origen (0,0) siempre es la esquina superior izquierda de la superficie.
-   *STRIDE*. El paso de una superficie, a veces denominado paso, es el ancho de la superficie en bytes. Dado un origen de superficie en la esquina superior izquierda, el intervalo siempre es positivo.
-   *Alineación*. La alineación de una superficie es a discreción del controlador de pantalla de gráficos. La superficie siempre debe estar alineada con DWORD; es decir, se garantiza que las líneas individuales dentro de la superficie se originen en un límite de 32 bits (DWORD). Sin embargo, la alineación puede ser superior a 32 bits, en función de las necesidades del hardware.
-   Formato empaquetado frente al formato plano. Los formatos YUV se dividen en formatos *empaquetados* y formatos *planos* . En un formato empaquetado, los componentes Y, U y V se almacenan en una sola matriz. Los píxeles se organizan en grupos de macropixels, cuyo diseño depende del formato. En un formato plano, los componentes Y, U y V se almacenan como tres planos independientes.

Cada uno de los formatos YUV descritos en este artículo tiene un código FOURCC asignado. Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.

-   4:4:4 (32 BPP)
    -   [AYUV](#ayuv)
-   4:2:2 (16 BPP)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 BPP)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 BPP)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>formatos 4:4:4, 32 bits por píxel

### <a name="ayuv"></a>AYUV

Se recomienda un solo formato 4:4:4, con el código FOURCC AYUV. Se trata de un formato empaquetado, donde cada píxel se codifica como cuatro bytes consecutivos, organizados en la secuencia que se muestra en la siguiente ilustración.

![Figura 2. diseño de memoria de ayuv](images/yuvformats01.gif)

Los bytes marcados como contienen valores para alfa.

## <a name="422-formats-16-bits-per-pixel"></a>formatos de 4:2:2, 16 bits por píxel

Se recomiendan dos formatos 4:2:2, con los siguientes códigos FOURCC:

-   YUY2
-   UYVY

Ambos son formatos empaquetados, donde cada macropixel es dos píxeles codificados como cuatro bytes consecutivos. Esto da como resultado una disminución de la intensidad horizontal del croma en un factor de dos.

### <a name="yuy2"></a>YUY2

En el formato YUY2, los datos se pueden tratar como una matriz de valores **Char** sin signo, donde el primer byte contiene el primer ejemplo y, el segundo byte contiene el primer ejemplo de U (CB), el tercer byte contiene el segundo ejemplo y y el cuarto byte contiene el primer ejemplo V (CR), como se muestra en el diagrama siguiente.

![Figura 3. diseño de memoria de YUY2](images/yuvformats02.gif)

Si la imagen se dirige como una matriz de valores de **palabra** Little-endian, la primera **palabra** contiene el primer ejemplo y en los bits menos significativos (LSBs) y el primer ejemplo de U (CB) en los bits más significativos (MSBs). La segunda **palabra** contiene el segundo ejemplo y en el LSBs y el primer ejemplo V (CR) de MSBs.

YUY2 es el formato de 4:2:2 píxeles preferido para la aceleración de vídeo de Microsoft DirectX (DirectX VA). Se espera que sea un requisito intermedio para los aceleradores de DirectX, que admiten vídeo de 4:2:2.

### <a name="uyvy"></a>UYVY

Este formato es el mismo que el formato YUY2, excepto en que se invierte el orden de los bytes; es decir, se voltean los bytes de croma y luminancia (Figura 4). Si la imagen se dirige como una matriz de dos valores de **palabra** Little-endian, la primera **palabra** contiene U en LSBs y Y0 en MSBs, y la segunda **palabra** contiene V en LSBs y Y1 en el MSBs.

![Figura 4. diseño de memoria de UYVY](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>formatos de 4:2:0, 16 bits por píxel

Se recomiendan dos formatos de 4:2:0 16 bits por píxel (BPP), con los siguientes códigos FOURCC:

-   IMC1
-   IMC3

Ambos formatos YUV son formatos planos. Los canales de croma se submuestran por un factor de dos en las dimensiones horizontal y vertical.

### <a name="imc1"></a>IMC1

Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo. A continuación se muestran todos los ejemplos de V (CR) y, a continuación, todos los ejemplos de U (CB). Los planos V y U tienen el mismo intervalo que el plano Y, lo que da lugar a áreas de memoria no utilizadas, tal como se muestra en la figura 5. Los planos de ti y V deben comenzar en los límites de memoria que tengan un múltiplo de 16 líneas. En la figura 5 se muestra el origen de usted y V para un fotograma de vídeo 352 x 240. La dirección inicial de los planos de ti y V se calcula de la siguiente manera:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

donde *py* es un puntero de byte al inicio de la matriz de memoria, tal y como se muestra en el diagrama siguiente.

![Figura 5. diseño de memoria de imc1 (ejemplo)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Este formato es idéntico a IMC1, excepto en que se intercambian los planos usted y V, como se muestra en el diagrama siguiente.

![Figura 6. diseño de memoria de imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>4:2:0 formatos, 12 bits por píxel

Se recomiendan cuatro formatos 4:2:0 12-BPP, con los siguientes códigos FOURCC:

-   IMC2
-   IMC4
-   YV12
-   NV12

En todos estos formatos, los canales de croma se submuestran por un factor de dos en las dimensiones horizontal y vertical.

### <a name="imc2"></a>IMC2

Este formato es el mismo que el de IMC1, excepto por la diferencia siguiente: las líneas V (CR) y U (CB) se intercalan en los límites de medio STRIDE. En otras palabras, cada línea de paso completo en el área de croma comienza con una línea de ejemplos de V, seguida de una línea de muestras de U que comienza en el siguiente límite de intervalo medio (Figura 7). Este diseño hace un uso más eficaz del espacio de direcciones que IMC1. Reduce el espacio de direcciones de croma en la mitad y, por tanto, el espacio de direcciones total en un 25 por ciento. Entre los formatos 4:2:0, IMC2 es el segundo formato preferido, después de NV12. En la imagen siguiente se ilustra este proceso.

![Figura 7. diseño de memoria de imc2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Este formato es idéntico a IMC2, excepto que se intercambian las líneas U (CB) y V (CR), tal y como se muestra en la siguiente ilustración.

![Ilustración 8. diseño de memoria de imc4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo. Esta matriz va seguida inmediatamente de todos los ejemplos V (CR). El paso del plano V es la mitad del intervalo del plano Y; y el plano V contiene la mitad de tantas líneas como el plano Y. El plano V va seguido inmediatamente de todos los ejemplos de U (CB), con el mismo intervalo y número de líneas que el plano V, tal como se muestra en la siguiente ilustración.

![Ilustración 9. diseño de memoria de YV12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo con un número par de líneas. El plano Y va seguido inmediatamente de una matriz de valores **Char** sin signo que contiene ejemplos empaquetados de U (CB) y V (CR). Cuando la matriz de U-V combinada se dirige como una matriz de valores de **palabra** Little-endian, LSBs contiene los valores U y MSBs contiene los valores V. NV12 es el formato preferido de 4:2:0 píxeles para DirectX VA. Se espera que sea un requisito intermedio para los aceleradores de DirectX, que admiten vídeo de 4:2:0. En la ilustración siguiente se muestra el plano y y la matriz que contiene ejemplos empaquetados y de V.

![Figura 10. diseño de memoria de nv12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversiones del espacio de colores y de la frecuencia de muestreo de croma

En esta sección se proporcionan instrucciones para la conversión entre YUV y RGB, y para la conversión entre algunos formatos YUV diferentes. Tenemos en cuenta dos esquemas de codificación RGB en esta sección: *RGB de 8 bits*, también conocido como sRGB o "RGB de imagen a gran escala", RGB de *estudio de vídeo* o "RGB con sala de cabezas". Se definen de la siguiente manera:

-   El equipo RGB usa 8 bits para cada muestra de rojo, verde y azul. El color negro se representa mediante R = G = B = 0 y el blanco se representa mediante R = G = B = 255.
-   Studio video RGB usa un número de bits N para cada muestra de rojo, verde y azul, donde N es 8 o más. El vídeo RGB de Studio usa un factor de escala diferente del de equipo RGB y tiene un desplazamiento. El negro se representa mediante R = G = B = 16 \* 2 ^ (N-8) y el blanco se representa mediante r = G = B = 235 \* 2 ^ (N-8). Sin embargo, los valores reales pueden quedar fuera de este intervalo.

Studio video RGB es la definición de RGB preferida para el vídeo en Windows, mientras que el equipo RGB es la definición de RGB preferida para las aplicaciones que no son de vídeo. En cualquier forma de RGB, las coordenadas de cromaticidad se especifican en ITU-R BT. 709 para la definición de los valores primarios de color RGB. Las coordenadas (x, y) de R, G y B son (0,64, 0,33), (0,30, 0,60) y (0,15, 0,06), respectivamente. El blanco de referencia es D65 con coordenadas (0,3127, 0,3290). La gamma nominal es de 1/0.45 (aproximadamente 2,2), con un gamma preciso definido en detalle en ITU-R BT. 709.

**Conversión entre RGB y 4:4:4 YUV**

En primer lugar, se describe la conversión entre RGB y 4:4:4 YUV. Para convertir 4:2:0 o 4:2:2 YUV en RGB, se recomienda convertir los datos de YUV en 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB. El formato AYUV, que es un formato 4:4:4, usa 8 bits cada uno para los ejemplos Y, U y V. YUV también puede definirse con más de 8 bits por muestra para algunas aplicaciones.

Se han definido dos conversiones de YUV dominantes de RGB para vídeo digital. Ambos se basan en la especificación conocida como recomendación de ITU-R BT. 709. La primera conversión es el formato YUV anterior definido para el uso de 50 Hz en BT. 709. Es igual que la relación especificada en la recomendación de ITU-R BT. 601, también conocida por su nombre anterior, CCIR 601. Se debe considerar el formato YUV preferido para la resolución de TV de definición estándar (720 x 576) y el vídeo de menor resolución. Se caracteriza por los valores de dos constantes *KR* y *KB*:

``` syntax
Kr = 0.299
Kb = 0.114
```

La segunda conversión es el formulario YUV más reciente definido para el uso de 60 Hz en BT. 709 y debe considerarse el formato preferido para las resoluciones de vídeo anteriores a SDTV. Se caracteriza por valores diferentes para estas dos constantes:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

La conversión de RGB a YUV se define a partir de lo siguiente:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

Los valores YUV se obtienen de la manera siguiente:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

where

-   M es el número de bits por muestra YUV (M >= 8).
-   Z es la variable de nivel negro. En el caso del equipo RGB, Z es igual a 0. En Studio video RGB, Z \* es igual a 16 2 ^ (n-8), donde N es el número de bits por ejemplo RGB (n >= 8).
-   S es la variable de escalado. En el caso del equipo RGB, S es igual a 255. Para Studio video RGB, S es igual \* a 219 2 ^ (N-8).

La función Floor (x) devuelve el número entero más grande menor o igual que x. La función clip3 (x, y, z) se define de la siguiente manera:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> clip3 debe implementarse como una función en lugar de una macro de preprocesador; de lo contrario, se producirán varias evaluaciones de los argumentos.

 

El ejemplo Y representa el brillo, y los ejemplos de ti y V representan las desviaciones de color hacia el azul y el rojo, respectivamente. El intervalo nominal para Y es 16 \* 2 ^ (m-8) a 235 \* 2 ^ (M-8). El color negro se representa como 16 \* 2 ^ (m-8) y el blanco se representa como 235 \* 2 ^ (m-8). El intervalo nominal para usted y V son 16 \* 2 ^ (m-8) a 240 \* 2 ^ (M-8), con el valor 128 \* 2 ^ (m-8) que representa el croma neutro. Sin embargo, los valores reales pueden estar fuera de estos intervalos.

En el caso de los datos de entrada con el formato de vídeo RGB de Studio, la operación de recorte es necesaria para mantener los valores de ti y V en el intervalo de 0 a (2 ^ M)-1. Si la entrada es RGB de equipo, la operación de recorte no es necesaria, porque la fórmula de conversión no puede producir valores fuera de este intervalo.

Estas son las fórmulas exactas sin aproximación. Todo lo que se muestra a continuación en este documento se deriva de estas fórmulas. En esta sección se describen las conversiones siguientes:

-   [Convertir RGB888 a YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Conversión de YUV de 8 bits a RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Conversión de 4:2:0 YUV a 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Conversión de 4:2:2 YUV a 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Conversión de 4:2:0 YUV a 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Convertir RGB888 a YUV 4:4:4

En el caso de la entrada RGB de equipo y la salida de 8 bits BT. 601, creemos que las fórmulas proporcionadas en la sección anterior se pueden aproximar razonablemente según lo siguiente:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Estas fórmulas producen resultados de 8 bits mediante coeficientes que no requieren más de 8 bits de precisión (sin signo). Los resultados intermedios requerirán hasta 16 bits de precisión.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Conversión de YUV de 8 bits a RGB888

En las fórmulas de RGB a YUV originales, una puede derivar las siguientes relaciones para BT. 601.

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

Por lo tanto, dado:

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

las fórmulas para convertir YUV en RGB pueden derivarse de la siguiente manera:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

donde `clip()` denota el recorte en un intervalo de \[ 0.. 255 \] . Creemos que estas fórmulas se pueden aproximar razonablemente según lo siguiente:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Estas fórmulas usan algunos coeficientes que requieren más de 8 bits de precisión para generar cada resultado de 8 bits, y los resultados intermedios requerirán más de 16 bits de precisión.

Para convertir 4:2:0 o 4:2:2 YUV en RGB, se recomienda convertir los datos de YUV en 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB. En las secciones siguientes se presentan algunos métodos para convertir los formatos 4:2:0 y 4:2:2 a 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Conversión de 4:2:0 YUV a 4:2:2 YUV

La conversión de 4:2:0 YUV a 4:2:2 YUV requiere una conversión vertical en un factor de dos. En esta sección se describe un método de ejemplo para realizar la conversión. El método supone que las imágenes de vídeo son análisis progresivo.

> [!Note]  
> El proceso de conversión de análisis entrelazado 4:2:0 a 4:2:2 presenta problemas atípicos y es difícil de implementar. En este artículo no se aborda el problema de convertir el análisis entrelazado de 4:2:0 a 4:2:2.

 

Permita que cada línea vertical de muestras de croma de entrada sea una matriz `Cin[]` que va de 0 a N-1. La línea vertical correspondiente en la imagen de salida será una matriz `Cout[]` que va de 0 a 2N-1. Para convertir cada línea vertical, realice el proceso siguiente:

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

donde clip () denota el recorte en un intervalo de \[ 0.. 255 \] .

> [!Note]  
> Las ecuaciones para controlar los bordes se pueden simplificar matemáticamente. Se muestran en este formulario para mostrar el efecto de compresión en los bordes de la imagen.

 

En efecto, este método calcula cada valor que falta mediante la interpolación de la curva en los cuatro píxeles adyacentes, ponderada hacia los valores de los dos píxeles más cercanos (Figura 11). El método de interpolación específico que se usa en este ejemplo genera muestras que faltan en posiciones de medio entero mediante un método conocido denominado Catmull-Rom interpolación, también conocido como interpolación de circunvolución cúbica.

![Figura 11. diagrama que muestra el muestreo de 4:2:0 a 4:2:2](images/yuvformats14.gif)

En términos de procesamiento de señal, la conversión vertical debería incluir, idealmente, una compensación de desplazamiento de fase para tener en cuenta el desplazamiento vertical de medio píxel (con respecto a la cuadrícula de muestreo 4:2:2 de salida) entre las ubicaciones de las líneas de ejemplo 4:2:0 y la ubicación de cada otra línea de ejemplo 4:2:2. Sin embargo, si se introduce este desplazamiento, se aumentaría la cantidad de procesamiento necesaria para generar los ejemplos y se impedirá la reconstrucción de los ejemplos originales de 4:2:0 a partir de la imagen de 4:2:2 de ejemplo. También haría imposible descodificar el vídeo directamente en las superficies 4:2:2 y, a continuación, usar esas superficies como imágenes de referencia para descodificar imágenes posteriores en la secuencia. Por lo tanto, el método que se proporciona aquí no tiene en cuenta la alineación vertical precisa de los ejemplos. Hacer esto probablemente no es perjudicial visualmente en resoluciones de imagen razonablemente altas.

Si comienza con un vídeo de 4:2:0 que usa la cuadrícula de muestreo definida en el vídeo H. 261, H. 263 o MPEG-1, la fase de las muestras de croma 4:2:2 de salida también se desplazará con un desplazamiento horizontal de medio píxel en relación con el espaciado de la cuadrícula de muestreo de luminancia (un desplazamiento de cuarto de píxeles en relación con el espaciado de 4:2:2 la cuadrícula Sin embargo, el formato MPEG-2 del vídeo 4:2:0 probablemente se usa con más frecuencia en los equipos y no se ve afectado por este problema. Además, es probable que la distinción no sea visualmente dañina en resoluciones de imagen razonablemente altas. Si intenta corregir este problema, se creará el mismo tipo de problemas descritos para el desplazamiento de fase vertical.

## <a name="converting-422-yuv-to-444-yuv"></a>Conversión de 4:2:2 YUV a 4:4:4 YUV

La conversión de 4:2:2 YUV a 4:4:4 YUV requiere una conversión horizontal en un factor de dos. El método descrito anteriormente para la conversión vertical se puede aplicar también a la conversión horizontal. Para vídeo MPEG-2 e ITU-R BT. 601, este método generará ejemplos con la alineación de fase correcta.

## <a name="converting-420-yuv-to-444-yuv"></a>Conversión de 4:2:0 YUV a 4:4:4 YUV

Para convertir 4:2:0 YUV en 4:4:4 YUV, puede seguir simplemente los dos métodos descritos anteriormente. Convierta la imagen 4:2:0 a 4:2:2 y, a continuación, convierta la imagen 4:2:2 a 4:4:4. También puede cambiar el orden de los dos procesos de conversión, ya que el orden de operación no importa realmente la calidad visual del resultado.

## <a name="other-yuv-formats"></a>Otros formatos YUV

Otros formatos YUV menos comunes son los siguientes:

-   AI44 es un formato YUV de paleta con 8 bits por muestra. Cada ejemplo contiene un índice en los 4 bits más significativos (MSBs) y un valor alfa en 4 bits menos significativos (LSBs). El índice hace referencia a una matriz de entradas de la paleta YUV, que debe definirse en el tipo de medio para el formato. Este formato se usa principalmente para imágenes de subimagen.
-   NV11 es un formato plano 4:1:1 con 12 bits por píxel. Los ejemplos Y aparecen en primer lugar en la memoria. El plano Y va seguido de una matriz de ejemplos empaquetados de U (CB) y V (CR). Cuando la matriz de U-V combinada se dirige como una matriz de valores de **palabra** Little-endian, los ejemplos de u se incluyen en el LSBs de cada **palabra** y los ejemplos de V se incluyen en el MSBs. (Este diseño de memoria es similar a NV12, aunque el muestreo de croma es diferente).
-   Y41P es un formato empaquetado de 4:1:1, con el usuario y V muestreados horizontalmente cada cuatro píxeles. Cada macropixel contiene 8 píxeles en tres bytes, con el siguiente diseño de bytes: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T es idéntico a Y41P, excepto el bit menos significativo de cada ejemplo Y especifica la clave de croma (0 = transparente, 1 = opaca).
-   Y42T es idéntico a UYVY, excepto el bit menos significativo de cada ejemplo Y especifica la clave de croma (0 = transparente, 1 = opaca).
-   YVYU es equivalente a YUYV, excepto en que se intercambian los ejemplos de los que usted y V.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identificar formatos YUV en Media Foundation

Cada uno de los formatos YUV descritos en este artículo tiene un código FOURCC asignado. Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.

Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente. Por ejemplo, la macro **MAKEFOURCC** se declara en mmsystem. h y la macro **FCC** se declara en Aviriff. h. Úselos de la siguiente manera:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres. Por ejemplo:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

Invertir el orden es necesario porque el sistema operativo Windows utiliza una arquitectura little-endian. ' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559.

En Media Foundation, los formatos se identifican mediante un GUID de tipo principal y un GUID de subtipo. El tipo principal de los formatos de vídeo del equipo es siempre MFMediaType \_ video. El subtipo se puede construir asignando el código FOURCC a un GUID, como se indica a continuación:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

donde `XXXXXXXX` es el código FourCC. Por lo tanto, el GUID del subtipo para YUY2 es:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Las constantes de los GUID de formato YUV más comunes se definen en el archivo de encabezado mfapi. h. Para obtener una lista de estas constantes, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del vídeo YUV](about-yuv-video.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



