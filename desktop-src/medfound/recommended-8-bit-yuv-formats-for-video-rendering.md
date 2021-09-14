---
description: Formatos YUV de 8 bits recomendados para la representación en vídeo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formatos YUV de 8 bits recomendados para la representación en vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268759"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a>Formatos YUV de 8 bits recomendados para la representación en vídeo

SteveRta y Stephen Estrop

Microsoft Corporation

Abril de 2002, actualizado en noviembre de 2008

En este tema se describen los formatos de color YUV de 8 bits que se recomiendan para la representación de vídeo en el Windows operativo. En este artículo se presentan técnicas para convertir entre formatos YUV y RGB, y también se proporcionan técnicas para mejorar elmuestreo de los formatos YUV. Este artículo está pensado para cualquier persona que trabaje con la decodificación o representación de vídeo de YUV en Windows.

## <a name="introduction"></a>Introducción

Se definen numerosos formatos YUV en todo el sector del vídeo. En este artículo se identifican los formatos YUV de 8 bits que se recomiendan para la representación de vídeo en Windows. Se recomienda a los proveedores de descodificadores y proveedores de pantalla que admitan los formatos descritos en este artículo. En este artículo no se abordan otros usos del color YUV, como la fotografía.

Los formatos descritos en este artículo usan 8 bits por ubicación de píxel para codificar el canal Y (también denominado canal luma) y usan 8 bits por muestra para codificar cada ejemplo de muestreo de U o V. Sin embargo, la mayoría de los formatos YUV usan menos de 24 bits por píxel de media, ya que contienen menos muestras de usted y V que de Y. En este artículo no se cubren los formatos YUV con canales Y de 10 bits o superiores.

> [!Note]  
> Para los fines de este artículo, el término U es equivalente a Cb y el término V es equivalente a Cr.

 

En este artículo se tratan los temas siguientes:

-   [Muestreo de YUV](#yuv-sampling). Describe las técnicas de muestreo de YUV más comunes.
-   [Definiciones de surface](#surface-definitions). Describe los formatos YUV recomendados.
-   [Conversiones de espacio de color y frecuencia de muestreo](#color-space-and-chroma-sampling-rate-conversions). Proporciona algunas directrices para convertir entre formatos YUV y RGB y para convertir entre diferentes formatos YUV.
-   [Identificar formatos YUV en Media Foundation](#identifying-yuv-formats-in-media-foundation). Explica cómo describir los tipos de formato YUV en Media Foundation.

## <a name="yuv-sampling"></a>Muestreo de YUV

Los canales de canalización pueden tener una frecuencia de muestreo menor que el canal luma, sin ninguna pérdida drástica de calidad perceptual. Se usa una notación denominada "A:B:C" para describir la frecuencia con la que se muestrean usted y V con respecto a Y:

-   4:4:4 significa que no hay ninguna disminución de los canales de los canales de los canales.
-   4:2:2 significa una disminución horizontal de 2:1, sin un bajomuestreo vertical. Cada línea de examen contiene cuatro muestras Y por cada dos muestras de U o V.
-   4:2:0 significa una disminución horizontal de 2:1, con un amuestreo vertical de 2:1.
-   4:1:1 significa una disminución horizontal de 4:1, sin un bajomuestreo vertical. Cada línea de examen contiene cuatro muestras Y para cada muestra de V y usted. El muestreo 4:1:1 es menos común que otros formatos y no se describe en detalle en este artículo.

En los diagramas siguientes se muestra cómo se muestrea el muestreo de cada una de las tasas de desmuestreo. Las muestras de Luma se representan mediante una cruzada y las muestras de muestras se representan mediante un círculo.

![Figura 1. muestreo de muestreo de muestreo](images/yuv-sampling-grids.png)

La forma dominante del muestreo 4:2:2 se define en la recomendación BT.601 de ITU-R. Hay dos variantes comunes de muestreo 4:2:0. Una de ellas se usa en vídeo MPEG-2 y la otra en MPEG-1 y en ITU-T Recomendaciones H.261 y H.263.

En comparación con el esquema MPEG-1, es más sencillo convertir entre el esquema MPEG-2 y las cuadrículas de muestreo definidas para los formatos 4:2:2 y 4:4:4. Por este motivo, se prefiere el esquema MPEG-2 en Windows y se debe considerar la interpretación predeterminada de los formatos 4:2:0.

## <a name="surface-definitions"></a>Definiciones de surface

En esta sección se describen los formatos YUV de 8 bits que se recomiendan para la representación de vídeo. Se divide en varias categorías:

-   [Formatos 4:4:4, 32 bits por píxel](#444-formats-32-bits-per-pixel)
-   [Formatos 4:2:2, 16 bits por píxel](#422-formats-16-bits-per-pixel)
-   [Formatos 4:2:0, 16 bits por píxel](#420-formats-16-bits-per-pixel)
-   [Formatos 4:2:0, 12 bits por píxel](#420-formats-12-bits-per-pixel)

En primer lugar, debe tener en cuenta los siguientes conceptos para comprender lo que sigue:

-   *Origen de la superficie.* Para los formatos YUV descritos en este artículo, el origen (0,0) siempre es la esquina superior izquierda de la superficie.
-   *Stride*. El paso de una superficie, a veces denominado paso, es el ancho de la superficie en bytes. Dado un origen de superficie en la esquina superior izquierda, el paso siempre es positivo.
-   *Alineación* de . La alineación de una superficie está a discreción del controlador de pantalla de gráficos. La superficie siempre debe estar alineada con DWORD; Es decir, se garantiza que las líneas individuales dentro de la superficie se originan en un límite de 32 bits (DWORD). Sin embargo, la alineación puede ser superior a 32 bits, dependiendo de las necesidades del hardware.
-   Formato empaquetado frente al formato plano. Los formatos YUV se dividen *en formatos empaquetados* y *formatos planas.* En un formato empaquetado, los componentes Y, U y V se almacenan en una sola matriz. Los píxeles se organizan en grupos de macropíxeles, cuyo diseño depende del formato. En un formato plano, los componentes Y, U y V se almacenan como tres planos independientes.

Cada uno de los formatos YUV descritos en este artículo tiene asignado un código FOURCC. Un código FOURCC es un entero de 32 bits sin signo que se crea concatenando cuatro caracteres ASCII.

-   4:4:4 (32 bpp)
    -   [AYUV](#ayuv)
-   4:2:2 (16 bpp)
    -   [YUY2](#yuy2)
    -   [UYVY](#uyvy)
-   4:2:0 (16 bpp)
    -   [IMC1](#imc1)
    -   [IMC3](#imc3)
-   4:2:0 (12 bpp)
    -   [IMC2](#imc2)
    -   [IMC4](#imc4)
    -   [YV12](#yv12)
    -   [NV12](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a>Formatos 4:4:4, 32 bits por píxel

### <a name="ayuv"></a>AYUV

Se recomienda un único formato 4:4:4, con el código FOURCC AYUV. Se trata de un formato empaquetado, donde cada píxel se codifica como cuatro bytes consecutivos, organizados en la secuencia que se muestra en la ilustración siguiente.

![Figura 2. Diseño de memoria de ayuv](images/yuvformats01.gif)

Los bytes marcados como A contienen valores para alfa.

## <a name="422-formats-16-bits-per-pixel"></a>Formatos 4:2:2, 16 bits por píxel

Se recomiendan dos formatos 4:2:2, con los siguientes códigos FOURCC:

-   YUY2
-   UYVY

Ambos son formatos empaquetados, donde cada macropixel tiene dos píxeles codificados como cuatro bytes consecutivos. Esto da como resultado una disminución horizontal del mosaico por un factor de dos.

### <a name="yuy2"></a>YUY2

En formato YUY2, los datos se pueden tratar como una matriz de valores **char** sin signo, donde el primer byte contiene la primera muestra Y, el segundo byte contiene la primera muestra U (Cb), el tercer byte contiene la segunda muestra Y y el cuarto byte contiene la primera muestra V (Cr), como se muestra en el diagrama siguiente.

![Figura 3. diseño de memoria yuy2](images/yuvformats02.gif)

Si la imagen se trata como una matriz de valores **word** little-endian, la primera **palabra** contiene la primera muestra Y en los bits menos significativos (LSB) y la primera muestra U (Cb) en los bits más significativos (MSB). La segunda **palabra** contiene el segundo ejemplo Y en los LSB y el primer ejemplo de V (Cr) en las MSB.

YUY2 es el formato preferido de 4:2:2 píxeles para la aceleración de vídeo de Microsoft DirectX (DirectX VA). Se espera que sea un requisito de término intermedio para los aceleradores de Va de DirectX que admiten vídeo 4:2:2.

### <a name="uyvy"></a>UYVY

Este formato es el mismo que el formato YUY2, excepto que se invierte el orden de bytes, es decir, se voltearán los bytes de color tordo y luma (figura 4). Si la imagen se dirige como una  matriz de dos valores word little-endian, la primera **palabra** contiene U en los LSB y Y0 en los MSB, y la segunda **palabra** contiene V en los LSB e Y1 en los MSB.

![Figura 4. Diseño de memoria uyvy](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a>Formatos 4:2:0, 16 bits por píxel

Se recomiendan dos formatos de 4:2:0 de 16 bits por píxel (bpp), con los siguientes códigos FOURCC:

-   IMC1
-   IMC3

Ambos formatos YUV son formatos planas. Los canales de mosaico se submuestrean por un factor de dos en las dimensiones horizontal y vertical.

### <a name="imc1"></a>IMC1

Todos los ejemplos de Y aparecen primero en memoria como una matriz de valores **char sin** signo. Esto va seguido de todos los ejemplos de V (Cr) y, a continuación, de todos los ejemplos de U (Cb). Los planos V y U tienen el mismo paso que el plano Y, lo que da lugar a áreas de memoria no utilizadas, como se muestra en la figura 5. Los planos you y V deben comenzar en límites de memoria que son un múltiplo de 16 líneas. En la figura 5 se muestra el origen de usted y V para un fotograma de vídeo de 352 x 240. La dirección inicial de los planos usted y V se calcula de la siguiente manera:

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

donde *pY* es un puntero de byte al inicio de la matriz de memoria, como se muestra en el diagrama siguiente.

![Figura 5. Diseño de memoria imc1 (ejemplo)](images/yuvformats04.gif)

### <a name="imc3"></a>IMC3

Este formato es idéntico a IMC1, excepto que los planos usted y V se intercambian, como se muestra en el diagrama siguiente.

![Figura 6. Diseño de memoria de imc3](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a>Formatos 4:2:0, 12 bits por píxel

Se recomiendan cuatro formatos 4:2:0 de 12 bpp, con los siguientes códigos FOURCC:

-   IMC2
-   IMC4
-   YV12
-   NV12

En todos estos formatos, los canales de canalón se submuestrean por un factor de dos en las dimensiones horizontal y vertical.

### <a name="imc2"></a>IMC2

Este formato es el mismo que el de IMC1, salvo por la siguiente diferencia: las líneas V (Cr) y U (Cb) se intercalan en límites de medio paso. En otras palabras, cada línea de paso completo en el área de la zona de la zona de muestreo comienza con una línea de muestras de V, seguida de una línea de muestras de U que comienza en el siguiente límite de medio paso (figura 7). Este diseño hace un uso más eficaz del espacio de direcciones que IMC1. Reduce el espacio de direcciones de la barra espaciadora a la mitad y, por tanto, el espacio total de direcciones en un 25 %. Entre los formatos 4:2:0, IMC2 es el segundo formato preferido, después de NV12. En la imagen siguiente se muestra este proceso.

![Figura 7. Diseño de memoria de imc2](images/yuvformats07.gif)

### <a name="imc4"></a>IMC4

Este formato es idéntico a IMC2, excepto que se intercambian las líneas U (Cb) y V (Cr), como se muestra en la ilustración siguiente.

![Figura 8. Diseño de memoria imc4](images/yuvformats06.gif)

### <a name="yv12"></a>YV12

Todos los ejemplos de Y aparecen primero en memoria como una matriz de valores **char sin** signo. Esta matriz va seguida inmediatamente de todos los ejemplos de V (Cr). El paso del plano V es la mitad del paso del plano Y; y el plano V contiene la mitad de líneas que el plano Y. El plano V va seguido inmediatamente de todos los ejemplos de U (Cb), con el mismo paso y número de líneas que el plano V, como se muestra en la ilustración siguiente.

![Figura 9. Diseño de memoria yv12](images/yuvformats08.gif)

### <a name="nv12"></a>NV12

Todos los ejemplos de Y aparecen primero en memoria como una matriz de valores **char** sin signo con un número par de líneas. El plano Y va seguido inmediatamente de una matriz de valores **char** sin signo que contiene ejemplos empaquetados de U (Cb) y V (Cr). Cuando la matriz de U-V combinada se dirige como una matriz de valores **word** little-endian, los LSB contienen los valores U y los MSB contienen los valores V. NV12 es el formato preferido de 4:2:0 píxeles para DirectX VA. Se espera que sea un requisito de término intermedio para los aceleradores de Va de DirectX que admiten vídeo 4:2:0. En la ilustración siguiente se muestra el plano Y y la matriz que contiene ejemplos empaquetados de you y V.

![Figura 10. Diseño de memoria nv12](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a>Conversiones de espacio de color y frecuencia de muestreo

En esta sección se proporcionan instrucciones para convertir entre YUV y RGB, y para convertir entre algunos formatos YUV diferentes. En esta sección se tienen en cuenta dos esquemas de codificación *RGB: RGB* de equipo de 8 bits, también conocido como sRGB o RGB de "escala completa", y vídeo de estudio *RGB,* o "RGB con sala de cabeza y de toe-room". Se definen de la siguiente manera:

-   El equipo RGB usa 8 bits para cada muestra de rojo, verde y azul. El negro se representa mediante R = G = B = 0, y el blanco se representa mediante R = G = B = 255.
-   El vídeo RGB de Studio usa un número de bits N para cada muestra de rojo, verde y azul, donde N es 8 o más. El vídeo RGB de Studio usa un factor de escalado diferente al RGB del equipo y tiene un desplazamiento. El negro se representa mediante R = G = B = 16 2^(N-8) y el blanco se representa mediante \* R = G = B = 235 \* 2^(N-8). Sin embargo, los valores reales pueden estar fuera de este intervalo.

Vídeo de Studio RGB es la definición RGB preferida para vídeo en Windows, mientras que RGB de equipo es la definición RGB preferida para aplicaciones que no son de vídeo. En cualquier forma de RGB, las coordenadas de colorticidad son las especificadas en ITU-R BT.709 para la definición de las primarias de color RGB. Las coordenadas (x,y) de R, G y B son (0,64, 0,33), (0,30, 0,60) y (0,15, 0,06), respectivamente. El blanco de referencia es D65 con coordenadas (0,3127, 0,3290). Gamma nominal es 1/0,45 (aproximadamente 2,2), con gamma preciso definido en detalle en ITU-R BT.709.

**Conversión entre RGB y 4:4:4 YUV**

Primero se describe la conversión entre RGB y 4:4:4 YUV. Para convertir 4:2:0 o 4:2:2 YUV en RGB, se recomienda convertir los datos de YUV a 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB. El formato AYUV, que es un formato 4:4:4, usa 8 bits cada uno para los ejemplos Y, U y V. YUV también se puede definir con más de 8 bits por ejemplo para algunas aplicaciones.

Se han definido dos conversiones YUV dominantes de RGB para vídeo digital. Ambos se basan en la especificación conocida como recomendación DE ITU-R BT.709. La primera conversión es el formulario YUV anterior definido para el uso de 50 Hz en BT.709. Es la misma relación especificada en la recomendación BT.601 de ITU-R, también conocida por su nombre anterior, CCIR 601. Debe considerarse el formato YUV preferido para la resolución de televisión de definición estándar (720 x 576) y el vídeo de resolución inferior. Se caracteriza por los valores de dos constantes *Kr* y *Kb*:

``` syntax
Kr = 0.299
Kb = 0.114
```

La segunda conversión es el formato YUV más reciente definido para el uso de 60 Hz en BT.709 y debe considerarse el formato preferido para las resoluciones de vídeo anteriores a SDTV. Se caracteriza por valores diferentes para estas dos constantes:

``` syntax
Kr = 0.2126
Kb = 0.0722
```

La conversión de RGB a YUV se define a partir de lo siguiente:

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

A continuación, los valores de YUV se obtienen de la siguiente manera:

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

, donde

-   M es el número de bits por ejemplo YUV (M >= 8).
-   Z es la variable de nivel negro. Para el equipo RGB, Z es igual a 0. Para vídeo de estudio RGB, Z es igual a 16 2^(N-8), donde N es el número de bits por muestra \* RGB (N >= 8).
-   S es la variable de escalado. Para el equipo RGB, S es igual a 255. Para vídeo de estudio RGB, S es igual a 219 \* 2^(N-8).

La función floor(x) devuelve el entero más grande menor o igual que x. La función clip3(x, y, z) se define de la siguiente manera:

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> clip3 debe implementarse como una función en lugar de como una macro de preprocesador. De lo contrario, se producirán varias evaluaciones de los argumentos.

 

El ejemplo Y representa el brillo, y las muestras usted y V representan las desviaciones de color hacia el azul y el rojo, respectivamente. El intervalo nominal de Y es de 16 \* 2^(M-8) a 235 \* 2^(M-8). El negro se representa como 16 \* 2^(M-8) y el blanco como 235 \* 2^(M-8). El intervalo nominal para usted y V es de 16 \* 2^(M-8) a 240 \* 2^(M-8), con el valor 128 \* 2^(M-8) que representa el efecto neutro. Sin embargo, los valores reales pueden estar fuera de estos intervalos.

Para los datos de entrada en forma rgb de vídeo de Studio, la operación de recorte es necesaria para mantener los valores de usted y V dentro del intervalo de 0 a (2^M)-1. Si la entrada es RGB del equipo, la operación de recorte no es necesaria, ya que la fórmula de conversión no puede generar valores fuera de este intervalo.

Estas son las fórmulas exactas sin aproximación. Todo lo que sigue en este documento se deriva de estas fórmulas. En esta sección se describen las conversiones siguientes:

-   [Convertir RGB888 a YUV 4:4:4](#converting-rgb888-to-yuv-444)
-   [Conversión de YUV de 8 bits a RGB888](#converting-8-bit-yuv-to-rgb888)
-   [Convertir 4:2:0 YUV en 4:2:2 YUV](#converting-420-yuv-to-422-yuv)
-   [Convertir 4:2:2 YUV en 4:4:4 YUV](#converting-422-yuv-to-444-yuv)
-   [Convertir 4:2:0 YUV en 4:4:4 YUV](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a>Convertir RGB888 a YUV 4:4:4

En el caso de la entrada RGB del equipo y la salida de BT.601 YUV de 8 bits, creemos que las fórmulas dadas en la sección anterior pueden ser razonablemente aproximadas por lo siguiente:

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

Estas fórmulas generan resultados de 8 bits mediante coeficientes que no requieren más de 8 bits de precisión (sin signo). Los resultados intermedios requerirán hasta 16 bits de precisión.

## <a name="converting-8-bit-yuv-to-rgb888"></a>Conversión de YUV de 8 bits a RGB888

A partir de las fórmulas RGB a YUV originales, se pueden derivar las relaciones siguientes para BT.601.

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

Las fórmulas para convertir YUV a RGB se pueden derivar de la siguiente manera:

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

donde `clip()` denota el recorte a un intervalo de \[ 0,.255 \] . Creemos que estas fórmulas se pueden aproximar razonablemente a lo siguiente:

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

Estas fórmulas usan algunos coeficientes que requieren más de 8 bits de precisión para generar cada resultado de 8 bits, y los resultados intermedios requerirán más de 16 bits de precisión.

Para convertir 4:2:0 o 4:2:2 YUV a RGB, se recomienda convertir los datos de YUV a 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB. Las secciones siguientes presentan algunos métodos para convertir los formatos 4:2:0 y 4:2:2 a 4:4:4.

## <a name="converting-420-yuv-to-422-yuv"></a>Convertir 4:2:0 YUV en 4:2:2 YUV

La conversión de 4:2:0 YUV a 4:2:2 YUV requiere una conversión vertical por un factor de dos. En esta sección se describe un método de ejemplo para realizar la inversión. El método supone que las imágenes de vídeo son de examen progresiva.

> [!Note]  
> El proceso de conversión de examen entrelazado de 4:2:0 a 4:2:2 presenta problemas atípicos y es difícil de implementar. En este artículo no se aborda el problema de convertir el examen entrelazado de 4:2:0 a 4:2:2.

 

Permita que cada línea vertical de muestras de muestreo de entrada sea una matriz `Cin[]` que va de 0 a N- 1. La línea vertical correspondiente en la imagen de salida será una matriz que va de 0 a `Cout[]` 2N- 1. Para convertir cada línea vertical, realice el siguiente proceso:

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

donde clip() denota el recorte a un intervalo de \[ 0,255 \] .

> [!Note]  
> Las ecuaciones para controlar los bordes se pueden simplificar matemáticamente. Se muestran en este formato para ilustrar el efecto de fijación en los bordes de la imagen.

 

En efecto, este método calcula cada valor que falta interpolando la curva sobre los cuatro píxeles adyacentes, ponderada hacia los valores de los dos píxeles más cercanos (Figura 11). El método de interpolación específico usado en este ejemplo genera muestras que faltan en posiciones de medio entero mediante un método conocido denominado interpolación Catmull-Rom, también conocido como interpolación de convolución cúbica.

![figura 11. diagrama que muestra el muestreo de 4:2:0 a 4:2:2](images/yuvformats14.gif)

En términos de procesamiento de señales, lo ideal es que la inversión vertical incluya una compensación de desplazamiento de fase para tener en cuenta el desplazamiento vertical de medio píxel (en relación con la cuadrícula de muestreo de salida 4:2:2) entre las ubicaciones de las líneas de muestra 4:2:0 y la ubicación de cada otra línea de muestra de 4:2:2. Sin embargo, introducir este desplazamiento aumentaría la cantidad de procesamiento necesario para generar las muestras y haría imposible reconstruir las muestras originales de 4:2:0 a partir de la imagen upsampled 4:2:2. También haría imposible descodificar vídeo directamente en superficies 4:2:2 y, a continuación, usar esas superficies como imágenes de referencia para descodificar imágenes posteriores en la secuencia. Por lo tanto, el método proporcionado aquí no tiene en cuenta la alineación vertical precisa de las muestras. Es probable que hacerlo no sea visualmente perjudicial a resoluciones de imagen razonablemente altas.

Si empieza con un vídeo de 4:2:0 que usa la cuadrícula de muestreo definida en vídeo H.261, H.263 o MPEG-1, la fase de las muestras de muestreo de salida 4:2:2 también se desplazará mediante un desplazamiento horizontal de medio píxel en relación con el espaciado en la cuadrícula de muestreo de luma (un desplazamiento de cuarto de píxel en relación con el espaciado de la cuadrícula de muestreo de muestreo de 4:2:2). Sin embargo, la forma MPEG-2 del vídeo 4:2:0 probablemente se usa con más frecuencia en equipos y no sufre este problema. Además, es probable que la distinción no sea visualmente dañina a resoluciones de imagen razonablemente altas. Si se intenta corregir este problema, se crearía el mismo tipo de problemas que se analizan para el desplazamiento de fase vertical.

## <a name="converting-422-yuv-to-444-yuv"></a>Convertir 4:2:2 YUV en 4:4:4 YUV

La conversión de 4:2:2 YUV a 4:4:4 YUV requiere una conversión horizontal por un factor de dos. El método descrito anteriormente para upconversion vertical también se puede aplicar a la upconversion horizontal. Para el vídeo MPEG-2 e ITU-R BT.601, este método producirá ejemplos con la alineación de fase correcta.

## <a name="converting-420-yuv-to-444-yuv"></a>Convertir 4:2:0 YUV en 4:4:4 YUV

Para convertir 4:2:0 YUV a 4:4:4 YUV, simplemente puede seguir los dos métodos descritos anteriormente. Convierta la imagen 4:2:0 en 4:2:2 y, a continuación, convierta la imagen 4:2:2 en 4:4:4. También puede cambiar el orden de los dos procesos de upconversion, ya que el orden de operación no importa realmente para la calidad visual del resultado.

## <a name="other-yuv-formats"></a>Otros formatos YUV

Algunos otros formatos YUV menos comunes incluyen los siguientes:

-   AI44 es un formato YUV tachado con 8 bits por muestra. Cada muestra contiene un índice en los 4 bits más significativos (MSB) y un valor alfa en los 4 bits menos significativos (LSB). El índice hace referencia a una matriz de entradas de la paleta YUV, que se deben definir en el tipo de medio para el formato. Este formato se usa principalmente para las imágenes de subimagen.
-   NV11 es un formato planar de 4:1:1 con 12 bits por píxel. Los ejemplos Y aparecen primero en la memoria. El plano Y va seguido de una matriz de ejemplos empaquetados de U (Cb) y V (Cr). Cuando la matriz de U-V combinada se trata como una matriz de valores **word** little-endian, las muestras de U se encuentran en los LSB de cada **WORD** y las muestras de V se incluyen en las MSB. (Este diseño de memoria es similar a NV12, aunque el muestreo de muestreo es diferente).
-   Y41P es un formato empaquetado de 4:1:1, con usted y V muestreados cada cuarto píxel horizontalmente. Cada macropixel contiene 8 píxeles en tres bytes, con el siguiente diseño de bytes: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`
-   Y41T es idéntico a Y41P, salvo que el bit menos significativo de cada muestra Y especifica la clave de la llave de la llave (0 = transparente, 1 = opaca).
-   Y42T es idéntico a UYVY, salvo que el bit menos significativo de cada muestra Y especifica la clave de la y (0 = transparente, 1 = opaca).
-   YVYU es equivalente a YUYV, salvo que se intercambian los ejemplos de usted y V.

## <a name="identifying-yuv-formats-in-media-foundation"></a>Identificación de formatos YUV en Media Foundation

Cada uno de los formatos YUV descritos en este artículo tiene asignado un código FOURCC. Un código FOURCC es un entero de 32 bits sin signo que se crea concatenando cuatro caracteres ASCII.

Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente. Por ejemplo, la macro **MAKEFOURCC** se declara en Mmsystem.h y la macro **FCC** se declara en Aviriff.h. Úsenlos como se muestra a continuación:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres. Por ejemplo:

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

Es necesario invertir el orden porque el Windows operativo usa una arquitectura little-endian. 'Y' = 0x59, 'U' = 0x55 y '2' = 0x32, por lo que '2YUY' es 0x32595559.

En Media Foundation, los formatos se identifican mediante un GUID de tipo principal y un GUID de subtipo. El tipo principal para los formatos de vídeo de equipo es siempre MFMediaType \_ Video . El subtipo se puede construir asignando el código FOURCC a un GUID, como se muestra a continuación:

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

donde `XXXXXXXX` es el código FOURCC. Por lo tanto, el GUID del subtipo para YUY2 es:

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

Las constantes para los GUID de formato YUV más comunes se definen en el archivo de encabezado mfapi.h. Para obtener una lista de estas constantes, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del vídeo de YUV](about-yuv-video.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> </dl>

 

 



