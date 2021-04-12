---
description: Vídeo FOURCCs
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: Vídeo FOURCCs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360569"
---
# <a name="video-fourccs"></a>Vídeo FOURCCs

Muchos formatos de vídeo tienen códigos FOURCC asignados. Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII. Por ejemplo, el código FOURCC del vídeo YUY2 es "YUY2".

Se definen varias macros de C/C++ para declarar valores FOURCC en el código fuente. La macro **MAKEFOURCC** se define en mmsystem. h y la macro **FCC** se define en Aviriff. h y otros archivos de encabezado. También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres. Por lo tanto, las siguientes instrucciones son equivalentes:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

(En el último ejemplo, se requiere invertir el orden de los bytes porque Windows utiliza una arquitectura little-endian. ' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559).

Algunas de las API de [DirectX video Acceleration 2,0](directx-video-acceleration-2-0.md) usan un valor de **D3DFORMAT** para describir un formato de vídeo. También se puede utilizar un código FOURCC en este contexto:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Constantes FOURCC

En la tabla siguiente se enumeran algunos códigos FOURCC comunes.



| Valor FOURCC | Descripción                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| H264       | Vídeo H. 264.                                                                                                          |
| 'I420'       | Vídeo YUV almacenado en formato 4:2:0 plano.                                                                              |
| 'IYUV'       | Vídeo YUV almacenado en formato 4:2:0 plano.                                                                              |
| ' M 4S2 '       | Vídeo MPEG-4 parte 2.                                                                                                  |
| MP4       | Códec Microsoft MPEG 4 versión 3. Este códec ya no se admite.                                                  |
| MP4V       | Vídeo MPEG-4 parte 2.                                                                                                  |
| 'MPG1'       | Vídeo MPEG-1.                                                                                                         |
| 'MSS1'       | Contenido codificado con el códec de pantalla Windows Media Video 7.                                                          |
| 'MSS2'       | Contenido codificado con el códec de pantalla de Windows Media Video 9.                                                          |
| UYVY       | Vídeo YUV almacenado en formato 4:2:2 empaquetado. Similar a YUY2, pero con diferente orden de datos.                         |
| 'WMV1'       | Contenido codificado con el códec Windows Media Video 7.                                                                 |
| 'WMV2'       | Contenido codificado con el códec Windows Media Video 8.                                                                 |
| 'WMV3'       | Contenido codificado con el códec Windows Media Video 9.                                                                 |
| 'WMVA'       | Contenido codificado con la versión antigua obsoleta del códec de perfil avanzado de Windows Media Video 9.                 |
| 'WMVP'       | Contenido codificado con el códec de imagen Windows Media Video 9,1.                                                         |
| 'WVC1'       | SMPTE 421M ("VC-1"). Contenido codificado con el perfil avanzado de Windows Media Video 9.                                     |
| 'WVP2'       | Contenido codificado con el códec Windows Media Video 9,1 Image V2.                                                      |
| YUY2       | Vídeo YUV almacenado en formato 4:2:2 empaquetado.                                                                              |
| 'YV12'       | Vídeo YUV almacenado en formato planar 4:2:0 o 4:1:1. Es idéntico a i420/IYUV, salvo que se cambian los planos usted y V. |
| YVU9       | Vídeo YUV almacenado en formato 16:1:1 plano.                                                                             |
| YVYU       | Vídeo YUV almacenado en formato 4:2:2 empaquetado. Similar a YUY2, pero con diferente orden de datos.                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[GUID de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 



