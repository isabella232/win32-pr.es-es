---
description: Datos de DV en el formato de archivo AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Datos de DV en el formato de archivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495545"
---
# <a name="dv-data-in-the-avi-file-format"></a>Datos de DV en el formato de archivo AVI

Microsoft ha especificado el formato de almacenamiento de datos de vídeo digital (DV) en archivos AVI. Conforme a esta especificación, se asegurará de que los archivos AVI creados en este formato serán compatibles con las versiones futuras de la arquitectura de vídeo digital de DirectShow para Windowsplatform.

En este artículo se describe el formato de archivos AVI que contienen datos de DV. Se definen FOURCCs específicos (códigos de cuatro caracteres) para los flujos de datos DV intercalados y los controladores de transmisión compresor/descompresor DV. Se define la estructura de formato de secuencia para los datos de DV. Se especifican las especificaciones para dos métodos de almacenamiento de datos de DV en el formato de archivo AVI.

Se supone que el lector está familiarizado con el formato de datos de DV. (Este formato se define en la *especificación de los VCR digitales de uso del consumidor*, también denominado libro azul).

Hay dos tipos de archivos AVI de DV: archivos AVI que contienen un flujo de datos DV, denominados archivos *de tipo 1* . y archivos AVI que contienen vídeo DV como una secuencia de ' vid ' y audio DV como secuencias ' Auds ', denominados archivos *de tipo 2* .

**Archivos AVI que contienen un flujo de datos DV (tipo 1)**

Los datos DV intercalados se pueden almacenar en su formato nativo como una sola secuencia dentro de un archivo de AVI RIFF. Esto tiene la ventaja de usar la cantidad mínima de almacenamiento de datos para DV. El principal inconveniente es que este formato de archivo no es compatible con las versiones anteriores del vídeo para Windows, porque no contiene una secuencia ' Auds ' de vídeo o de audio. Se proporciona compatibilidad con la secuencia DV intercalada a través de los filtros [DV multiplexor](dv-muxer-filter.md) y [divisor DV](dv-splitter-filter.md) que se proporcionan con DirectShow.

Los datos de DV se pueden almacenar en un solo flujo dentro de un archivo de AVI. para ello, se especifica el elemento FOURCC ' iavs ' (audio y vídeo entrelazado) (código de cuatro caracteres) en el miembro **fccType** y cualquiera de los DVSL ' DVSD ', ' dvhd ' o ' FOURCCs ' en el miembro **fccHandler** del fragmento del encabezado de secuencia ' strh '. Los fotogramas por segundo de la secuencia de vídeo se deben especificar en los miembros **dwRate** y **dwScale** y el número total de bloques de vídeo en el fragmento ' movi ' en el miembro **dwLength** .

El controlador de flujo "DVSD" FOURCC especifica que los datos de DV están definidos en la parte 2 de la *especificación de los VCR digitales de uso del consumidor*. El vídeo tiene el formato de 525 líneas a 29,97 Hz (525-60) o líneas de 625 a 25,00 Hz (625-50).

El controlador de flujo "dvhd" FOURCC especifica que los datos de DV están definidos en la parte 3 de la *especificación de los VCR digitales de uso del consumidor*. El vídeo tiene el formato de 1125 líneas a 30,00 Hz (1125-60) o líneas de 1250 a 25,00 Hz (1250-50).

El controlador de flujo "DVSL" FOURCC especifica que los datos de DV están tal y como se define en la parte 6 de la *especificación de los VCR digitales de uso del consumidor*. El vídeo tiene el formato de SD de compresión alta (SDL).

> [!Note]  
> El resto de este artículo proporciona definiciones para las secuencias "DVSD".

 

El fragmento de encabezado de secuencia debe ir seguido de un fragmento de formato de secuencia [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

Los datos DV reales se almacenan como \# \# fragmentos ' DC ' en el fragmento ' movi ' (el \# \# en el formato representa el identificador de flujo). Cada fragmento contiene un fotograma de datos, ya sea 10 o 12 secuencias de DV DIF para sistemas 525-60 o 625-50, respectivamente. El formato de secuencia DIF SD (' DVSD ') se define en la segunda parte de la *especificación de los VCR digitales de uso del consumidor*.

En el ejemplo siguiente se muestra el formulario AIFF RIFF para un archivo AVI con un flujo de datos DV, expandido con fragmentos de encabezado completados.


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



**Archivos AVI que contienen secuencias de audio DV y vídeo DV (tipo 2)**

Los datos DV intercalados se pueden dividir en una secuencia de vídeo y de una a cuatro secuencias de audio dentro de un archivo de AVI RIFF. Esto tiene la ventaja de ser compatible con versiones anteriores de vídeo para Windows, porque contiene un flujo de vídeo estándar ' vid ' y, al menos, un flujo de audio estándar ' Auds ', el principal inconveniente es que este formato de archivo requiere que los datos de audio se almacenen de forma redundante como secuencias de audio. El flujo de "vídeo" es realmente el flujo de datos DV intercalado nativo. Sin embargo, como un flujo estándar de ' vid ' con un tipo de controlador de ' DVSD ', se usa el [descodificador de vídeo DV](dv-video-decoder-filter.md) . Este formato también requiere el uso del filtro de [divisor DV](dv-splitter-filter.md) para dividir los archivos "capturados" antes de escribirlos como archivos AVI.

Los datos de DV se pueden almacenar como una secuencia de vídeo con un número independiente de secuencias de audio en un archivo de AVI RIFF. La secuencia de vídeo se especifica con un encabezado de flujo de vídeo estándar (el valor del miembro **fccType** es ' vid '). El miembro **fccHandler** se especifica como ' DVSD ', ' dvhd ' o ' DVSL '. Los fotogramas por segundo de la secuencia de vídeo se deben especificar en los miembros **dwRate** y **dwScale** y el número total de bloques de vídeo en el fragmento ' movi ' en el miembro **dwLength** .

En este archivo AVI que contiene vídeo DV como una secuencia de ' vid ' y un audio DV como una forma de secuencias de DV ' Auds ', el fragmento de formato de secuencia de vídeo es una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) estándar. El fragmento de formato de secuencia se puede extender opcionalmente para incluir el fragmento [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando el tamaño del fragmento del formato de flujo de 40 bytes (tamaño de la estructura **BITMAPINFOHEADER** ) a 72 bytes (tamaño de **BITMAPINFOHEADER** más **DVINFO** ) e inmediatamente después de la estructura de datos **BITMAPINFOHEADER** con una estructura de datos **DVINFO** .

Las secuencias de audio se especifican con un encabezado de flujo de audio estándar (el valor del miembro **fccType** es "Auds"). El miembro **fccHandler** no se utiliza para secuencias de audio.

Los datos de vídeo DV se almacenan como \# \# fragmentos "DC", tal como se define en la descripción anterior de un archivo AVI con uno de datos DV, y los datos de audio se almacenan como \# \# fragmentos "WB" en el fragmento "movi".

> [!Note]  
> Es posible que la *especificación de los VCR digitales de uso del consumidor* no esté disponible en algunos idiomas y países.

 

En el ejemplo siguiente se muestra el formulario AIFF RIFF para un archivo AVI que contiene vídeo DV como una secuencia ' vid ' y audio DV como secuencias ' Auds ' expandidas con fragmentos de encabezado completos (incluidos los datos de [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) opcionales que siguen a [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) en el subfragmento ' strf ' para la secuencia ' vid ').


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

 

 
