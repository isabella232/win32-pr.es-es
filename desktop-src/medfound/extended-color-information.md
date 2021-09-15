---
description: Información de color extendida
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Información de color extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ba43180a0f1e5253540088c1638f59d52380c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466908"
---
# <a name="extended-color-information"></a>Información de color extendida

Si sabe algo sobre el color RGB, sabe que (255, 255, 255) es el triplete RGB de 8 bits para el color *blanco*. Pero, ¿cuál es el *color real* definido por este triplete?

La respuesta puede ser sorprendente: sin información adicional, este triplete no define ningún color determinado. El significado de cualquier valor RGB depende del *espacio de color*. Si no se conoce el espacio de color, en sentido estricto, no se conoce el color.

Un espacio de color define cómo se debe reproducir la representación numérica de un valor de color determinado como luz física. Cuando el vídeo se codifica en un espacio de colores pero se muestra en otro, da como resultado colores distorsionados, a menos que el vídeo se corrija por colores. Por lo tanto, para lograr una fidelidad de color precisa, es fundamental conocer el espacio de color del vídeo de origen. Anteriormente, la canalización de vídeo de Windows no tenía información sobre el espacio de color previsto. A partir Windows Vista, tanto DirectShow como Media Foundation información de color extendida en el tipo de medio. Esta información también está disponible para la aceleración de vídeo de DirectX (DXVA).

La manera estándar de describir matemáticamente un espacio de color es usar el espacio de colores XYZ de CIE, definido por la International Commission on Desaprobación (CIE). No es práctico usar valores XYZ de CIE directamente en vídeo, pero el espacio de colores XYZ de CIE se puede usar como una representación intermedia al convertir entre espacios de colores.

Para reproducir los colores con precisión, se necesita la siguiente información:

-   Color principal. Los elementos principales de color definen cómo se representan los valores tmulus de CIE XYZ como componentes RGB. En efecto, las primarias de color definen el "significado" de un valor RGB determinado.
-   Función de transferencia. La función de transferencia es una función que convierte los valores RGB lineales en valores no lineales de R'G'B'. Esta función también se denomina *corrección gamma.*
-   Matriz de transferencia. La matriz de transferencia define cómo R'G'B' se convierte a Y'PbPr.
-   Muestreo de muestreo de muestreo. La mayoría de los vídeos de YUV se transmiten con menos resolución en los componentes de los componentes de la zona que el luma. El muestreo de muestreo se indica mediante el FOURCC del formato de vídeo. Por ejemplo, YUY2 es un formato 4:2:2, lo que significa que las muestras de muestras se muestrean horizontalmente por un factor de 2.
-   Siting de croma. Cuando se muestrea el brillo, la posición de las muestras de muestreo con respecto a las muestras de luma determina cómo se deben interpolar las muestras que faltan.
-   Intervalo nominal. El intervalo nominal define cómo se escalan los valores de Y'PbPr a Y'CbCr.

## <a name="color-space-in-media-types"></a>Espacio de color en tipos de medios

DirectShow, Media Foundation y aceleración de vídeo de DirectX (DXVA) tienen distintas maneras de representar formatos de vídeo. Afortunadamente, es fácil traducir la información de espacio de color de una a otra, porque las enumeraciones pertinentes son las mismas.

-   DXVA 1.0: la información de espacio de color se proporciona en la [**estructura \_ DXVA ExtendedFormat.**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat)
-   DXVA 2.0: la información de espacio de color se proporciona en la estructura [**de estructura \_ DXVA2 ExtendedFormat.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) Esta estructura es idéntica a la estructura DXVA 1.0 y el significado de los campos es el mismo.
-   DirectShow: la información de espacio de color se proporciona en la [**estructura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) La información se almacena en los 24 bits superiores del **campo dwControlFlags.** Si hay información de espacio de colores, establezca la marca **AMCONTROL \_ COLORINFO \_ PRESENT** en **dwControlFlags.** Cuando se establece esta marca, el campo **dwControlFlags** debe interpretarse como una estructura [**\_ ExtendedFormat de DXVA,**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) salvo que los 8 bits inferiores de la estructura están reservados para las marcas **\_ XXX de AMCONTROL.**
-   Controladores de captura de vídeo: la información de espacio de color se proporciona en la [**estructura \_ VIDEOINFOHEADER2 de KS.**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) Esta estructura es idéntica a la [**estructura VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) y el significado de los campos es el mismo.
-   Media Foundation: la información de espacio de color se almacena como atributos en el tipo de medio:

    

    | Información de color  | Atributo                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Color principal    | [**VÍDEO PRINCIPAL DE MF \_ MT \_ \_**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Función de transferencia  | [**MF \_ MT \_ TRANSFER \_ (FUNCIÓN)**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matriz de transferencia    | [**MF \_ MT \_ YUV \_ MATRIX**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Submuestreo de croma | [**SUBTIPO \_ MT DE MF \_**](mf-mt-subtype-attribute.md)<br/> (Dado por FOURCC, que se almacena en el primer **DWORD** del GUID del subtipo).<br/> |
    | Siting (Siting)      | [**SITING \_ DE \_ VÍDEO \_ MF MT \_**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Rango nominal      | [**RANGO \_ \_ NOMINAL DE VÍDEO MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversión de espacio de color

La conversión de un espacio Y'CbCr a otro requiere los pasos siguientes.

1.  Cuantificación inversa: convierta la representación Y'CbCr en una representación Y'PbPr, mediante el intervalo nominal de origen.
2.  Upsampling: convierta los valores muestreados a 4:4:4 mediante la interpolación de los valores de los colores.
3.  Conversión de YUV a RGB: convierta de Y'PbPr a R'G'B no lineal' mediante la matriz de transferencia de origen.
4.  Función de transferencia inversa: convierta R'G'B' no lineal en RGB lineal, usando el inverso de la función de transferencia.
5.  Conversión de espacio de color RGB: use las primarias de color para convertir del espacio RGB de origen al espacio RGB de destino.
6.  Función de transferencia: convierta RGB lineal en R'G'B no lineal, mediante la función de transferencia de destino.

7.  Conversión RGB a YUV: convierta R'G'B' a Y'PbPr, mediante la matriz de transferencia de destino.
8.  Downsampling: convierta 4:4:4 a 4:2:2, 4:2:0 o 4:1:1 mediante el filtrado de los valores de los trastos.
9.  Cuantificación: convierta Y'PbPr en Y'CbCr, mediante el intervalo nominal de destino.

Los pasos 1 a 4 se producen en el espacio de color de origen y los pasos 6 a 9 se producen en el espacio de color de destino. En la implementación real, los pasos intermedios se pueden aproximar y se pueden combinar los pasos adyacentes. Por lo general, hay un equilibrio entre la precisión y el costo computacional.

Por ejemplo, para convertir RT.601 a RT.709 se necesitan las siguientes fases:

-   Cuantificación inversa: Y'CbCr(601) a Y'PbPr(601)
-   Upsampling: Y'PbPr(601)
-   YUV a RGB: Y'PbPr(601) a R'G'B'(601)
-   Función de transferencia inversa: R'G'B'(601) a RGB(601)
-   Conversión de espacios de color RGB: RGB(601) a RGB(709)
-   Función de transferencia: RGB(709) a R'G'B'(709)
-   RGB a YUV: R'G'B'(709) a Y'PbPr(709)
-   Downsampling: Y'PbPr(709)

-   Cuantificación: Y'PbPr(709) a Y'CbCr(709)

## <a name="using-extended-color-information"></a>Uso de información de color extendida

Para conservar la fidelidad del color en toda la canalización, la información de espacio de color debe introducirse en el origen o el descodificador y transmitirse hasta el receptor a través de la canalización.

### <a name="video-capture-devices"></a>Dispositivos de captura de vídeo

La mayoría de los dispositivos de captura análogos usan un espacio de colores bien definido al capturar vídeo. Los controladores de captura deben ofrecer un formato con un bloque de formato **\_ VIDEOINFOHEADER2** de KS que contenga la información de color. Por compatibilidad con versiones anteriores, el controlador debe aceptar formatos que no contengan la información de color. Esto permitirá que el controlador funcione con componentes que no aceptan la información de color extendida.

### <a name="file-based-sources"></a>Orígenes basados en archivos

Al analizar un archivo de vídeo, el origen multimedia (o filtro del analizador, en DirectShow) podría proporcionar parte de la información de color. Por ejemplo, el navegador de DVD puede determinar el espacio de color en función del contenido del DVD. Es posible que haya otra información de color disponible para el descodificador. Por ejemplo, una secuencia de vídeo elemental MPEG-2 proporciona la información de color en el campo de extensión \_ de \_ visualización de secuencia. Si la información de color no se describe explícitamente en el origen, el tipo de contenido podría definirla implícitamente. Por ejemplo, las variedades ÁLISIS y PAL de vídeo DV usan espacios de color diferentes. Por último, el descodificador puede usar la información de color que obtiene del tipo de medio del origen.

### <a name="other-components"></a>Otros componentes

Es posible que otros componentes necesiten usar la información de espacio de color en un tipo de medio:

-   Los convertidores de espacio de colores de software deben usar información de espacio de color al seleccionar un algoritmo de conversión.
-   Los mezcladores de vídeo, como el mezclador de representador de vídeo mejorado (EVR), deben usar la información de color al mezclar secuencias de vídeo de diferentes tipos de contenido.
-   Las API de procesamiento de vídeo DXVA y los DDIs permiten al autor de la llamada especificar información de espacio de color. La GPU debe usar esta información cuando realice mezclas de vídeo de entrada dura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
