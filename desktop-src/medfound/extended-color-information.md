---
description: Información de color ampliada
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Información de color ampliada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ba43180a0f1e5253540088c1638f59d52380c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808083"
---
# <a name="extended-color-information"></a>Información de color ampliada

Si sabe algo sobre el color RGB, sabe que (255, 255, 255) es el tripledo RGB de 8 bits para el color *blanco*. Pero, ¿cuál es el *color* real definido por este triple?

La respuesta puede ser sorprendente: sin información adicional, este triple no define ningún color determinado. El significado de cualquier valor RGB depende del *espacio de colores*. Si no se conoce el espacio de colores, entonces hablaremos de que no sabemos el color.

Un espacio de colores define cómo se debe reproducir la representación numérica de un valor de color determinado como luz física. Cuando el vídeo se codifica en un espacio de colores, pero se muestra en otro, los colores se distorsionan, a menos que el vídeo se corrija por color. Para lograr una fidelidad de color precisa, por lo tanto, es fundamental conocer el espacio de colores del vídeo de origen. Anteriormente, la canalización de vídeo en Windows no incluía información sobre el espacio de colores previsto. A partir de Windows Vista, tanto DirectShow como Media Foundation admiten la información de color extendida en el tipo de medio. Esta información también está disponible para DirectX video Acceleration (DXVA).

La manera estándar de describir un espacio de colores matemáticamente es usar el espacio de color de CIE XYZ, definido por la Comisión Internacional en iluminación (CIE). No es práctico usar valores de CIE XYZ directamente en el vídeo, pero el espacio de colores de CIE XYZ se puede usar como una representación intermedia al convertir entre espacios de colores.

Para reproducir los colores con precisión, se necesita la siguiente información:

-   Primarios de color. Las principales colores definen cómo se representan los valores de los triestímulos de CIE XYZ como componentes RGB. En efecto, los valores primarios de color definen el "significado" de un valor RGB determinado.
-   Función de transferencia. La función de transferencia es una función que convierte valores RGB lineales en valores de R'G'B no lineales. Esta función también se denomina *corrección Gamma*.
-   Matriz de transferencia. La matriz de transferencia define cómo se convierte R'G'B ' en Y'PbPr.
-   Muestreo de croma. La mayoría del vídeo YUV se transmite con menos resolución en los componentes de croma que la luminancia. El muestreo de croma se indica mediante el FOURCC del formato de vídeo. Por ejemplo, YUY2 es un formato 4:2:2, lo que significa que las muestras de croma se muestrean horizontalmente en un factor de 2.
-   Croma en el emplazamiento. Cuando se muestrea el croma, la posición de los ejemplos de croma relativa a las muestras de luminancia determina cómo se deben interpolar las muestras que faltan.
-   Intervalo nominal. El intervalo nominal define cómo se escalan los valores de Y'PbPr a Y'CbCr.

## <a name="color-space-in-media-types"></a>Espacio de colores en tipos de medios

DirectShow, Media Foundation y la aceleración de vídeo de DirectX (DXVA) tienen diferentes formas de representar formatos de vídeo. Afortunadamente, es fácil traducir la información del espacio de colores de una a otra, ya que las enumeraciones correspondientes son las mismas.

-   DXVA 1,0: se proporciona información sobre el espacio de colores en la estructura de [**DXVA \_ ExtendedFormat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) .
-   DXVA 2,0: se proporciona información sobre el espacio de colores en la estructura de estructura de [**DXVA2 \_ ExtendedFormat**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) . Esta estructura es idéntica a la estructura DXVA 1,0 y el significado de los campos es el mismo.
-   DirectShow: se proporciona información sobre el espacio de colores en la estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . La información se almacena en los 24 bits superiores del campo **dwControlFlags** . Si hay información de espacio de color, establezca la marca **AMCONTROL \_ COLORINFO \_ present** en **dwControlFlags**. Cuando se establece esta marca, el campo **dwControlFlags** debe interpretarse como una estructura de [**DXVA \_ ExtendedFormat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) , salvo que los 8 bits inferiores de la estructura están reservados para las marcas **AMCONTROL \_ XXX** .
-   Controladores de captura de vídeo: se proporciona información sobre el espacio de colores en la estructura de [**KS \_ VIDEOINFOHEADER2**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) . Esta estructura es idéntica a la estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) y el significado de los campos es el mismo.
-   Media Foundation: la información del espacio de colores se almacena como atributos en el tipo de medio:

    

    | Información de color  | Atributo                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Primarios de color    | [**\_ \_ primarios de vídeo MF MT \_**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Transfer (función)  | [**MF \_ MT \_ Transfer ( \_ función)**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matriz de transferencia    | [**MF \_ MT \_ YUV \_ Matrix**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Submuestreo de croma | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)<br/> (Proporcionado por el FOURCC, que se almacena en el primer **valor DWORD** del GUID del subtipo).<br/> |
    | Croma en el emplazamiento      | [**vídeo croma de MF MT en el \_ \_ \_ \_ emplazamiento**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Rango nominal      | [**\_ \_ \_ rango nominal de vídeo \_ de MF MT**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversión de espacio de colores

La conversión de un espacio de Y'CbCr a otro requiere los pasos siguientes.

1.  Cuantificación inversa: convierta la representación Y'CbCr en una representación Y'PbPr mediante el intervalo nominal de origen.
2.  Muestreo: convierta los valores de croma muestreados en 4:4:4 mediante la interpolación de valores de croma.
3.  Conversión de YUV a RGB: convertir de Y'PbPr a R'G'B no lineal ', usando la matriz de transferencia de origen.
4.  Función de transferencia inversa: convierte R'G'B no lineal en RGB lineal, mediante el inverso de la función de transferencia.
5.  Conversión de espacio de colores RGB: Use los primarios de color para convertir el espacio RGB de origen en el espacio RGB de destino.
6.  Función de transferencia: convertir RGB lineal en R'G'B no lineales con la función de transferencia de destino.

7.  Conversión de RGB a YUV: convierta R'G'B en Y'PbPr con la matriz de transferencia de destino.
8.  Disminución de resolución: convierta 4:4:4 a 4:2:2, 4:2:0 o 4:1:1 filtrando los valores de croma.
9.  Cuantificación: convierta Y'PbPr en Y'CbCr con el intervalo nominal de destino.

Los pasos 1 a 4 se producen en el espacio de colores de origen y los pasos 6 a 9 se producen en el espacio de colores de destino. En la implementación real, se pueden aplicar pasos intermedios y se pueden combinar pasos adyacentes. Por lo general, hay un equilibrio entre la precisión y el costo computacional.

Por ejemplo, para realizar la conversión de RT. 601 a RT. 709, se requieren las siguientes fases:

-   Cuantificación inversa: Y'CbCr (601) a Y'PbPr (601)
-   Muestreo: Y'PbPr (601)
-   YUV a RGB: Y'PbPr (601) a R'G'B ' (601)
-   Función de transferencia inversa: R'G'B ' (601) a RGB (601)
-   Conversión de espacio de colores RGB: RGB (601) a RGB (709)
-   Función de transferencia: RGB (709) a R'G'B ' (709)
-   RGB a YUV: R'G'B ' (709) a Y'PbPr (709)
-   Disminución de resolución: Y'PbPr (709)

-   Cuantificación: Y'PbPr (709) a Y'CbCr (709)

## <a name="using-extended-color-information"></a>Usar información de color extendida

Para conservar la fidelidad de color a lo largo de la canalización, la información del espacio de colores debe introducirse en el origen o en el descodificador y transmitirse todo el camino a través de la canalización al receptor.

### <a name="video-capture-devices"></a>Dispositivos de captura de vídeo

La mayoría de los dispositivos de captura analógicos usan un espacio de colores bien definido al capturar vídeo. Los controladores de captura deben ofrecer un formato con un bloque de formato **KS \_ VIDEOINFOHEADER2** que contiene la información de color. Por compatibilidad con versiones anteriores, el controlador debe aceptar formatos que no contengan la información de color. Esto permitirá que el controlador funcione con componentes que no acepten la información de color ampliada.

### <a name="file-based-sources"></a>Orígenes basados en archivos

Al analizar un archivo de vídeo, el origen del medio (o el filtro del analizador, en DirectShow) podría proporcionar parte de la información de color. Por ejemplo, el navegador de DVD puede determinar el espacio de color basado en el contenido del DVD. Puede haber otra información de color disponible para el descodificador. Por ejemplo, una secuencia de vídeo MPEG-2 elemental proporciona la información de color en el \_ campo extensión de visualización de secuencia \_ . Si la información de color no se describe explícitamente en el origen, podría estar definida implícitamente por el tipo de contenido. Por ejemplo, las variedades NTSC y PAL de vídeo DV usan diferentes espacios de color. Por último, el descodificador puede utilizar cualquier información de color que obtenga del tipo de medio del origen.

### <a name="other-components"></a>Otros componentes

Es posible que otros componentes necesiten usar la información del espacio de colores en un tipo de medio:

-   Los convertidores de espacio de colores de software deben usar información de espacio de colores al seleccionar un algoritmo de conversión.
-   Los mezcladores de vídeo, como el mezclador de representador de vídeo mejorado (EVR), deben usar la información de color al mezclar flujos de vídeo de distintos tipos de contenido.
-   Las API de procesamiento de vídeo de DXVA y DDIs permiten al llamador especificar información de espacio de colores. La GPU debe usar esta información cuando realiza la combinación de vídeos de hardward.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
