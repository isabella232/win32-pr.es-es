---
description: Códigos FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Códigos FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152018"
---
# <a name="fourcc-codes"></a>Códigos FOURCC

Muchos formatos de medios digitales tienen códigos FOURCC asignados. Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII. Por ejemplo, el código FOURCC del vídeo YUY2 es "YUY2". En el caso de los formatos de vídeo comprimidos y los formatos de vídeo no RGB (como YUV), el miembro de **bicompresión** de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) debe establecerse en el código FourCC.

Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente. Por ejemplo, la macro **MAKEFOURCC** se declara en mmsystem. h y la macro **FCC** se declara en Aviriff. h. Úselos de la siguiente manera:


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres. Por ejemplo:


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



Invertir el orden es necesario porque el sistema operativo Microsoft Windows usa una arquitectura little-endian. ' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Convertir códigos FOURCC en GUID de subtipo

Un intervalo de 2 \* 32 GUID está reservado para representar FOURCCs. Estos GUID tienen todo el formato, `XXXXXXXX-0000-0010-8000-00AA00389B71` donde `XXXXXXXX` es el código FourCC. Por lo tanto, el GUID del subtipo para YUY2 es `32595559-0000-0010-8000-00AA00389B71` .

Muchos de estos GUID ya están definidos en el archivo de encabezado UUID. h. Por ejemplo, el subtipo YUY2 se define como MEDIASUBTYPE \_ YUY2. La biblioteca de clases base de DirectShow también proporciona una clase auxiliar, [**FOURCCMap**](fourccmap.md), que se puede usar para convertir códigos FourCC en valores GUID. El constructor **FOURCCMap** toma un código FourCC como parámetro de entrada. Después, puede convertir el objeto **FOURCCMap** al GUID correspondiente:


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

 

 



