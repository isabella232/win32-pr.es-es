---
description: En este tema se presentan los formatos de píxel que proporciona el componente de creación de imágenes de Windows (WIC).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Información general sobre formatos de píxeles nativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df37481399ac8193effc5d8f93aa49050460ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716399"
---
# <a name="native-pixel-formats-overview"></a>Información general sobre formatos de píxeles nativos

En este tema se presentan los formatos de píxel que proporciona el componente de creación de imágenes de Windows (WIC).

Un formato de píxel describe el diseño de memoria de cada píxel de un mapa de bits. Este diseño de memoria describe cómo se codifican los datos de imagen de un mapa de bits especificando el formato numérico y la organización del canal de color. WIC admite varios formatos numéricos para varios esquemas de organización de canal de color, lo que proporciona una amplia gama de formatos de píxeles.

-   [Profundidad de bits](#bit-depth)
-   [Codificación numérica](#numerical-encoding)
-   [Canales de color](#color-channels)
    -   [Modelo de color RGB/BGR](#rgbbgr-color-model)
    -   [Modelo de color CMYK](#cmyk-color-model)
    -   [Modelo de color de n canales](#n-channel-color-model)
    -   [Modelos de color indizados y de escala de grises](#indexed-and-grayscale-color-models)
    -   [Modelo de color Y'CbCr](#ycbcr-color-model)
-   [Formato de píxel de WIC](#wic-pixel-format)
    -   [Formatos de píxel no definidos](#undefined-pixel-formats)
    -   [Formatos de píxel indexados](#indexed-pixel-formats)
    -   [Formatos de píxeles de bits empaquetados](#packed-bit-pixel-formats)
    -   [Formatos de píxeles de escala de grises](#grayscale-pixel-formats)
    -   [Formatos de píxeles RGB/BGR](#rgbbgr-pixel-formats)
    -   [Formatos CMYK de píxeles](#cmyk-pixel-formats)
    -   [Formatos de píxel de canal n](#n-channel-pixel-formats)
    -   [Formatos de píxel de solo alfa](#alpha-only-pixel-formats)
    -   [Formatos de píxeles de Y'CbCr](#ycbcr-pixel-formats)
-   [Espacio de colores](#color-space)
-   [Formatos de imagen nativa](#native-image-formats)
    -   [Códec nativo de BMP](#bmp-native-codec)
    -   [Códec nativo GIF](#gif-native-codec)
    -   [Códec nativo de ICO](#ico-native-codec)
    -   [Códec JPEG nativo](#jpeg-native-codec)
    -   [Códec nativo PNG](#png-native-codec)
    -   [Códec nativo TIFF](#tiff-native-codec)
    -   [Códec nativo de JPEG-XR](#jpeg-xr-native-codec)
-   [Códec nativo de DDS](#dds-native-codec)
-   [Extensibilidad del formato de píxel](#pixel-format-extensibility)
-   [Temas relacionados](#related-topics)

## <a name="bit-depth"></a>Profundidad de bits

La *profundidad de bits* es el número de bits que se usa para codificar cada canal de color. En la actualidad, la mayoría de las imágenes digitales usan una profundidad de bits de 8, lo que significa que cada canal de color de un píxel se representa con 8 bits, lo que proporciona 2 ⁸ (256) valores únicos por canal. Una imagen que tiene una profundidad de bits de 8 y tres canales de color (como rojo, verde y azul) usa 24 bits por píxel (BPP), que proporciona los diferentes colores de 2 ² ⁴ (16.777.216) por píxel.

Para mejorar la resolución de color, se puede usar una profundidad de bits de 16 o 32. Esto proporciona a cada canal de color los valores únicos de 2 ¹ ⁶ (65.536) o 2 ³ ², a costa de más memoria por píxel.

En algunos formatos, la profundidad de bits no es múltiplo de 8. Estos formatos se denominan formatos *empaquetados* , ya que los canales de color de un píxel no se alinean con los límites de bytes. Por ejemplo, si las profundidades de bits de 5, tres canales de color se pueden almacenar en 16 bits (incluido 1 bit de relleno, para que los píxeles estén alineados por bytes). Los formatos empaquetados son útiles cuando se limita la capacidad de memoria o de procesamiento.

## <a name="numerical-encoding"></a>Codificación numérica

Para la mayoría de las imágenes digitales de hoy en día, se usan bytes sin signo y enteros cortos sin signo para describir el intervalo numérico de cada canal de color. El valor mínimo (0) representa la intensidad cero en un canal de color único y el negro se consigue cuando todos los canales de color son cero. Del mismo modo, el valor máximo representa la intensidad total y el blanco se consigue cuando todos los canales de color tienen una intensidad máxima. A una profundidad de bits de 8, un UINT proporciona 256 valores únicos por canal de color (0-255). Un UINT de 16 bits proporciona 65.536 valores únicos por canal de color (0-65.535).

Además, WIC admite formatos de punto fijo y de punto flotante. Estos formatos admiten intervalos dinámicos mayores, ya que todo el intervalo numérico de cada canal de color es mayor que el intervalo visible. Como resultado, los colores se pueden ajustar por encima o por debajo del rango visible, durante los pasos intermedios del procesamiento de imágenes, sin pérdida de información de la imagen.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point la codificación numérica

los valores de punto fijo de 16 bits se interpretan como s 2,13: bit de signo, dos bits enteros y trece bits fraccionarios. Mediante esta interpretación, un intervalo numérico de − 4,0 a + 3,999... se puede representar con el valor de 1,0 representado por el valor entero con signo 8192 (0x2000).

los valores de punto fijo de 32 bits se interpretan como s 7.24: Sign bit, siete bits enteros y veinte bits fraccionarios. Mediante esta interpretación, un intervalo numérico de − 128,0 a + 127,999... se puede representar con el valor de 1,0 representado por el valor entero con signo 16777216 (0x01000000).

## <a name="color-channels"></a>Canales de color

Los canales de color de un formato de píxel definen el diseño de memoria de cada color en los datos de imagen de un mapa de bits. Hay una variedad de estructuras de canal de color diferentes comunes en las imágenes digitales de hoy en día, y WIC proporciona compatibilidad con muchos de ellos.

### <a name="rgbbgr-color-model"></a>Modelo de color RGB/BGR

Los formatos RGB y BGR describen los colores de un modelo de color aditivo. El método más común para describir una imagen es con tres canales de color independientes que representan los colores rojo (R), verde (G) y azul (B). WIC proporciona compatibilidad con estos tres canales en el orden rojo-verde-azul (RGB) o azul-verde-rojo (BGR). Este es el orden en el que cada canal de color aparece dentro de la secuencia de bits secuencial. Por ejemplo, en el formato de GUID \_ WICPixelFormat32bppRGB, cada píxel tiene un ancho de 32 bits. El canal rojo es el primer byte (menos significativo) de la memoria, seguido de verde y azul. Por el contrario, en el formato de GUID \_ WICPixelFormat32bppBGR, los canales de color están en el orden contrario. WIC es compatible con varios formatos de RGB/BGR, incluidos los formatos de bits empaquetados especiales como GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Los canales de color de los formatos de bits empaquetados de BGR especiales no se encuentran en múltiplos de 8, como los canales de color de los formatos de píxel típicos. Esto significa que los valores del canal no se alinean en bytes. Se debe tener cuidado al leer canales de color de bits empaquetados.

 

Además de los formatos RGB y BGR, WIC también proporciona formatos de píxeles RGB y BGR que admiten un canal alfa (A). El canal alfa proporciona datos de opacidad para el píxel. En el caso de los formatos con un canal alfa agregado, el canal alfa normalmente se encuentra en último lugar en el orden del canal de color. Por ejemplo, en el formato de píxel GUID \_ WICPixelFormat32bppBGRA, el orden de los bytes es azul, verde y rojo, seguido del canal alfa.

WIC también admite formatos de píxel RGB de alfa premultiplicado (P). En un formato de píxel RGBA típico, los valores de color rojo, verde y azul son los valores de color reales de la imagen. Para crear una imagen compuesta en el formato RGBA estándar, el valor alfa de la imagen de primer plano se debe multiplicar por cada uno de los canales rojo, verde y azul antes de agregarlo al color de la imagen de fondo. En un formato de píxel RGB de alfa premultiplicado, cada canal de color ya se ha multiplicado por el valor alfa. Esto proporciona un método más eficaz de composición de imágenes con datos de canal alfa. Para recuperar los valores de color verdaderos de cada canal en un formato de píxel de PRGBA/PBGRA, la multiplicación de canal alfa se debe invertir dividiendo los valores de color por el valor alfa.

### <a name="cmyk-color-model"></a>Modelo de color CMYK

CMYK es un modelo de color de sustracción que se usa en la impresión. Los colores generados por un modelo CMYK son generados por la luz que no se absorbe, pero que se reflejan. CMYK es un modelo de cuatro canales de cian (C), magenta (M), amarillo (Y) y negro (K). Cuando los cuatro canales de color tienen el valor máximo, el resultado es negro. Al igual que los modelos de color RGB/BGR, el orden de los bytes dentro de la secuencia de bits secuencial viene determinado por el nombre del formato de píxel. Por ejemplo, en el formato de píxel GUID \_ WICPixelFormat32bppCMYK, cada píxel se compone de 32 bits. El primer byte contiene el valor aguamarina, seguido a su vez por magenta, amarillo y negro. WIC proporciona formatos de píxel para CMYK en 32 y 64 bits por píxel (BPP).

Además del modelo de color CMYK estándar, WIC también proporciona CMYK con Alpha. Esto permite que las imágenes CMYK tengan datos de mezcla alfa similares al modelo de color RGB/BGR. El canal alfa se encuentra inmediatamente después de negro en el flujo de bits secuencial de un mapa de bits.

### <a name="n-channel-color-model"></a>Modelo de color de n canales

Para mayor flexibilidad, WIC también proporciona formatos de píxel que no tienen un orden de canal predefinido. WIC proporciona formatos de píxel que admiten de tres a ocho canales de datos de imagen continuos a profundidad de bits de 8 y 16. A diferencia de los formatos de píxel RGB/BGR y CMYK, los formatos de n canales no especifican el orden del canal sino el número de canales de color disponibles. Por ejemplo, en el formato de píxel GUID \_ WICPixelFormat32bpp4Channels, cada píxel se compone de 32 bits con cada uno de los 4 canales que ocupan un solo byte.

WIC también proporciona formatos de píxel para el canal n con alfa. Esto permite que las imágenes de n canales tengan datos de mezcla alfa similares a los modelos de color RGB/BGR y CMYK. El canal alfa se encuentra inmediatamente después del último canal de color en el flujo de bits secuencial de un mapa de bits.

### <a name="indexed-and-grayscale-color-models"></a>Modelos de color indizados y de escala de grises

Los formatos *indexados* utilizan una tabla de colores, denominada *paleta*. La paleta se almacena externamente en los datos de píxeles o, de lo contrario, se define de forma implícita. El valor de cada píxel de la imagen es un índice en la paleta. Con un formato indizado, el número de bits por píxel está directamente relacionado con el número de entradas de la paleta. Esto reduce considerablemente la cantidad de datos necesarios para representar la imagen, pero también restringe el número de colores disponibles para la imagen. WIC admite formatos indizados con 1, 2, 4 u 8 BPP.

En el caso de los formatos monocromo (escala de grises), WIC admite 1, 2, 4, 8, 16 y 32 bits por píxel. En el caso de profundidades de bits de 1, 8, 16 y 32, los datos de color se almacenan en un solo canal. En el caso de profundidades de bits de 2 o 4, los índices se encuentran en una paleta de escala de grises.

### <a name="ycbcr-color-model"></a>Modelo de color Y'CbCr

WIC agrega compatibilidad con el modelo de color JPEG JFIF Y'CbCr. Y'CbCr separe los colores en un componente de luminancia (Y) y dos componentes de croma (CB y CR). Muchos archivos JPEG almacenan datos de imagen de forma nativa mediante el modelo de color Y'CbCr.

El sistema visual humano es menos sensible a los cambios en croma que a la luminancia, y los formatos de Y'CbCr pueden aprovechar esta sensibilidad reducida reduciendo la cantidad de datos de cromas que se almacenan en relación con la luminancia. Para ello, se almacena el croma y la luminancia en planos independientes y se escala cada plano de componente a una resolución diferente. Este procedimiento se conoce como submuestreo de croma.

Dado que los datos de croma y de luminancia se almacenan por separado y pueden tener distintas resoluciones, WIC define formatos de píxeles de luminancia y cromas independientes. WIC admite datos de 8 bits por canal.

## <a name="wic-pixel-format"></a>Formato de píxel de WIC

Los formatos de píxel en WIC se definen mediante GUID para evitar conflictos con los IHV. WIC proporciona un nombre descriptivo para hacer referencia al GUID de un formato de píxel nativo. La Convención de nomenclatura para los formatos de píxel de WIC es la siguiente:

**\[GUID \_ WICPixelFormat \] \[ bits por píxel \] \[ tipo de \] almacenamiento de orden de canal \[\]**

| Componente de formato         | Descripción                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Identificación descriptiva para todos los formatos de píxel de WIC. El nombre descriptivo para todos los píxeles de WIC comienza con esta cadena.                                                                                                                                                                                       |
| **Bits por píxel**       | El número de bits por píxel (BPP) usado para el formato de píxel.                                                                                                                                                                                                                                                |
| **Orden de canales**        | El modelo de canal de color y el orden de cada canal para el formato.                                                                                                                                                                                                                                            |
| **Tipo de almacenamiento**         | Codificación numérica utilizada para el formato de píxel. La codificación predeterminada es un entero sin signo. Si no hay nada que siga la información del modelo de color, se implica un entero sin signo (UINT). FixedPoint y float se usan para identificar formatos de píxeles que usan la codificación de punto flotante y punto flotante, respectivamente. |



 

> [!Note]  
> En el caso de los formatos de canal n, \[ el orden de los canales \] no especifica el orden de los colores, sino el número de canales disponibles. Por ejemplo, GUID \_ WICPixelFormat24bpp3Channels proporciona 3 canales de color donde "3Channels" es la \[ entrada de orden del canal \] , pero solo indica el número de canales y no el pedido.

 

Por ejemplo, el nombre descriptivo GUID \_ WICPixelFormat24bppRGB significa que el formato de píxel usa 24 bits por píxel y el modelo de color RGB. Dado que el nombre no identifica explícitamente un tipo de almacenamiento, se implica un entero sin signo.

WIC admite varios formatos de píxeles. En las tablas siguientes se agrupan formatos de píxel similares por estructura de color, al tiempo que se proporciona información adicional, como la profundidad de bits, los bits por píxel y la codificación numérica. Cada tabla contiene la siguiente información:

-   **Nombre descriptivo**. Nombre descriptivo del formato de píxel.
-   **Recuento de canales**. Número de canales de color.
-   **Bits por canal**. Número de bits por canal (profundidad de bits).
-   **Bits por píxel**. Número de bits por píxel, incluidos los bits de relleno.
-   **Tipo de almacenamiento**. Codificación numérica de los datos de la imagen. Este valor puede ser un entero sin signo (UINT), un número de punto fijo (FixedPoint) o un número de punto flotante (float).

> [!Note]  
> Para mayor claridad, este documento hace referencia a los formatos de píxel solo por sus nombres descriptivos. El valor hexadecimal real de los formatos de píxeles se puede encontrar en los archivos wincodec. h/IDL.

 

### <a name="undefined-pixel-formats"></a>Formatos de píxel no definidos

La lista siguiente muestra los formatos de píxeles genéricos que se usan cuando el formato de píxel es indefinido o no es importante para una operación de imagen.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formatos de píxel indexados

En la tabla siguiente se enumeran los formatos de píxel indexados que proporciona WIC. En estos formatos, el valor de cada píxel es un índice en una paleta de colores.



| Nombre descriptivo                   | Recuento de canales | Bits por píxel | Tipo de almacenamiento |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formatos de píxeles de bits empaquetados

En la tabla siguiente se enumeran los formatos de bits empaquetados proporcionados por WIC. En estos formatos, los datos del canal de color no están alineados en bytes.



| Nombre descriptivo                          | Recuento de canales | Bits por canal       | Bits por píxel | Tipo de almacenamiento |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5 (B)/6 (G)/5 (R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5 (B)/5 (G)/5 (R)/1 (A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |

En el caso de los \_ formatos GUID WICPixelFormat32bppBGR101010 y \_ WICPixelFormat32bppRGBA1010102 GUID, el canal rojo se almacena en los bits menos significativos. En el caso de los \_ formatos GUID WICPixelFormat32bppR10G10B10A2 y \_ WICPixelFormat32bppR10G10B10A2HDR10 GUID, el canal rojo se define en los bits más significativos, el mismo diseño que [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

El formato de GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 es el formato de píxel de 10 bits para HDR10 (espacio de colores BT. 2020 y SMPTE St. 2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formatos de píxeles de escala de grises

En la tabla siguiente se enumeran los formatos de escala de grises que proporciona WIC. En estos formatos, los datos de color representan tonalidades de gris.



| Nombre descriptivo                           | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>Formatos de píxeles RGB/BGR

En la tabla siguiente se enumeran los formatos RGB/BGR proporcionados por WIC. Estos formatos separan los datos de color primario en canales rojo (R), verde (G) y azul (B). Se proporciona un canal alfa (A) adicional para la información de opacidad en algunos formatos.



| Nombre descriptivo                            | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | Float        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | Fijo        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | Fijo        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | Float        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | Fijo        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | Fijo        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | Fijo        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | Fijo        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | Fijo        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | Fijo        |



 

> [!Note]  
> \*El \_ formato WICPixelFormat32bppRGBE de GUID codifica los valores de punto flotante de 3 16 bits en 4 bytes, como se indica a continuación: tres mantisa de 8 bits sin signo para los canales R, G y B, más un exponente compartido de 8 bits. Este formato proporciona una precisión de punto flotante de 16 bits en una representación de píxeles más pequeña.

 

A partir de Windows 8 y la [actualización de la plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), WIC proporciona formatos adicionales, que se muestran en la tabla aquí.



| Nombre descriptivo                      | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formatos CMYK de píxeles

En la tabla siguiente se enumeran los formatos CMYK proporcionados por WIC. Estos formatos separan los datos de color primario en canales cian (C), magenta (M), amarillo (Y) y negro (K).



| Nombre descriptivo                      | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formatos de píxel de canal n

En la tabla siguiente se enumeran los formatos de n canales proporcionados por WIC. Estos formatos proporcionan una serie de canales de color sin definir para almacenar los datos de la imagen.



| Nombre descriptivo                            | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Formatos de píxel de solo alfa

En la tabla siguiente se enumeran los formatos de solo alfa proporcionados por WIC. Este formato solo contiene información alfa.



| Nombre descriptivo                 | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formatos de píxeles de Y'CbCr

En la tabla siguiente se enumeran los formatos de Y'CbCr proporcionados por WIC. Estos formatos separan los datos de color primario en luminancia (Y), la diferencia de croma azul (CB) y la diferencia de Choma roja (CR). Tenga en cuenta que estos formatos están diseñados para almacenar datos JPEG JFIF Y'CbCr píxeles.



| Nombre descriptivo                 | Recuento de canales | Bits por píxel | Tipo de almacenamiento |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Espacio de colores

Los formatos de píxel en sí mismos no tienen un espacio de colores. Por lo general, el espacio de colores es una interpretación semántica de los valores de píxeles que depende del contexto del mapa de bits. Algunas imágenes identifican un contexto de color que define el espacio de colores de la imagen. Solo en ausencia de un contexto de color, se debe inferir el espacio de colores.

La información de contexto de color se define mediante la interfaz [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para WIC. Para recuperar la información de contexto de color de un marco de imagen, use el método **GetColorContext** .

En ausencia de información sobre el espacio de colores de una imagen, la regla general para la inferencia del espacio de colores es que los formatos de tipo UINT RGB y de escala de grises usan el espacio de colores RGB (sRGB) estándar, mientras que los formatos RGB y de escala de grises extendidos usan el espacio de colores RGB (scRGB). El modelo de color CMYK usa un espacio de colores RWOP.

## <a name="native-image-formats"></a>Formatos de imagen nativa

Cada uno de los códecs WIC proporcionados por Windows admite un subconjunto de los formatos de píxel de WIC. Para cada códec, los formatos de descodificación admitidos pueden ser diferentes de los formatos de codificación admitidos.

Al descodificar una imagen, si los datos se almacenan de forma nativa en un formato de píxel que el descodificador no admite, se convertirá en un formato admitido. Para determinar el formato de píxel de salida, llame a [**IWICBitmapFrameDecode:: GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Al codificar una imagen, use [**IWICBitmapFrameEncode:: SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) para solicitar que el codificador use un formato de píxel específico. El codificador devolverá el formato de píxel más cercano compatible, que puede ser diferente del que se solicitó.

En las tablas siguientes se muestran los formatos de píxel admitidos por cada uno de los códecs WIC proporcionados por Windows.

### <a name="bmp-native-codec"></a>Códec nativo de BMP



| Formatos de píxeles del descodificador                   | Formatos de píxeles del codificador                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | GUID \_ WICPixelFormat32bppBGRA\*         |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint | GUID \_ WICPixelFormat32bppPBGRA          |
|                                         | GUID \_ WICPixelFormat64bppRGBAFixedPoint |
|                                         | GUID \_ WICPixelFormat64bppBGRAFixedPoint |



 

> [!Note]  
> GUID \_ WICPixelFormat32bppBGRA solo se admite en Windows 8, la [actualización de la plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)y versiones posteriores.
>
> -   Para codificar en este formato, use la opción de codificador **EnableV5Header32bppBGRA** . El BMP se escribirá con un encabezado BITMAPV5HEADER.
> -   Si un archivo tiene un BITMAPV5HEADER, se descodifica como GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Códec nativo GIF



| Formatos de píxeles del descodificador           | Formatos de píxeles del codificador           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Códec nativo de ICO



| Formatos de píxeles del descodificador         | Formatos de píxeles del codificador |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Códec JPEG nativo



| Formatos de píxeles del descodificador         | Formatos de píxeles del codificador         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Códec nativo PNG



| Formatos de píxeles del descodificador           | Formatos de píxeles del codificador           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite  | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat2bppGray    | GUID \_ WICPixelFormat2bppGray    |
| GUID \_ WICPixelFormat4bppGray    | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray    | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray   | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat24bppBGR    | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat32bppBGRA   | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat48bppRGB    | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat64bppRGBA   | GUID \_ WICPixelFormat48bppBGR    |
|                                 | GUID \_ WICPixelFormat64bppRGBA   |
|                                 | GUID \_ WICPixelFormat64bppBGRA   |



 

### <a name="tiff-native-codec"></a>Códec nativo TIFF



| Formatos de píxeles del descodificador                | Formatos de píxeles del codificador           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite       | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat4bppGray         | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray         | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray        | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat32bppGrayFloat   | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat24bppBGR         | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppCMYK   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppCMYK        |                                 |
| GUID \_ WICPixelFormat40bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppCMYK        |                                 |
| GUID \_ WICPixelFormat80bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> GUID \_ WICPixelFormat96bppRGBFloat solo se admite en Windows 8, la [actualización de la plataforma para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)y versiones posteriores.

 

### <a name="jpeg-xr-native-codec"></a>Códec nativo de JPEG-XR



| Formatos de píxeles del descodificador                    | Formatos de píxeles del codificador                    |
|------------------------------------------|------------------------------------------|
| GUID \_ WICPixelFormatBlackWhite           | GUID \_ WICPixelFormatBlackWhite           |
| GUID \_ WICPixelFormat8bppGray             | GUID \_ WICPixelFormat8bppGray             |
| GUID \_ WICPixelFormat16bppBGR555          | GUID \_ WICPixelFormat16bppBGR555          |
| GUID \_ WICPixelFormat16bppGray            | GUID \_ WICPixelFormat16bppGray            |
| GUID \_ WICPixelFormat24bppBGR             | GUID \_ WICPixelFormat24bppBGR             |
| GUID \_ WICPixelFormat24bppRGB             | GUID \_ WICPixelFormat24bppRGB             |
| GUID \_ WICPixelFormat32bppBGR             | GUID \_ WICPixelFormat32bppBGR             |
| GUID \_ WICPixelFormat32bppBGRA            | GUID \_ WICPixelFormat32bppBGRA            |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | GUID \_ WICPixelFormat48bppRGBFixedPoint   |
| GUID \_ WICPixelFormat16bppGrayFixedPoint  | GUID \_ WICPixelFormat16bppGrayFixedPoint  |
| GUID \_ WICPixelFormat32bppBGR101010       | GUID \_ WICPixelFormat32bppBGR101010       |
| GUID \_ WICPixelFormat48bppRGB             | GUID \_ WICPixelFormat48bppRGB             |
| GUID \_ WICPixelFormat64bppRGBA            | GUID \_ WICPixelFormat64bppRGBA            |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat96bppRGBFixedPoint   |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat128bppRGBAFloat      |
| GUID \_ WICPixelFormat128bppRGBFloat       | GUID \_ WICPixelFormat128bppRGBFloat       |
| GUID \_ WICPixelFormat32bppCMYK            | GUID \_ WICPixelFormat32bppCMYK            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppCMYK            | GUID \_ WICPixelFormat64bppCMYK            |
| GUID \_ WICPixelFormat24bpp3Channels       | GUID \_ WICPixelFormat24bpp3Channels       |
| GUID \_ WICPixelFormat32bpp4Channels       | GUID \_ WICPixelFormat32bpp4Channels       |
| GUID \_ WICPixelFormat40bpp5Channels       | GUID \_ WICPixelFormat40bpp5Channels       |
| GUID \_ WICPixelFormat48bpp6Channels       | GUID \_ WICPixelFormat48bpp6Channels       |
| GUID \_ WICPixelFormat56bpp7Channels       | GUID \_ WICPixelFormat56bpp7Channels       |
| GUID \_ WICPixelFormat64bpp8Channels       | GUID \_ WICPixelFormat64bpp8Channels       |
| GUID \_ WICPixelFormat48bpp3Channels       | GUID \_ WICPixelFormat48bpp3Channels       |
| GUID \_ WICPixelFormat64bpp4Channels       | GUID \_ WICPixelFormat64bpp4Channels       |
| GUID \_ WICPixelFormat80bpp5Channels       | GUID \_ WICPixelFormat80bpp5Channels       |
| GUID \_ WICPixelFormat96bpp6Channels       | GUID \_ WICPixelFormat96bpp6Channels       |
| GUID \_ WICPixelFormat112bpp7Channels      | GUID \_ WICPixelFormat112bpp7Channels      |
| GUID \_ WICPixelFormat128bpp8Channels      | GUID \_ WICPixelFormat128bpp8Channels      |
| GUID \_ WICPixelFormat40bppCMYKAlpha       | GUID \_ WICPixelFormat40bppCMYKAlpha       |
| GUID \_ WICPixelFormat80bppCMYKAlpha       | GUID \_ WICPixelFormat80bppCMYKAlpha       |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | GUID \_ WICPixelFormat32bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | GUID \_ WICPixelFormat40bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | GUID \_ WICPixelFormat48bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | GUID \_ WICPixelFormat56bpp6ChannelsAlpha  |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | GUID \_ WICPixelFormat64bpp7ChannelsAlpha  |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | GUID \_ WICPixelFormat72bpp8ChannelsAlpha  |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | GUID \_ WICPixelFormat64bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | GUID \_ WICPixelFormat80bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | GUID \_ WICPixelFormat96bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bppRGBAHalf        | GUID \_ WICPixelFormat112bpp6ChannelsAlpha |
| GUID \_ WICPixelFormat48bppRGBHalf         | GUID \_ WICPixelFormat128bpp7ChannelsAlpha |
| GUID \_ WICPixelFormat32bppRGBE            | GUID \_ WICPixelFormat144bpp8ChannelsAlpha |
| GUID \_ WICPixelFormat16bppGrayHalf        | GUID \_ WICPixelFormat64bppRGBAHalf        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint  | GUID \_ WICPixelFormat48bppRGBHalf         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | GUID \_ WICPixelFormat32bppRGBE            |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | GUID \_ WICPixelFormat16bppGrayHalf        |
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ WICPixelFormatBlackWhite           |



 

## <a name="dds-native-codec"></a>Códec nativo de DDS



| Formatos de píxeles del descodificador          | Formatos de píxeles del codificador          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> El códec DDS de Windows proporciona compatibilidad con archivos DDS codificados con los siguientes \_ valores de formato de DXGI:

 

-   Formato de DXGI \_ \_ BC1 \_ UNORM
-   Formato de DXGI \_ \_ BC2 \_ UNORM
-   Formato de DXGI \_ \_ BC3 \_ UNORM

Se descodifican y codifican como GUID \_ WICPixelFormat32bppBGRA o GUID \_ WICPixelFormat32bppPBGRA. Para obtener más información, vea [información general sobre el formato DDS](dds-format-overview.md).

## <a name="pixel-format-extensibility"></a>Extensibilidad del formato de píxel

Los formatos de imagen personalizados pueden usar formatos de píxeles que no son proporcionados de forma nativa por WIC como YCbCr (YUV) y YCCK (Y/CB/CR/K). WIC proporciona un modelo de extensibilidad que permite que los formatos de píxel integrados y los complementos funcionen dentro de la misma canalización de imágenes. Para integrar estos formatos de píxel con la canalización de imágenes de WIC, debe crear convertidores de formato de píxel para convertir formatos de píxeles de complemento en uno o varios de los formatos de píxel nativos. La interfaz principal para generar convertidores de formato es [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUID y CLSID de WIC](-wic-guids-clsids.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[HD Photo Specification 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
