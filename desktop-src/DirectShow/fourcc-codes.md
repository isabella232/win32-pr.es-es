---
description: Códigos FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Códigos FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25820d21fb8e8386fb11816c373debf427fa783b8a2f2d4723a46e689e6aea0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043325"
---
# <a name="fourcc-codes"></a>Códigos FOURCC

Muchos formatos de medios digitales tienen códigos FOURCC asignados. Un código FOURCC es un entero de 32 bits sin signo que se crea concatenando cuatro caracteres ASCII. Por ejemplo, el código FOURCC para el vídeo YUY2 es "YUY2". En el caso de los formatos de vídeo comprimidos y los formatos de vídeo no RGB (como YUV), el miembro **biCompression** de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) debe establecerse en el código FOURCC.

Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente. Por ejemplo, la macro **MAKEFOURCC** se declara en Mmsystem.h y la macro **FCC** se declara en Aviriff.h. Úsenlos como se muestra a continuación:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



También puede declarar un código FOURCC directamente como literal de cadena simplemente invirtiendo el orden de los caracteres. Por ejemplo:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



Es necesario invertir el orden porque el sistema operativo Windows microsoft usa una arquitectura little-endian. 'Y' = 0x59, 'U' = 0x55 y '2' = 0x32, por lo que '2YUY' es 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Conversión de códigos FOURCC en GUID de subtipo

Se reserva un intervalo de \* 2 32 GUID para representar FOURCC. Estos GUID tienen todo el formato `XXXXXXXX-0000-0010-8000-00AA00389B71` donde es el código `XXXXXXXX` FOURCC. Por lo tanto, el GUID del subtipo para YUY2 es `32595559-0000-0010-8000-00AA00389B71` .

Muchos de estos GUID ya están definidos en el archivo de encabezado Uuids.h. Por ejemplo, el subtipo YUY2 se define como MEDIASUBTYPE \_ YUY2. La DirectShow de clases base también proporciona una clase auxiliar, [**FOURCCMap**](fourccmap.md), que se puede usar para convertir códigos FOURCC en valores GUID. El constructor **FOURCCMap** toma un código FOURCC como parámetro de entrada. A continuación, puede convertir **el objeto FOURCCMap** al GUID correspondiente:


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Subtipos de audio**](audio-subtypes.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabajar con códecs](working-with-codecs.md)
</dt> </dl>

 

 



