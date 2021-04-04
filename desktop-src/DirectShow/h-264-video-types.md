---
description: Tipos de vídeo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997628"
---
# <a name="h264-video-types"></a>Tipos de vídeo H. 264

Los siguientes subtipos de medios se definen para el vídeo H. 264.



| Subtype                | FOURCC | Descripción                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ avc1** | 'AVC1' | H. 264 fragmentada sin códigos de inicio.                           |
| **MEDIASUBTYPE \_ H264** | H264 | H. 264 fragmentada con códigos de inicio.                              |
| **MEDIASUBTYPE \_ H264** | H264 | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente. |
| **MEDIASUBTYPE \_ x264** | 'X264' | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente. |



 

Estos GUID de subtipos se declaran en wmcodecdsp. h.

La diferencia principal entre estos tipos de medios es la presencia de códigos de inicio en el fragmentada. Si el subtipo es **MEDIASUBTYPE \_ avc1**, el fragmentada no contiene códigos de inicio.

### <a name="h264-bitstream-with-start-codes"></a>H. 264 fragmentada con códigos de inicio

Los bitstreams de H. 264 que se transmiten a través del aire o que se encuentran en flujos de programa o transporte MPEG-2, o grabados en HD-DVD, se formatean como se describe en el Anexo B de ITU-T Rec. H. 264. Según esta especificación, fragmentada consta de una secuencia de unidades de capa de abstracción de red (NALUs), cada una de las cuales tiene como prefijo un código de inicio igual a 0x000001 o 0x00000001.

Cuando los códigos de inicio están presentes en fragmentada, se usa el siguiente tipo de medio:



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| Tipo principal  | **Vídeo de MEDIATYPE \_**                                                                              |
| Subtipos    | **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** o **MEDIASUBTYPE \_ x264** |
| Tipo de formato | **Formato \_ Videoinfo**, **format \_ VideoInfo2**, **format \_ MPEG2Video** o **GUID \_ null**          |



 

Si el tipo de formato es **GUID \_ null**, no hay ninguna estructura de formato presente.

Cuando fragmentada contiene códigos de inicio, cualquiera de los tipos de formato enumerados aquí es suficiente, porque el descodificador no requiere ninguna información adicional para analizar la secuencia. El fragmentada ya contiene toda la información que necesita el descodificador y los códigos de inicio permiten al descodificador localizar el inicio de cada NALU.

Los siguientes subtipos son equivalentes:

### <a name="h264-bitstream-without-start-codes"></a>H. 264 fragmentada sin códigos de inicio

El formato de contenedor MP4 almacena datos de H. 264 sin códigos de inicio. En su lugar, cada NALU tiene como prefijo un campo de longitud, que proporciona la longitud de NALU en bytes. El tamaño del campo de longitud puede variar, pero suele ser de 1, 2 o 4 bytes.

Cuando los códigos de inicio no están presentes en fragmentada, se usa el siguiente tipo de medio.



|             |                        |
|-------------|------------------------|
| Tipo principal  | **Vídeo de MEDIATYPE \_**   |
| Subtype     | **MEDIASUBTYPE \_ avc1** |
| Tipo de formato | **FORMATO \_ MPEG2Video** |



 

El bloque Format es una estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) . Esta estructura se debe rellenar de la siguiente manera:

-   **HDR**: una estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que describe el fragmentada. No hay ninguna tabla de colores presente después de la parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la estructura y **biClrUsed** debe ser cero.
-   **dwStartTimeCode**: no se usa. Establecer en cero.
-   **cbSequenceHeader**: la longitud de la matriz de **dwSequenceHeader** en bytes.
-   **dwProfile**: especifica el perfil H. 264.
-   **dwLevel**: especifica el nivel H. 264.
-   **dwFlags**: el número de bytes usados para el campo de longitud que aparece antes de cada **Nalu**. El campo de longitud indica el tamaño de los siguientes NALU en bytes. Por ejemplo, si **dwFlags** es 4, cada Nalu va precedido de un campo de longitud de 4 bytes. Los valores válidos son 1, 2 y 4.
-   **dwSequenceHeader**: una matriz de bytes que puede contener el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.

El contenedor MP4 podría contener conjuntos de parámetros de secuencia (SPS) o conjuntos de parámetros de imagen (PPS) como unidades NAL especiales en encabezados de archivo o en una secuencia independiente (distinta de la secuencia de vídeo). Cuando se establece el formato, el tipo de medio puede especificar las unidades de SPS y de PPS NAL en la matriz **dwSequenceHeader** . Si **cbSequenceHeader** es mayor que cero, **dwSequenceHeader** es el inicio de una matriz de bytes que contiene SPS y PPS NALUs, delimitado por campos de longitud de 2 bytes, todo ello en el orden de bytes de la red (Big-endian). Es posible tener SPS y PPS, solo uno de estos tipos, o ninguno. El tipo real de cada NALU se puede determinar mediante el examen del campo de **\_ \_ tipo de unidad nal** del mismo Nalu.

Cuando se usa este tipo de medio, cada ejemplo multimedia se inicia al principio de un NALU y las unidades NAL no abarcan los ejemplos. Esto permite que el descodificador se recupere de los datos dañados o ejemplos quitados.

 

 



