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
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="8eade-103">Datos de DV en el formato de archivo AVI</span><span class="sxs-lookup"><span data-stu-id="8eade-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="8eade-104">Microsoft ha especificado el formato de almacenamiento de datos de vídeo digital (DV) en archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="8eade-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="8eade-105">Conforme a esta especificación, se asegurará de que los archivos AVI creados en este formato serán compatibles con las versiones futuras de la arquitectura de vídeo digital de DirectShow para Windowsplatform.</span><span class="sxs-lookup"><span data-stu-id="8eade-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="8eade-106">En este artículo se describe el formato de archivos AVI que contienen datos de DV.</span><span class="sxs-lookup"><span data-stu-id="8eade-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="8eade-107">Se definen FOURCCs específicos (códigos de cuatro caracteres) para los flujos de datos DV intercalados y los controladores de transmisión compresor/descompresor DV.</span><span class="sxs-lookup"><span data-stu-id="8eade-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="8eade-108">Se define la estructura de formato de secuencia para los datos de DV.</span><span class="sxs-lookup"><span data-stu-id="8eade-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="8eade-109">Se especifican las especificaciones para dos métodos de almacenamiento de datos de DV en el formato de archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="8eade-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="8eade-110">Se supone que el lector está familiarizado con el formato de datos de DV.</span><span class="sxs-lookup"><span data-stu-id="8eade-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="8eade-111">(Este formato se define en la *especificación de los VCR digitales de uso del consumidor*, también denominado libro azul).</span><span class="sxs-lookup"><span data-stu-id="8eade-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="8eade-112">Hay dos tipos de archivos AVI de DV: archivos AVI que contienen un flujo de datos DV, denominados archivos *de tipo 1* . y archivos AVI que contienen vídeo DV como una secuencia de ' vid ' y audio DV como secuencias ' Auds ', denominados archivos *de tipo 2* .</span><span class="sxs-lookup"><span data-stu-id="8eade-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="8eade-113">**Archivos AVI que contienen un flujo de datos DV (tipo 1)**</span><span class="sxs-lookup"><span data-stu-id="8eade-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="8eade-114">Los datos DV intercalados se pueden almacenar en su formato nativo como una sola secuencia dentro de un archivo de AVI RIFF.</span><span class="sxs-lookup"><span data-stu-id="8eade-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="8eade-115">Esto tiene la ventaja de usar la cantidad mínima de almacenamiento de datos para DV.</span><span class="sxs-lookup"><span data-stu-id="8eade-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="8eade-116">El principal inconveniente es que este formato de archivo no es compatible con las versiones anteriores del vídeo para Windows, porque no contiene una secuencia ' Auds ' de vídeo o de audio.</span><span class="sxs-lookup"><span data-stu-id="8eade-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="8eade-117">Se proporciona compatibilidad con la secuencia DV intercalada a través de los filtros [DV multiplexor](dv-muxer-filter.md) y [divisor DV](dv-splitter-filter.md) que se proporcionan con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8eade-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="8eade-118">Los datos de DV se pueden almacenar en un solo flujo dentro de un archivo de AVI. para ello, se especifica el elemento FOURCC ' iavs ' (audio y vídeo entrelazado) (código de cuatro caracteres) en el miembro **fccType** y cualquiera de los DVSL ' DVSD ', ' dvhd ' o ' FOURCCs ' en el miembro **fccHandler** del fragmento del encabezado de secuencia ' strh '.</span><span class="sxs-lookup"><span data-stu-id="8eade-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="8eade-119">Los fotogramas por segundo de la secuencia de vídeo se deben especificar en los miembros **dwRate** y **dwScale** y el número total de bloques de vídeo en el fragmento ' movi ' en el miembro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="8eade-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="8eade-120">El controlador de flujo "DVSD" FOURCC especifica que los datos de DV están definidos en la parte 2 de la *especificación de los VCR digitales de uso del consumidor*.</span><span class="sxs-lookup"><span data-stu-id="8eade-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="8eade-121">El vídeo tiene el formato de 525 líneas a 29,97 Hz (525-60) o líneas de 625 a 25,00 Hz (625-50).</span><span class="sxs-lookup"><span data-stu-id="8eade-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="8eade-122">El controlador de flujo "dvhd" FOURCC especifica que los datos de DV están definidos en la parte 3 de la *especificación de los VCR digitales de uso del consumidor*.</span><span class="sxs-lookup"><span data-stu-id="8eade-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="8eade-123">El vídeo tiene el formato de 1125 líneas a 30,00 Hz (1125-60) o líneas de 1250 a 25,00 Hz (1250-50).</span><span class="sxs-lookup"><span data-stu-id="8eade-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="8eade-124">El controlador de flujo "DVSL" FOURCC especifica que los datos de DV están tal y como se define en la parte 6 de la *especificación de los VCR digitales de uso del consumidor*.</span><span class="sxs-lookup"><span data-stu-id="8eade-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="8eade-125">El vídeo tiene el formato de SD de compresión alta (SDL).</span><span class="sxs-lookup"><span data-stu-id="8eade-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="8eade-126">El resto de este artículo proporciona definiciones para las secuencias "DVSD".</span><span class="sxs-lookup"><span data-stu-id="8eade-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="8eade-127">El fragmento de encabezado de secuencia debe ir seguido de un fragmento de formato de secuencia [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="8eade-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="8eade-128">Los datos DV reales se almacenan como \# \# fragmentos ' DC ' en el fragmento ' movi ' (el \# \# en el formato representa el identificador de flujo).</span><span class="sxs-lookup"><span data-stu-id="8eade-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="8eade-129">Cada fragmento contiene un fotograma de datos, ya sea 10 o 12 secuencias de DV DIF para sistemas 525-60 o 625-50, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8eade-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="8eade-130">El formato de secuencia DIF SD (' DVSD ') se define en la segunda parte de la *especificación de los VCR digitales de uso del consumidor*.</span><span class="sxs-lookup"><span data-stu-id="8eade-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="8eade-131">En el ejemplo siguiente se muestra el formulario AIFF RIFF para un archivo AVI con un flujo de datos DV, expandido con fragmentos de encabezado completados.</span><span class="sxs-lookup"><span data-stu-id="8eade-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


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



<span data-ttu-id="8eade-132">**Archivos AVI que contienen secuencias de audio DV y vídeo DV (tipo 2)**</span><span class="sxs-lookup"><span data-stu-id="8eade-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="8eade-133">Los datos DV intercalados se pueden dividir en una secuencia de vídeo y de una a cuatro secuencias de audio dentro de un archivo de AVI RIFF.</span><span class="sxs-lookup"><span data-stu-id="8eade-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="8eade-134">Esto tiene la ventaja de ser compatible con versiones anteriores de vídeo para Windows, porque contiene un flujo de vídeo estándar ' vid ' y, al menos, un flujo de audio estándar ' Auds ', el principal inconveniente es que este formato de archivo requiere que los datos de audio se almacenen de forma redundante como secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="8eade-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="8eade-135">El flujo de "vídeo" es realmente el flujo de datos DV intercalado nativo.</span><span class="sxs-lookup"><span data-stu-id="8eade-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="8eade-136">Sin embargo, como un flujo estándar de ' vid ' con un tipo de controlador de ' DVSD ', se usa el [descodificador de vídeo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8eade-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="8eade-137">Este formato también requiere el uso del filtro de [divisor DV](dv-splitter-filter.md) para dividir los archivos "capturados" antes de escribirlos como archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="8eade-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="8eade-138">Los datos de DV se pueden almacenar como una secuencia de vídeo con un número independiente de secuencias de audio en un archivo de AVI RIFF.</span><span class="sxs-lookup"><span data-stu-id="8eade-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="8eade-139">La secuencia de vídeo se especifica con un encabezado de flujo de vídeo estándar (el valor del miembro **fccType** es ' vid ').</span><span class="sxs-lookup"><span data-stu-id="8eade-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="8eade-140">El miembro **fccHandler** se especifica como ' DVSD ', ' dvhd ' o ' DVSL '.</span><span class="sxs-lookup"><span data-stu-id="8eade-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="8eade-141">Los fotogramas por segundo de la secuencia de vídeo se deben especificar en los miembros **dwRate** y **dwScale** y el número total de bloques de vídeo en el fragmento ' movi ' en el miembro **dwLength** .</span><span class="sxs-lookup"><span data-stu-id="8eade-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="8eade-142">En este archivo AVI que contiene vídeo DV como una secuencia de ' vid ' y un audio DV como una forma de secuencias de DV ' Auds ', el fragmento de formato de secuencia de vídeo es una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) estándar.</span><span class="sxs-lookup"><span data-stu-id="8eade-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="8eade-143">El fragmento de formato de secuencia se puede extender opcionalmente para incluir el fragmento [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , aumentando el tamaño del fragmento del formato de flujo de 40 bytes (tamaño de la estructura **BITMAPINFOHEADER** ) a 72 bytes (tamaño de **BITMAPINFOHEADER** más **DVINFO** ) e inmediatamente después de la estructura de datos **BITMAPINFOHEADER** con una estructura de datos **DVINFO** .</span><span class="sxs-lookup"><span data-stu-id="8eade-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="8eade-144">Las secuencias de audio se especifican con un encabezado de flujo de audio estándar (el valor del miembro **fccType** es "Auds").</span><span class="sxs-lookup"><span data-stu-id="8eade-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="8eade-145">El miembro **fccHandler** no se utiliza para secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="8eade-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="8eade-146">Los datos de vídeo DV se almacenan como \# \# fragmentos "DC", tal como se define en la descripción anterior de un archivo AVI con uno de datos DV, y los datos de audio se almacenan como \# \# fragmentos "WB" en el fragmento "movi".</span><span class="sxs-lookup"><span data-stu-id="8eade-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="8eade-147">Es posible que la *especificación de los VCR digitales de uso del consumidor* no esté disponible en algunos idiomas y países.</span><span class="sxs-lookup"><span data-stu-id="8eade-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="8eade-148">En el ejemplo siguiente se muestra el formulario AIFF RIFF para un archivo AVI que contiene vídeo DV como una secuencia ' vid ' y audio DV como secuencias ' Auds ' expandidas con fragmentos de encabezado completos (incluidos los datos de [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) opcionales que siguen a [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) en el subfragmento ' strf ' para la secuencia ' vid ').</span><span class="sxs-lookup"><span data-stu-id="8eade-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8eade-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8eade-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eade-150">Formato de archivo AVI</span><span class="sxs-lookup"><span data-stu-id="8eade-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
