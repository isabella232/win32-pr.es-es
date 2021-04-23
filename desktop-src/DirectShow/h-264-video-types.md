---
description: Tipos de vídeo H.264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H.264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909023"
---
# <a name="h264-video-types"></a>Tipos de vídeo H.264

Los siguientes subtipos multimedia se definen para el vídeo H.264.



| Subtype                | FOURCC | Descripción                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | 'AVC1' | Secuencia de bits H.264 sin códigos de inicio.                           |
| **MEDIASUBTYPE \_ H264** | 'H264' | Secuencia de bits H.264 con códigos de inicio.                              |
| **MEDIASUBTYPE \_ h264** | 'h264' | Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente. |
| **MEDIASUBTYPE \_ X264** | 'X264' | Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente. |



 

Estos GUID de subtipo se declaran en wmcodecdsp.h.

La principal diferencia entre estos tipos de medios es la presencia de códigos de inicio en la secuencia de bits. Si el subtipo es **MEDIASUBTYPE \_ AVC1,** la secuencia de bits no contiene códigos de inicio.

### <a name="h264-bitstream-with-start-codes"></a>Secuencia de bits H.264 con códigos de inicio

Las secuencias de bits H.264 que se transmiten a través del aire, que se encuentran en secuencias de transporte o programas MPEG-2, o que se graban en HD-DVD, tienen el formato descrito en el anexo B de ITU-T Rec. H.264. Según esta especificación, el flujo de bits consta de una secuencia de unidades de capa de abstracción de red (NALUs), cada una de las cuales tiene un prefijo de código de inicio igual a 0x000001 o 0x00000001.

Cuando los códigos de inicio están presentes en la secuencia de bits, se usa el siguiente tipo de medio:



| Etiqueta | Value |
|-------------|---------------------------------------------------------------------------------------------------|
| Tipo principal  | **VÍDEO \_ MEDIATYPE**                                                                              |
| Subtipos    | **MEDIASUBTYPE \_ H264,** **MEDIASUBTYPE \_ h264,** **MEDIASUBTYPE \_ X264** o **MEDIASUBTYPE \_ x264** |
| Tipo de formato | **FORMAT \_ VideoInfo,** **FORMAT \_ VideoInfo2,** **FORMAT \_ MPEG2Video** o **GUID \_ NULL**          |



 

Si el tipo de formato es **GUID \_ NULL,** no hay ninguna estructura de formato presente.

Cuando la secuencia de bits contiene códigos de inicio, cualquiera de los tipos de formato enumerados aquí es suficiente, ya que el descodificador no requiere ninguna información adicional para analizar la secuencia. El flujo de bits ya contiene toda la información necesaria para el descodificador y los códigos de inicio permiten al descodificador localizar el inicio de cada NALU.

Los subtipos siguientes son equivalentes:

### <a name="h264-bitstream-without-start-codes"></a>Secuencia de bits H.264 sin códigos de inicio

El formato de contenedor MP4 almacena datos H.264 sin códigos de inicio. En su lugar, cada NALU tiene el prefijo de un campo de longitud, que proporciona la longitud de NALU en bytes. El tamaño del campo de longitud puede variar, pero normalmente es de 1, 2 o 4 bytes.

Cuando los códigos de inicio no están presentes en la secuencia de bits, se usa el siguiente tipo de medio.



| Etiqueta | Value |
|-------------|------------------------|
| Tipo principal  | **Vídeo \_ DE MEDIATYPE**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| Tipo de formato | **FORMAT \_ MPEG2Video** |



 

El bloque de formato es una [**estructura MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) Esta estructura debe rellenarse de la siguiente manera:

-   **hdr:** estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que describe la secuencia de bits. No hay ninguna tabla de colores después de [**la parte BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la estructura y **biClrUsed** debe ser cero.
-   **dwStartTimeCode:** no se usa. Establecer en cero.
-   **cbSequenceHeader:** longitud de la **matriz dwSequenceHeader** en bytes.
-   **dwProfile:** especifica el perfil H.264.
-   **dwLevel:** especifica el nivel H.264.
-   **dwFlags:** número de bytes usados para el campo de longitud que aparece antes de cada **NALU.** El campo length indica el tamaño del siguiente NALU en bytes. Por ejemplo, si **dwFlags** es 4, cada NALU va precedida de un campo de longitud de 4 bytes. Los valores válidos son 1, 2 y 4.
-   **dwSequenceHeader:** matriz de bytes que puede contener NALUs de conjunto de parámetros de secuencia (SPS) y conjunto de parámetros de imagen (PPS).

El contenedor MP4 puede contener conjuntos de parámetros de secuencia (SPS) o conjuntos de parámetros de imagen (PPS) como unidades NAL especiales en encabezados de archivo o en una secuencia independiente (distinta de la secuencia de vídeo). Cuando se establece el formato, el tipo de medio puede especificar unidades SPS y PPS NAL en la **matriz dwSequenceHeader.** Si **cbSequenceHeader** es mayor que cero, **dwSequenceHeader** es el inicio de una matriz de bytes que contiene SPS y PPS NALUs, delimitado por campos de longitud de 2 bytes, todos en orden de bytes de red (big-endian). Es posible tener SPS y PPS, solo uno de estos tipos o ninguno. El tipo real de cada NALU se puede determinar examinando el campo de tipo de unidad **nal \_ \_** del propio NALU.

Cuando se usa este tipo de medio, cada ejemplo multimedia se inicia al principio de una NALU y las unidades NAL no abarcan muestras. Esto permite al descodificador recuperarse de datos dañados o ejemplos eliminados.

 

 



