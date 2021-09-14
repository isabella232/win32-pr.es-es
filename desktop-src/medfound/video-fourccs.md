---
description: Vídeo FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Vídeo FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363638"
---
# <a name="video-fourccs"></a>Vídeo FOURCCs

Muchos formatos de vídeo tienen asignados códigos FOURCC. Un código FOURCC es un entero de 32 bits sin signo que se crea concatenando cuatro caracteres ASCII. Por ejemplo, el código FOURCC para el vídeo YUY2 es "YUY2".

Se definen varias macros de C/C++ para declarar valores FOURCC en el código fuente. La **macro MAKEFOURCC** se define en Mmsystem.h y la macro **de FCC** se define en Aviriff.h y en otros archivos de encabezado. También puede declarar un código FOURCC directamente como literal de cadena simplemente invirtiendo el orden de los caracteres. Por lo tanto, las siguientes instrucciones son equivalentes:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

(En el último ejemplo, es necesario invertir el orden de bytes porque Windows usa una arquitectura little-endian. 'Y' = 0x59, 'U' = 0x55 y '2' = 0x32, por lo que '2YUY' es 0x32595559).

Algunas de las API de aceleración de vídeo [2.0](directx-video-acceleration-2-0.md) de DirectX usan un valor **D3DFORMAT** para describir un formato de vídeo. También se puede usar un código FOURCC en este contexto:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Constantes FOURCC

En la tabla siguiente se enumeran algunos códigos FOURCC comunes.



| Valor FOURCC | Descripción                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| 'H264'       | Vídeo de H.264.                                                                                                          |
| 'I420'       | Vídeo YUV almacenado en formato plano 4:2:0.                                                                              |
| 'IYUV'       | Vídeo YUV almacenado en formato plano 4:2:0.                                                                              |
| 'M4S2'       | Vídeo MPEG-4, parte 2.                                                                                                  |
| 'MP4S'       | Códec Mpeg 4 de Microsoft versión 3. Este códec ya no se admite.                                                  |
| 'MP4V'       | Vídeo MPEG-4, parte 2.                                                                                                  |
| 'MPG1'       | Vídeo MPEG-1.                                                                                                         |
| 'MSS1'       | Contenido codificado con el códec de pantalla Windows Media Video 7.                                                          |
| 'MSS2'       | Contenido codificado con el códec de pantalla Windows Media Video 9.                                                          |
| 'UYVY'       | Vídeo YUV almacenado en formato empaquetado 4:2:2. Similar a YUY2, pero con una ordenación de datos diferente.                         |
| 'WMV1'       | Contenido codificado con el códec Windows Media Video 7.                                                                 |
| 'WMV2'       | Contenido codificado con el códec Windows Media Video 8.                                                                 |
| 'WMV3'       | Contenido codificado con el códec Windows Media Video 9.                                                                 |
| 'WMVA'       | Contenido codificado con la versión anterior y obsoleta del códec de perfil avanzado Windows Media Video 9.                 |
| 'WMVP'       | Contenido codificado con el códec Windows imagen de Media Video 9.1.                                                         |
| 'WVC1'       | SMPTE 421M ("VC-1"). Contenido codificado con Windows perfil avanzado de Media Video 9.                                     |
| 'WVP2'       | Contenido codificado con el códec Windows imagen v2 de Media Video 9.1.                                                      |
| 'YUY2'       | Vídeo YUV almacenado en formato empaquetado 4:2:2.                                                                              |
| 'YV12'       | Vídeo YUV almacenado en formato plano 4:2:0 o 4:1:1. Idéntico a I420/IYUV, salvo que los planos you y V se cambian. |
| 'YVU9'       | Vídeo de YUV almacenado en formato plano 16:1:1.                                                                             |
| 'YVYU'       | Vídeo YUV almacenado en formato empaquetado 4:2:2. Similar a YUY2, pero con una ordenación de datos diferente.                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 



