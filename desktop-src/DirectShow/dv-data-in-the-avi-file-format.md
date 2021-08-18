---
description: Datos DV en formato de archivo AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Datos DV en formato de archivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c048cb42fa3ba49457c115944075c064b9cfd4c31263519e9d5af3e5f0a268a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749117"
---
# <a name="dv-data-in-the-avi-file-format"></a>Datos DV en formato de archivo AVI

Microsoft ha especificado el formato para el almacenamiento de datos de vídeo digital (DV) en archivos AVI. El cumplimiento de esta especificación garantizará que los archivos AVI creados en este formato sean compatibles con versiones futuras de la arquitectura de vídeo digital de DirectShow para Windowsplatform.

En este artículo se describe el formato de los archivos AVI que contienen datos DV. Se definen los FOURCC específicos (códigos de cuatro caracteres) para los flujos de datos DV intercalados y los controladores de flujo de descompresión/descompresión de DV. Se define la estructura de formato de secuencia para los datos DV. Se especifican especificaciones para dos métodos de almacenamiento de datos DV en el formato de archivo AVI.

Se supone que el lector está familiarizado con el formato de datos DV. (Este formato se define en la Especificación de *VCR digitales* de uso del consumidor, también denominada libro azul).

Hay dos tipos de archivos DV AVI: archivos AVI que contienen un flujo de datos DV, *denominados archivos de tipo 1;* y archivos AVI que contienen vídeo DV como secuencia "vids" y audio DV como secuencias "auds", denominados *archivos de tipo 2.*

**Archivos AVI que contienen un flujo de datos DV (tipo 1)**

Los datos DV intercalados se pueden almacenar en su formato nativo como una sola secuencia dentro de un archivo AVI RIFF. Esto tiene la ventaja de usar la cantidad mínima de almacenamiento de datos para DV. La principal desventaja es que este formato de archivo no es compatible con versiones anteriores de Video para Windows, ya que no contiene una secuencia de vídeo "vids" ni de audio "auds". Se proporciona compatibilidad con la secuencia DV intercalada a través de los filtros [DV Muxer](dv-muxer-filter.md) y [DV Splitter](dv-splitter-filter.md) proporcionados con DirectShow.

Los datos DV se pueden almacenar en una sola secuencia dentro de un archivo AVI RIFF especificando los FOURCC "iavs" (secuencia de audio y vídeo intercalados) (código de cuatro caracteres) en el miembro **fccType** y cualquiera de los FOURC "dvsd", "dvhd" o "dvsl" en el miembro **fccHandler** del fragmento de encabezado de secuencia "strh". Los fotogramas por segundo de la secuencia de vídeo deben especificarse en los miembros **dwRate** y **dwScale** y en el número total de bloques de vídeo del fragmento "mgula" del **miembro dwLength.**

El controlador de secuencias 'dvsd' FOURCC especifica que los datos DV se definen en la parte 2 de la especificación de vcrs digitales de uso *del consumidor.* El vídeo tiene el formato de 525 líneas a 29,97 Hz (525-60) o 625 líneas a 25,00 Hz (625-50).

El controlador de secuencias 'dvhd' FOURCC especifica que los datos DV se definen en la parte 3 de la especificación de vcrs digitales de uso *del consumidor.* El vídeo tiene el formato de 1125 líneas a 30,00 Hz (1125-60) o 1250 líneas a 25,00 Hz (1250-50).

El controlador de secuencias 'dvsl' FOURCC especifica que los datos DV se definen en la parte 6 de la especificación de vcrs digitales de uso *del consumidor.* El vídeo tiene el formato de SD (SDL) de compresión alta.

> [!Note]  
> En el resto de este artículo se proporcionan definiciones para secuencias "dvsd".

 

El fragmento de encabezado de secuencia debe ir seguido de un fragmento de formato de secuencia [**DVINFO.**](/windows/desktop/api/strmif/ns-strmif-dvinfo)

Los datos dv reales se almacenan como fragmentos "dc" en el fragmento \# "mtransmisión" (el en el formato \# representa el identificador de \# \# flujo). Cada fragmento contiene un fotograma de datos, ya sea 10 o 12 secuencias DV DIF para sistemas 525-60 o 625-50, respectivamente. El formato de secuencia DIF DV SD ('dvsd') se define en la parte 2 de la especificación de *vcrs digitales* de uso del consumidor.

En el ejemplo siguiente se muestra el formulario RIFF de AIFF para un archivo AVI con un flujo de datos DV, expandido con fragmentos de encabezado completados.


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



**Archivos AVI que contienen vídeo DV y audio DV Secuencias (tipo 2)**

Los datos DV intercalados se pueden dividir en una secuencia de vídeo y de una a cuatro secuencias de audio dentro de un archivo AVI RIFF. Esto tiene la ventaja de ser compatible con versiones anteriores de Video para Windows, ya que contiene una secuencia de vídeo estándar "vids" y al menos una secuencia de audio estándar "auds". La principal desventaja es que este formato de archivo requiere que los datos de audio se almacenen redundantemente como secuencias de audio. La secuencia de "vídeo" es realmente el flujo de datos DV intercalado nativo. Sin embargo, como una secuencia estándar "vids" con un tipo de controlador de "dvsd", se usa el descodificador de vídeo [DV.](dv-video-decoder-filter.md) Este formato también requiere el uso del filtro [divisor DV](dv-splitter-filter.md) para dividir los archivos "capturados" antes de escribirlos como archivos AVI.

Los datos DV se pueden almacenar como una secuencia de vídeo con un número independiente de secuencias de audio en un archivo AVI RIFF. La secuencia de vídeo se especifica con un encabezado de secuencia de vídeo estándar (el valor del miembro **fccType** es "vids"). El **miembro fccHandler** se especifica como "dvsd", "dvhd" o "dvsl". Los fotogramas por segundo de la secuencia de vídeo deben especificarse en los miembros **dwRate** y **dwScale** y en el número total de bloques de vídeo del fragmento "mgula" del **miembro dwLength.**

En este archivo AVI que contiene vídeo DV como secuencia "vids" y audio DV como secuencias "auds" forma de DV, el fragmento de formato de secuencia de vídeo es una estructura [**BITMAPINFOHEADER estándar.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Opcionalmente, el fragmento de formato de secuencia se puede ampliar para incluir el fragmento [**DVINFO,**](/windows/desktop/api/strmif/ns-strmif-dvinfo) aumentando el tamaño del fragmento de formato de secuencia de 40 bytes (tamaño de la estructura **BITMAPINFOHEADER)** a 72 bytes (tamaño de **bitmapinfoheader** más estructuras **DVINFO)** y siguiendo inmediatamente la estructura de datos **BITMAPINFOHEADER** con una estructura de datos **DVINFO.**

Las secuencias de audio se especifican con un encabezado de secuencia de audio estándar (el valor del miembro **fccType** es "auds"). El **miembro fccHandler** no se usa para las secuencias de audio.

Los datos de vídeo DV se almacenan como fragmentos "dc", tal y como se define en la descripción anterior de un archivo AVI con un solo dato DV, y los datos de audio se almacenan como fragmentos "wb" en el fragmento \# \# \# \# "munión".

> [!Note]  
> Es *posible que la especificación de los VCR digitales* de uso del consumidor no esté disponible en algunos idiomas y países.

 

En el ejemplo siguiente se muestra el formulario RIFF de AIFF para un archivo AVI que contiene vídeo DV como una secuencia "vids" y audio DV como secuencias "auds" expandida con fragmentos de encabezado completados (incluidos los datos [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) opcionales que sigue a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) en el sub fragmento "strf" para la secuencia "vids").


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de archivo AVI](avi-file-format.md)
</dt> </dl>

 

 
