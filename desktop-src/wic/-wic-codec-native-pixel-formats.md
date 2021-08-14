---
description: En este tema se presentan los formatos de píxeles proporcionados por Windows Imaging Component (WIC).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Información general sobre los formatos de píxeles nativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379e67d422ccbd05ef178e67eb25c973e6b5943ef85d22873097f245f8914a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206344"
---
# <a name="native-pixel-formats-overview"></a>Información general sobre los formatos de píxeles nativos

En este tema se presentan los formatos de píxeles proporcionados por Windows Imaging Component (WIC).

Un formato de píxel describe el diseño de memoria de cada píxel de un mapa de bits. Este diseño de memoria describe cómo se codifican los datos de imagen de un mapa de bits especificando el formato numérico y la organización del canal de color. WIC admite varios formatos numéricos para varios esquemas de organización de canal de color, lo que proporciona una amplia gama de formatos de píxel.

-   [Profundidad de bits](#bit-depth)
-   [Codificación numérica](#numerical-encoding)
-   [Canales de color](#color-channels)
    -   [Modelo de color RGB/BGR](#rgbbgr-color-model)
    -   [Modelo de color COLOR](#cmyk-color-model)
    -   [Modelo de color de n canales](#n-channel-color-model)
    -   [Modelos de color indexados y de escala de grises](#indexed-and-grayscale-color-models)
    -   [Modelo de color Y'CbCr](#ycbcr-color-model)
-   [Formato de píxel wic](#wic-pixel-format)
    -   [Formatos de píxeles no definidos](#undefined-pixel-formats)
    -   [Formatos de píxel indexados](#indexed-pixel-formats)
    -   [Formatos de píxeles de bits empaquetados](#packed-bit-pixel-formats)
    -   [Formatos de píxeles de escala de grises](#grayscale-pixel-formats)
    -   [Formatos de píxel RGB/BGR](#rgbbgr-pixel-formats)
    -   [Formatos de píxeles de XEL](#cmyk-pixel-formats)
    -   [Formatos de píxeles de n canales](#n-channel-pixel-formats)
    -   [Formatos de píxeles de solo alfa](#alpha-only-pixel-formats)
    -   [Formatos de píxeles Y'CbCr](#ycbcr-pixel-formats)
-   [Espacio de color](#color-space)
-   [Formatos de imagen nativa](#native-image-formats)
    -   [Códec nativo BMP](#bmp-native-codec)
    -   [Códec nativo GIF](#gif-native-codec)
    -   [Códec nativo de ICO](#ico-native-codec)
    -   [Códec nativo JPEG](#jpeg-native-codec)
    -   [Códec nativo PNG](#png-native-codec)
    -   [Códec nativo TIFF](#tiff-native-codec)
    -   [Códec nativo JPEG-XR](#jpeg-xr-native-codec)
-   [Códec nativo de DDS](#dds-native-codec)
-   [Extensibilidad del formato de píxel](#pixel-format-extensibility)
-   [Temas relacionados](#related-topics)

## <a name="bit-depth"></a>Profundidad de bits

La *profundidad de bits* es el número de bits usados para codificar cada canal de color. En la actualidad, la mayoría de las imágenes digitales usan una profundidad de bits de 8, lo que significa que cada canal de color de un píxel se representa mediante 8 bits, lo que proporciona 2⁸ (256) valores únicos por canal. Una imagen que tiene una profundidad de bits de 8 y tres canales de color (como rojo, verde y azul) usa 24 bits por píxel (bpp), lo que proporciona 2⁴ (16 777 216) colores diferentes por píxel.

Para una mejor resolución de color, se puede usar una profundidad de bits de 16 o 32. Esto proporciona a cada canal de color 2⁶ (65 536) o 2 además de valores únicos, a un costo de más memoria por píxel.

En algunos formatos, la profundidad de bits no es un múltiplo de 8. Estos formatos se *denominan formatos empaquetados,* porque los canales de color de un píxel no están alineados con los límites de bytes. Por ejemplo, si las profundidades de bits de 5, se pueden almacenar tres canales de color en 16 bits (incluido un bit de relleno, para que los píxeles se alineen en bytes). Los formatos empaquetados son útiles cuando la memoria o la potencia de procesamiento están limitadas.

## <a name="numerical-encoding"></a>Codificación numérica

En la mayoría de las imágenes digitales actuales, se usan bytes sin signo y enteros cortos sin signo para describir el intervalo numérico de cada canal de color. El valor mínimo (0) representa la intensidad cero en un único canal de color y el negro se logra cuando todos los canales de color son cero. Del mismo modo, el valor máximo representa la intensidad completa y el blanco se logra cuando todos los canales de color tienen una intensidad completa. A una profundidad de bits de 8, un UINT proporciona 256 valores únicos por canal de color (0 - 255). Un UINT de 16 bits proporciona 65 536 valores únicos por canal de color (de 0 a 65 535).

Además, WIC admite formatos de punto fijo y de punto flotante. Estos formatos admiten intervalos dinámicos más grandes, ya que todo el intervalo numérico de cada canal de color es mayor que el intervalo visible. Como resultado, los colores se pueden ajustar por encima o por debajo del intervalo visible, durante los pasos intermedios del procesamiento de imágenes, sin pérdida de información de imagen.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point codificación numérica

Los valores de punto fijo de 16 bits se interpretan como s2.13: bit de signo, dos bits enteros y 13 bits fraccionales. Con esta interpretación, un intervalo numérico de entre -4,0 y +3,999... se puede representar, con el valor de 1,0 representado por el valor entero con signo 8192 (0x2000).

Los valores de punto fijo de 32 bits se interpretan como s7.24: bit de signo, siete bits enteros y 24 fracciones de bits. Con esta interpretación, un intervalo numérico de entre -128,0 y +127,999... se puede representar, con el valor de 1,0 representado por el valor entero con signo 16777216 (0x01000000).

## <a name="color-channels"></a>Canales de color

Los canales de color de un formato de píxel definen el diseño de memoria de cada color dentro de los datos de imagen de un mapa de bits. Hay una variedad de estructuras de canal de color diferentes comunes en las imágenes digitales de hoy en día, y WIC proporciona compatibilidad con muchas de ellas.

### <a name="rgbbgr-color-model"></a>Modelo de color RGB/BGR

Los formatos RGB y BGR describen los colores de un modelo de color aditiva. El método más común para describir una imagen es con tres canales de color independientes que representan los colores rojo (R), verde (G) y azul (B). WIC proporciona compatibilidad con estos tres canales en el orden rojo-verde-azul (RGB) o azul-verde-rojo (BGR). Este es el orden en el que cada canal de color aparece dentro de la secuencia de bits secuencial. Por ejemplo, en el formato \_ GUID WICPixelFormat32bppRGB, cada píxel tiene 32 bits de ancho. El canal rojo es el primer byte (menos significativo) en memoria, seguido de verde y, a continuación, azul. Por el contrario, en el formato \_ WICPixelFormat32bppBGR guid, los canales de color están en el orden opuesto. WIC admite varios formatos RGB/BGR, incluidos formatos de bits empaquetados especiales, como GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> Los canales de color de los formatos de bits empaquetados de BGR especiales no están en múltiplo de 8, como los canales de color en formatos de píxel típicos. Esto significa que los valores del canal no están alineados en bytes. Se debe tener cuidado al leer los canales de color de bits empaquetados.

 

Además de los formatos RGB y BGR, WIC también proporciona formatos de píxel RGB y BGR que admiten un canal alfa (A). El canal alfa proporciona datos de opacidad para el píxel. En el caso de los formatos con un canal alfa agregado, el canal alfa suele aparecer en último lugar en el orden del canal de color. Por ejemplo, en el formato de píxel GUID WICPixelFormat32bppBGRA, el orden de bytes es azul, verde y rojo, seguido del \_ canal alfa.

WIC también admite formatos de píxel RGB alfa multiplicados previamente (P). En un formato de píxel RGBA típico, los valores de color rojo, verde y azul son los valores de color reales de la imagen. Para crear una imagen compuesta en el formato RGBA estándar, el valor alfa de la imagen en primer plano debe multiplicarse por cada uno de los canales rojo, verde y azul antes de agregarlo al color de la imagen de fondo. En un formato de píxel rgb alfa multiplicado previamente, cada canal de color ya se ha multiplicado por el valor alfa. Esto proporciona un método más eficaz de composición de imágenes con datos de canal alfa. Para recuperar los valores de color verdaderos de cada canal en un formato de píxel PRGBA/PBGRA, la multiplicación del canal alfa se debe invertir dividiendo los valores de color por el valor alfa.

### <a name="cmyk-color-model"></a>Modelo de color COLOR

OFFSET es un modelo de color resta que se usa en la impresión. Los colores generados por un modelo IONE se generan mediante la luz que no se trata, sino que se refleja. CIAN es un modelo de cuatro canales de cian (C), al rojo (M), al amarillo (Y) y al negro (K). Cuando los cuatro canales de color están en el valor máximo, el resultado es negro. Al igual que los modelos de color RGB/BGR, el orden de bytes dentro de la secuencia de bits secuencial está determinado por el nombre del formato de píxel. Por ejemplo, en el formato de píxel GUID \_ WICPixelFormat32bpp JPEG, cada píxel está compuesto por 32 bits. El primer byte contiene el valor de cian, seguido a su vez por el color púrpura, amarillo y negro. WIC proporciona formatos de píxel para XEL a 32 y 64 bits por píxel (bpp).

Además del modelo de color CIC estándar, WIC también proporciona CIC con alfa. Esto permite que las imágenes COMBINE tengan datos de combinación alfa similares al modelo de color RGB/BGR. El canal alfa se encuentra inmediatamente después del negro en la secuencia de bits secuencial de un mapa de bits.

### <a name="n-channel-color-model"></a>Modelo de color de n canales

Para mayor flexibilidad, WIC también proporciona formatos de píxeles que no tienen un orden de canal predefinido. WIC proporciona formatos de píxeles que admiten entre tres y ocho canales de datos de imagen continuos a profundidades de bits de 8 y 16. A diferencia de los formatos de píxel RGB/BGR y PRECISE, los formatos de n canales no especifican el orden del canal, sino el número de canales de color disponibles. Por ejemplo, en el formato de píxel GUID WICPixelFormat32bpp4Channels, cada píxel se forma con 32 bits y cada uno de los 4 canales ocupa un \_ solo byte.

WIC también proporciona formatos de píxel para n canales con alfa. Esto permite que las imágenes de n canales tengan datos de combinación alfa similares a los modelos de color RGB/BGR y RGB. El canal alfa se encuentra inmediatamente después del último canal de color en el flujo de bits secuencial de un mapa de bits.

### <a name="indexed-and-grayscale-color-models"></a>Modelos de color indexados y de escala de grises

*Los formatos* indexados usan una tabla de colores, denominada *paleta*. La paleta se almacena externamente en los datos de píxeles o se define implícitamente. El valor de cada píxel de la imagen es un índice en la paleta. Con un formato indexado, el número de bits por píxel está directamente relacionado con el número de entradas de la paleta. Esto reduce significativamente la cantidad de datos necesarios para representar la imagen, pero también restringe el número de colores disponibles para la imagen. WIC admite formatos indexados con 1, 2, 4 u 8 bpp.

En el caso de los formatos monocromáticos (escala de grises), WIC admite 1, 2, 4, 8, 16 y 32 bits por píxel. Para las profundidades de bits de 1, 8, 16 y 32, los datos de color se almacenan en un único canal. Para profundidades de bits de 2 o 4, los píxeles son índices en una paleta de escala de grises.

### <a name="ycbcr-color-model"></a>Modelo de color de Y'CbCr

WIC agrega compatibilidad con el modelo de color JPEG JFIF Y'CbCr. Y'CbCr separa los colores en un componente de luma (Y' ) y dos componentes de componentes de componentes (Cb y Cr). Muchos archivos JPEG almacenan datos de imagen de forma nativa mediante el modelo de color Y'CbCr.

El sistema visual humano es menos sensible a los cambios en el lenguaje que al luma, y los formatos Y'CbCr pueden aprovechar esta sensibilidad reducida al reducir la cantidad de datos de la zona de calor que se almacenan en relación con luma. Para ello, almacenan el brillo y el luma en planos independientes y escalan cada plano de componente a una resolución diferente. Esta práctica se conoce como submuestreo de tosco.

Dado que los datos de color y luma se almacenan por separado y pueden ser resoluciones diferentes, WIC define formatos de píxeles de luma y de píxeles de forma independiente. WIC admite datos de 8 bits por canal.

## <a name="wic-pixel-format"></a>Formato de píxel de WIC

Los formatos de píxel de WIC se definen mediante GUID para evitar conflictos con los IHV. WIC proporciona un nombre descriptivo para hacer referencia al GUID de un formato de píxel nativo. La convención de nomenclatura para los formatos de píxeles de WIC es la siguiente:

**\[Guid \_ WICPixelFormat \] \[ Bits per Pixel Channel Order \] \[ Storage \] \[ Type\]**

| Componente de formato         | Descripción                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Identificación descriptiva para todos los formatos de píxel de WIC. El nombre descriptivo de todos los píxeles de WIC comienza con esta cadena.                                                                                                                                                                                       |
| **Bits por píxel**       | Número de bits por píxel (bpp) usados para el formato de píxel.                                                                                                                                                                                                                                                |
| **Orden del canal**        | Modelo de canal de color y orden de cada canal para el formato.                                                                                                                                                                                                                                            |
| **Tipo de almacenamiento**         | Codificación numérica utilizada para el formato de píxel. La codificación predeterminada es un entero sin signo. Si nada sigue la información del modelo de color, se implica un entero sin signo (UINT). FixedPoint y Float se usan para identificar formatos de píxel que usan codificación de punto fijo y punto flotante respectivamente. |



 

> [!Note]  
> En el caso de los formatos de n canales, El orden del canal no \[ especifica el orden de \] color, sino el número de canales disponibles. Por ejemplo, GUID \_ WICPixelFormat24bpp3Channels proporciona 3 canales de color donde "3Channels" es la entrada channel order, pero indica solo el número de canales y no el \[ \] orden.

 

Por ejemplo, el nombre descriptivo GUID WICPixelFormat24bppRGB significa que el formato de píxel usa 24 bits por píxel y el \_ modelo de color RGB. Dado que el nombre no identifica explícitamente un tipo de almacenamiento, se implica un entero sin signo.

WIC admite varios formatos de píxel. Las tablas siguientes agrupan formatos de píxeles similares por estructura de color y proporcionan información adicional, como la profundidad de bits, los bits por píxel y la codificación numérica. Cada tabla contiene la siguiente información:

-   **Nombre descriptivo**. Nombre descriptivo del formato de píxel.
-   **Recuento de canales**. Número de canales de color.
-   **Bits por canal.** Número de bits por canal (profundidad de bits).
-   **Bits por píxel.** Número de bits por píxel, incluidos los bits de relleno.
-   **Storage tipo**. Codificación numérica de los datos de la imagen. Este valor puede ser un entero sin signo (UINT), un número de punto fijo (FixedPoint) o un número de punto flotante (Float).

> [!Note]  
> Para mayor claridad, este documento hace referencia a formatos de píxel solo por sus nombres descriptivos. El valor hexadecimal real de los formatos de píxel se puede encontrar en los archivos wincodec.h/idl.

 

### <a name="undefined-pixel-formats"></a>Formatos de píxeles no definidos

En la lista siguiente se muestran los formatos de píxel genéricos que se usan cuando el formato de píxel es indefinido o no es importante para una operación de imagen.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formatos de píxeles indexados

En la tabla siguiente se enumeran los formatos de píxel indexados proporcionados por WIC. En estos formatos, el valor de cada píxel es un índice en una paleta de colores.



| Nombre descriptivo                   | Recuento de canales | Bits por píxel | Tipo de almacenamiento |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formatos de píxeles de bits empaquetados

En la tabla siguiente se enumeran los formatos de bits empaquetados proporcionados por WIC. En estos formatos, los datos del canal de color no están alineados con bytes.



| Nombre descriptivo                          | Recuento de canales | Bits por canal       | Bits por píxel | Tipo de almacenamiento |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5(B)/6(G)/5(R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5(B)/5(G)/5(R)/1(A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |

Para los formatos \_ WICPixelFormat32bppBGR101010 y GUID \_ WICPixelFormat32bppRGBA1010102, el canal rojo se almacena en los bits menos significativos. Para los formatos \_ GUID WICPixelFormat32bppR10G10B10A2 y GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, el canal rojo se [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)define en los bits más significativos, el mismo diseño que DXGI_FORMAT_R10G10B10A2_UNORM .

El formato \_ WICPixelFormat32bppR10G10B10A2HDR10 es el formato de píxel de 10 bits para HDR10 (espacio de colores BT.2020 y SMPTE ST.2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formatos de píxeles de escala de grises

En la tabla siguiente se enumeran los formatos de escala de grises proporcionados por WIC. En estos formatos, los datos de color representan tonos de gris.



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



 

### <a name="rgbbgr-pixel-formats"></a>Formatos de píxel RGB/BGR

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
> \*El formato GUID WICPixelFormat32bppRGBE codifica tres valores de punto flotante de 16 bits en 4 bytes, como se muestra a continuación: tres mantisas de 8 bits sin signo para los canales R, G y B, además de un exponente compartido de \_ 8 bits. Este formato proporciona una precisión de punto flotante de 16 bits en una representación de píxel más pequeña.

 

A partir Windows 8 y la actualización de plataforma [para Windows 7,](/windows/desktop/direct3darticles/platform-update-for-windows-7)WIC proporciona formatos adicionales, que se muestran en la tabla aquí.



| Nombre descriptivo                      | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formatos de píxeles de XEL

En la tabla siguiente se enumeran los formatos FORMAT proporcionados por WIC. Estos formatos separan los datos de color primario en canales de ánea (C), png (M), amarillo (Y) y negro (K).



| Nombre descriptivo                      | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppPIX      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppPIX      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCIALAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCIALAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formatos de píxeles de n canales

En la tabla siguiente se enumeran los formatos de n canales proporcionados por WIC. Estos formatos proporcionan una serie de canales de color no definidos para almacenar datos de imagen.



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



 

### <a name="alpha-only-pixel-formats"></a>Formatos de píxeles de solo alfa

En la tabla siguiente se enumeran los formatos de solo alfa proporcionados por WIC. Este formato solo contiene información alfa.



| Nombre descriptivo                 | Recuento de canales | Bits por canal | Bits por píxel | Tipo de almacenamiento |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formatos de píxeles Y'CbCr

En la tabla siguiente se enumeran los formatos Y'CbCr proporcionados por WIC. Estos formatos separan los datos de color principal en luma (Y), diferencia de color azul (Cb) y diferencia de choma rojo (Cr). Tenga en cuenta que estos formatos están diseñados para almacenar datos de píxeles jpeg JFIF Y'CbCr.



| Nombre descriptivo                 | Recuento de canales | Bits por píxel | Tipo de almacenamiento |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Espacio de color

Los formatos de píxel en sí no tienen un espacio de color. Por lo general, el espacio de color es una interpretación semántica de los valores de píxel que depende del contexto del mapa de bits. Algunas imágenes identifican un contexto de color que define el espacio de color de la imagen. Solo en ausencia de un contexto de color se debe inferir el espacio de color.

La interfaz [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para WIC define la información de contexto de color. Para recuperar la información de contexto de color de un marco de imagen, use el **método GetColorContext.**

En ausencia de información de espacio de color para una imagen, la regla general para la inferencia de espacio de color es que los formatos UINT RGB y escala de grises usan el espacio de colores RGB estándar (sRGB), mientras que los formatos RGB y escala de grises de punto fijo y de punto flotante usan el espacio de colores RGB extendido (scRGB). El modelo de color SPACE usa un espacio de colores RWOP.

## <a name="native-image-formats"></a>Formatos de imagen nativa

Cada uno de Windows códecs WIC proporcionados admite un subconjunto de los formatos de píxel wic. Para cada códec, los formatos de descodificación admitidos pueden ser diferentes de los formatos de codificación admitidos.

Al descodificar una imagen, si los datos se almacenan de forma nativa en un formato de píxel que no es compatible con el descodificador, se convertirá en un formato compatible. Para determinar el formato de píxel de salida, llame [**a IWICBitmapFrameDecode::GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Al codificar una imagen, use [**IWICBitmapFrameEncode::SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) para solicitar que el codificador use un formato de píxel específico. El codificador devolverá el formato de píxeles admitido más cercano, que puede ser diferente de lo que se solicitó.

En las tablas siguientes se muestran los formatos de píxeles admitidos por cada uno Windows códecs WIC proporcionados.

### <a name="bmp-native-codec"></a>Códec nativo BMP



| Descodificar formatos de píxel                   | Formatos de píxeles de codificador                   |
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
> EL \_ GUID WICPixelFormat32bppBGRA solo se admite en Windows 8, la actualización de plataforma [para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)y versiones posteriores.
>
> -   Para codificar a este formato, use la opción del codificador **EnableV5Header32bppBGRA.** Bmp se escribirá con un encabezado BITMAPV5HEADER.
> -   Si un archivo tiene bitmapV5HEADER, se descodifica como GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Códec nativo GIF



| Formatos de píxeles de descodificador           | Formatos de píxeles del codificador           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Códec nativo de ICO



| Formatos de píxeles de descodificador         | Formatos de píxeles del codificador |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Códec nativo JPEG



| Formatos de píxeles de descodificador         | Formatos de píxeles del codificador         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppPIX | GUID \_ WICPixelFormat32bppPIX |



 

### <a name="png-native-codec"></a>Códec nativo PNG



| Formatos de píxeles de descodificador           | Formatos de píxeles del codificador           |
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



| Formatos de píxeles de descodificador                | Formatos de píxeles del codificador           |
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
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppPIX   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppPIX        |                                 |
| GUID \_ WICPixelFormat40bppCIALAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppPIX        |                                 |
| GUID \_ WICPixelFormat80bppCIALAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> EL \_ GUID WICPixelFormat96bppRGBFloat solo se admite en Windows 8, la actualización de plataforma [para Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)y versiones posteriores.

 

### <a name="jpeg-xr-native-codec"></a>Códec nativo JPEG-XR



| Formatos de píxeles de descodificador                    | Formatos de píxeles del codificador                    |
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
| GUID \_ WICPixelFormat32bppPIX            | GUID \_ WICPixelFormat32bppPIX            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppYUN            | GUID \_ WICPixelFormat64bppYUN            |
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
| GUID \_ WICPixelFormat40bppALEAlpha       | GUID \_ WICPixelFormat40bppALEAlpha       |
| GUID \_ WICPixelFormat80bppALEAlpha       | GUID \_ WICPixelFormat80bppALEAlpha       |
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



 

## <a name="dds-native-codec"></a>Códec nativo DDS



| Formatos de píxeles de descodificador          | Formatos de píxeles del codificador          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> El códec Windows DDS proporcionado admite archivos DDS codificados con los siguientes valores \_ DE FORMATO DXGI:

 

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   DXGI \_ FORMAT \_ BC3 \_ UNORM

Se descodifican y codifican como \_ GUID WICPixelFormat32bppBGRA o GUID \_ WICPixelFormat32bppPBGRA. Para obtener más información, vea Información [general sobre el formato DDS.](dds-format-overview.md)

## <a name="pixel-format-extensibility"></a>Extensibilidad del formato de píxel

Los formatos de imagen personalizados pueden usar formatos de píxeles que WIC no proporciona de forma nativa, como YCbCr (YUV) y YCCK (Y/Cb/Cr/K). WIC proporciona un modelo de extensibilidad que permite que los formatos de píxeles integrados y de complemento funcionen dentro de la misma canalización de creación de imágenes. Para integrar estos formatos de píxel con la canalización de creación de imágenes de WIC, debe crear convertidores de formato de píxeles para convertir los formatos de píxel del complemento en uno o varios de los formatos de píxel nativos. La interfaz principal para compilar convertidores de formato es [**IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUID y CLID de WIC](-wic-guids-clsids.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
