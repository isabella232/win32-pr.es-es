---
description: Acerca del vídeo de YUV
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Acerca del vídeo de YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499a8adfe1a43a22fe9bdd9ff4e576b7a14c398a9dafc0b945647d7225ad581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744253"
---
# <a name="about-yuv-video"></a>Acerca del vídeo de YUV

El vídeo digital se codifica a menudo en un *formato YUV.* En este artículo se explican los conceptos generales del vídeo de YUV, junto con cierta terminología, sin entrar en profundidad en las matemáticas del procesamiento de vídeo de YUV.

Si ha trabajado con gráficos de equipo, probablemente esté familiarizado con el color RGB. Un color RGB se codifica con tres valores: rojo, verde y azul. Estos valores corresponden directamente a partes del espectro visible. Los tres valores RGB forman un sistema de coordenadas matemático, denominado espacio *de color*. El componente rojo define un eje de este sistema de coordenadas, el azul define el segundo y el verde el tercero, como se muestra en la ilustración siguiente. Cualquier color RGB válido se encuentra en algún lugar dentro de este espacio de colores. Por ejemplo, el rojo puro es 100 % azul, 100 % rojo y 0 % verde.

![diagrama que muestra el espacio de colores rgb](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Aunque RGB es una manera común de representar colores, otros sistemas de coordenadas son posibles. El término *YUV hace* referencia a una familia de espacios de color, que codifican la información de brillo por separado de la información de color. Al igual que RGB, YUV usa tres valores para representar cualquier color. Estos valores se denominan Y', U y V. (De hecho, este uso del término "YUV" es técnicamente inexacto. En el vídeo del equipo, el término YUV casi siempre hace referencia a un espacio de color determinado denominado Y'CbCr, que se describe más adelante. Sin embargo, A menudo se usa YUV como término general para cualquier espacio de color que funcione con los mismos principios que Y'CbCr).

El componente Y', también denominado *luma*, representa el valor de brillo del color. El símbolo primo (') se usa para diferenciar luma de un valor estrechamente relacionado, *luminance*, que se designa como Y. La luminosidad se deriva de valores *RGB* lineales, mientras que luma se deriva de valores RGB no *lineales* (corregidos gamma). La luminosidad es una medida más cercana del brillo verdadero, pero luma es más práctica de usar por motivos técnicos. El símbolo primo se omite con frecuencia, pero los espacios de color YUV siempre usan luma, no luminance.

Luma se deriva de un color RGB tomando un promedio ponderado de los componentes rojo, verde y azul. Para televisión de definición estándar, se usa la fórmula siguiente:

`Y' = 0.299R + 0.587G + 0.114B`

Esta fórmula refleja el hecho de que el ojo humano es más sensible a determinadas longitudes de onda de luz que a otras, lo que afecta al brillo percibido de un color. La luz azul aparece más atenuada, el verde es más claro y el rojo está en algún lugar entre ellos. Esta fórmula también refleja las características físicas de los televisores iniciales. Se usa una fórmula más reciente, teniendo en cuenta la tecnología moderna de televisión, para televisión de alta definición:

`Y' = 0.2125R + 0.7154G + 0.0721B`

La ecuación luma para televisión de definición estándar se define en una especificación denominada ITU-R BT.601. Para televisión de alta definición, la especificación pertinente es ITU-R BT.709.

Los componentes you y V,  también denominados *valores de croma* o valores de diferencia de color, se derivan restando el valor Y de los componentes rojo y azul del color RGB original:

`U = B - Y'`

`V = R - Y'`

Juntos, estos valores contienen suficiente información para recuperar el valor RGB original.

## <a name="benefits-of-yuv"></a>Ventajas de YUV

La televisión análoga usa YUV en parte por motivos históricos. Las señales de televisión de color analógico se diseñaron para ser compatibles con las televisión en blanco y negro. La señal de televisión de color lleva la información de los colores (usted y V) superpuesta a la señal luma. Las televisión en blanco y negro omiten el tono y muestran la señal combinada como una imagen de escala de grises. (La señal está diseñada para que el brillo no interfiera significativamente con la señal luma). Los televisores de color pueden extraer el efecto de color y volver a convertir la señal en RGB.

YUV tiene otra ventaja que es más relevante hoy en día. El ojo humano es menos sensible a los cambios de matiz que a los cambios de brillo. Como resultado, una imagen puede tener menos información de color que la información de luma sin sacrificar la calidad percibida de la imagen. Por ejemplo, es habitual muestrear los valores de los mosaicos a la mitad de la resolución horizontal de las muestras de luma. En otras palabras, por cada dos muestras de luma en una fila de píxeles, hay una muestra de U y una muestra de V. Suponiendo que se usan 8 bits para codificar cada valor, se necesitan un total de 4 bytes por cada dos píxeles (dos Y, una U y una V), para un promedio de 16 bits por píxel, o un 30 % menos que la codificación RGB equivalente de 24 bits.

YUV no es intrínsecamente más compacto que RGB. A menos que se desmuestree la escala, un píxel YUV tiene el mismo tamaño que un píxel RGB. Además, la conversión de RGB a YUV no es una pérdida. Si no hay ningún contramuestreo, un píxel YUV se puede convertir de nuevo en RGB sin pérdida de información. El bajomuestreo hace que una imagen de YUV sea más pequeña y también pierde parte de la información de color. Sin embargo, si se realiza correctamente, la pérdida no es perceptualmente significativa.

## <a name="yuv-in-computer-video"></a>Vídeo de YUV en equipo

Las fórmulas enumeradas anteriormente para YUV no son las conversiones exactas que se usan en el vídeo digital. El vídeo digital suele utilizar una forma de YUV denominada Y'CbCr. Básicamente, Y'CbCr funciona mediante el escalado de los componentes de YUV a los siguientes intervalos:



| Componente | Intervalo                              |
|-----------|------------------------------------|
| Y'        | 16–235                             |
| Cb/Cr     | 16-240, con 128 que representa cero |



 

Estos intervalos suponen 8 bits de precisión para los componentes de Y'CbCr. Esta es la derivación exacta de Y'CbCr, mediante la definición BT.601 de luma:

1.  Comience con valores RGB en el \[ intervalo 0...1. \] En otras palabras, el negro puro es 0 y el blanco puro es 1. Lo importante es que se trata de valores RGB no lineales (corregidos gamma).
2.  Calcule el luma. Para BT.601, Y' = 0,299R + 0,587G + 0,114B, como se describió anteriormente.
3.  Calcule los valores intermedios de diferencias de intermedios (B - Y') e (R - Y'). Estos valores tienen un intervalo de +/- 0,886 para (B - Y') y +/- 0,701 para (R - Y').
4.  Escale los valores de diferencia de la escala como se muestra a continuación:

    Pb = (0,5 / (1 - 0,114)) × (B - Y')

    Pr = (0,5 / (1 - 0,299)) × (R - Y')

    Estos factores de escalado están diseñados para proporcionar a ambos valores el mismo intervalo numérico, +/- 0,5. Juntos, definen un espacio de colores YUV denominado Y'PbPr. Este espacio de color se usa en vídeo de componentes análogos.

5.  Escale los valores de Y'PbPr para obtener los valores finales de Y'CbCr:

    Y' = 16 + 219 × Y'

    Cb = 128 + 224 × Pb

    Cr = 128 + 224 × Pr

Estos últimos factores de escalado generan el intervalo de valores enumerados en la tabla anterior. Por supuesto, puede convertir RGB directamente a Y'CbCr sin almacenar los resultados intermedios. Los pasos se enumeran aquí por separado para mostrar cómo se deriva Y'CbCr de las ecuaciones YUV originales que se indican al principio de este artículo.

En la tabla siguiente se muestran los valores RGB y YCbCr para varios colores, usando de nuevo la definición BT.601 de luma.



| Color   | R   | G   | B   | Y'  | Cb  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Negro   | 0   | 0   | 0   | 16  | 128 | 128 |
| Rojo     | 255 | 0   | 0   | 81  | 90  | 240 |
| Verde   | 0   | 255 | 0   | 145 | 54  | 34  |
| Azul    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cian    | 0   | 255 | 255 | 170 | 166 | 16  |
| Fucsia | 255 | 0   | 255 | 106 | 202 | 222 |
| Amarillo  | 255 | 255 | 0   | 210 | 16  | 146 |
| Blanco   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Como se muestra en esta tabla, Cb y Cr no se corresponden con ideas intuitivas sobre el color. Por ejemplo, el blanco puro y el negro puro contienen niveles neutros de Cb y Cr (128). Los valores más altos y más bajos para Cb son azul y amarillo, respectivamente. Para Cr, los valores más altos y más bajos son rojo y cian.

## <a name="for-more-information"></a>Para obtener más información

-   [Formatos YUV de 8 bits recomendados para la representación en vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Vídeo Demystified, quinta edición. Newnes, 2007.
-   Charles A. Poymond. Una introducción técnica al vídeo digital. Wiley, 1996.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 



