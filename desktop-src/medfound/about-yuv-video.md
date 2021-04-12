---
description: Acerca del vídeo YUV
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Acerca del vídeo YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b57b4a453870af34c221683bdaf613b5038081d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541374"
---
# <a name="about-yuv-video"></a>Acerca del vídeo YUV

El vídeo digital suele estar codificado en formato *YUV* . En este artículo se explican los conceptos generales del vídeo YUV, junto con cierta terminología, sin profundizar en las matemáticas del procesamiento de vídeo YUV.

Si ha trabajado con gráficos informáticos, probablemente esté familiarizado con el color RGB. Un color RGB se codifica con tres valores: rojo, verde y azul. Estos valores corresponden directamente a partes del espectro visible. Los tres valores RGB forman un sistema de coordenadas matemático, denominado *espacio de colores*. El componente rojo define un eje de este sistema de coordenadas, el azul define el segundo y el verde define el tercero, tal y como se muestra en la siguiente ilustración. Cualquier color RGB válido se encuentra en algún lugar de este espacio de colores. Por ejemplo, el magenta puro es 100% azul, 100% rojo y 0% verde.

![diagrama que muestra el espacio de colores RGB](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Aunque RGB es una forma común de representar colores, son posibles otros sistemas de coordenadas. El término *YUV* hace referencia a una familia de espacios de colores que codifican la información de brillo por separado de la información de color. Como RGB, YUV usa tres valores para representar cualquier color. Estos valores se denominan Y ', U y V. (de hecho, este uso del término "YUV" es técnicamente inexacto. En el vídeo del equipo, el término YUV casi siempre hace referencia a un espacio de colores determinado denominado Y'CbCr, que se describe más adelante. Sin embargo, se suele usar YUV como término general para cualquier espacio de colores que funcione en los mismos principios que Y'CbCr).

El componente Y ', también denominado *luminancia*, representa el valor de luminosidad del color. El símbolo primo (') se usa para diferenciar la luminancia de un valor estrechamente relacionado, *luminancia*, que se designa como Y. la luminancia se deriva de los valores RGB *lineales* , mientras que la luminancia se deriva de valores RGB *no lineales* (corregidos con gamma). La luminancia es una medida más cercana del verdadero brillo, pero la luminancia es más práctica de utilizar por motivos técnicos. El símbolo primo se suele omitir, pero los espacios de colores YUV siempre usan luminancia, no luminancia.

La luminancia se deriva de un color RGB tomando una media ponderada de los componentes rojo, verde y azul. Para el televisor de definición estándar, se usa la fórmula siguiente:

`Y' = 0.299R + 0.587G + 0.114B`

Esta fórmula refleja el hecho de que el ojo humano es más sensible a ciertas longitudes de onda de luz que a otras, lo que afecta al brillo percibido de un color. La luz azul aparece atenuada, el color verde es el más brillante y el rojo está en alguna parte. Esta fórmula también refleja las características físicas de los fósforos que se usan en los televisores iniciales. Una fórmula más reciente, teniendo en cuenta la tecnología de televisión moderna, se usa para el televisor de alta definición:

`Y' = 0.2125R + 0.7154G + 0.0721B`

La ecuación de luminancia para el televisor de definición estándar se define en una especificación denominada ITU-R BT. 601. En el caso de televisión de alta definición, la especificación relevante es ITU-R BT. 709.

Los componentes usted y V, también denominados valores de *croma* o valores de *diferencia de color* , se derivan restando el valor Y de los componentes rojo y azul del color RGB original:

`U = B - Y'`

`V = R - Y'`

Juntos, estos valores contienen información suficiente para recuperar el valor RGB original.

## <a name="benefits-of-yuv"></a>Ventajas de YUV

El televisor analógico usa YUV en parte para los motivos históricos. Las señales de televisión en color analógico se diseñaron para ser compatibles con la compatibilidad con televisores en blanco y negro. La señal de televisión en color lleva la información de croma (usted y V) superpuesta a la señal de luminancia. Los televisores en blanco y negro omiten el croma y muestran la señal combinada como una imagen de escala de grises. (La señal está diseñada para que el croma no interfiera significativamente con la señal de luminancia). Los televisores en color pueden extraer el croma y volver a convertir la señal en RGB.

YUV tiene otra ventaja que es más relevante hoy en día. El ojo humano es menos sensible a los cambios en el matiz que los cambios en el brillo. Como resultado, una imagen puede tener menos información de croma que la información de luminancia sin sacrificar la calidad de la imagen. Por ejemplo, es habitual que muestre los valores de croma a la mitad de la resolución horizontal de las muestras de luminancia. En otras palabras, para cada dos muestras de luminancia en una fila de píxeles, hay un ejemplo de U y un ejemplo de V. Suponiendo que se usan 8 bits para codificar cada valor, se necesitan un total de 4 bytes para cada dos píxeles (dos Y ', una U y una V), para un promedio de 16 bits por píxel o un 30% menor que la codificación RGB equivalente de 24 bits.

YUV no es intrínsecamente más compacta que RGB. A menos que el croma sea Downsampled, un píxel YUV tiene el mismo tamaño que un píxel RGB. Además, la conversión de RGB a YUV no es una pérdida. Si no hay ninguna disminución de la resolución, se puede volver a convertir un píxel YUV a RGB sin pérdida de información. La reducción de la resolución de la imagen YUV es menor y también pierde parte de la información de color. Sin embargo, si se realiza correctamente, la pérdida no es perceptualmente significativa.

## <a name="yuv-in-computer-video"></a>Vídeo YUV en el equipo

Las fórmulas enumeradas anteriormente para YUV no son las conversiones exactas usadas en vídeo digital. El vídeo digital suele usar una forma de YUV denominada Y'CbCr. Esencialmente, Y'CbCr funciona escalando los componentes YUV a los siguientes intervalos:



| Componente | Intervalo                              |
|-----------|------------------------------------|
| Sí        | de 16 a 235                             |
| CB/CR     | 16 – 240, con 128 que representa cero |



 

Estos intervalos suponen 8 bits de precisión para los componentes de Y'CbCr. Esta es la derivación exacta de Y'CbCr, con la definición BT. 601 de luminancia:

1.  Empiece con valores RGB en el intervalo \[ 0... 1 \] . En otras palabras, el negro puro es 0 y el blanco puro es 1. Lo importante es que se trata de valores RGB no lineales (con corrección gamma).
2.  Calcular la luminancia. Para BT. 601, Y ' = 0.299 R + 0.587 G + 0.114 B, como se describió anteriormente.
3.  Calcular los valores de diferencia de croma intermedios (B-Y ') y (R-Y '). Estos valores tienen un intervalo de +/-0,886 para (B-Y ') y +/-0,701 para (R-Y ').
4.  Escale los valores de diferencia de croma de la manera siguiente:

    PB = (0,5/(1-0,114)) × (B-Y ')

    PR = (0,5/(1-0,299)) × (R-Y ')

    Estos factores de escala están diseñados para dar a ambos valores el mismo intervalo numérico, +/-0,5. Juntos, definen un espacio de colores YUV denominado Y'PbPr. Este espacio de colores se usa en vídeo de componentes analógicos.

5.  Escale los valores de Y'PbPr para obtener los valores de Y'CbCr finales:

    Y ' = 16 + 219 × Y '

    CB = 128 + 224 × PB

    CR = 128 + 224 × PR

Estos últimos factores de escala producen el intervalo de valores enumerados en la tabla anterior. Por supuesto, puede convertir RGB directamente en Y'CbCr sin almacenar los resultados intermedios. Los pasos se enumeran por separado aquí para mostrar cómo Y'CbCr deriva de las ecuaciones YUV originales proporcionadas al principio de este artículo.

En la tabla siguiente se muestran los valores RGB y YCbCr de varios colores, de nuevo con la definición BT. 601 de luminancia.



| Color   | R   | G   | B   | Sí  | CB  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Negro   | 0   | 0   | 0   | 16  | 128 | 128 |
| Rojo     | 255 | 0   | 0   | 81  | 90  | 240 |
| Verde   | 0   | 255 | 0   | 145 | 54  | 34  |
| Azul    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cian    | 0   | 255 | 255 | 170 | 166 | 16  |
| Fucsia | 255 | 0   | 255 | 106 | 202 | 222 |
| Amarillo  | 255 | 255 | 0   | 210 | 16  | 146 |
| Blanco   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Como se muestra en esta tabla, CB y CR no se corresponden con ideas intuitivas sobre el color. Por ejemplo, el blanco puro y el negro puro contienen niveles neutros de CB y CR (128). Los valores más altos y más bajos de CB son azul y amarillo, respectivamente. En CR, los valores más altos y más bajos son rojo y aguamarina.

## <a name="for-more-information"></a>Para obtener más información

-   [Formatos YUV de 8 bits recomendados para la representación de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Vídeo Demystified, quinta edición. Newnes, 2007.
-   Charles A. Poynton. Introducción técnica a vídeo digital. Wiley, 1996.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



