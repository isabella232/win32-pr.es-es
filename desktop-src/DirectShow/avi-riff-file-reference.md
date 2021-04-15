---
description: Referencia de archivo de AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referencia de archivo de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495664"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="d4580-103">Referencia de archivo de AVI</span><span class="sxs-lookup"><span data-stu-id="d4580-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="d4580-104">El formato de archivo AVI de Microsoft es una especificación de archivo RIFF utilizada con aplicaciones que capturan, editan y reproducen secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4580-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="d4580-105">En general, los archivos AVI contienen varios flujos de tipos de datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="d4580-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="d4580-106">La mayoría de las secuencias AVI usan secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4580-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="d4580-107">Una variación simple de una secuencia AVI usa datos de vídeo y no requiere una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="d4580-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="d4580-108">En esta sección no se describen las extensiones de formato de archivo AVI OpenDML.</span><span class="sxs-lookup"><span data-stu-id="d4580-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="d4580-109">Para obtener más información acerca de estas extensiones, consulte *extensiones de formato de archivo AVI de OpenDML*, publicadas por el Subcomité del formato de archivo AVI de OpenDML AVI.</span><span class="sxs-lookup"><span data-stu-id="d4580-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="d4580-110">FOURCCs</span><span class="sxs-lookup"><span data-stu-id="d4580-110">FOURCCs</span></span>

<span data-ttu-id="d4580-111">Un FOURCC (código de cuatro caracteres) es un entero sin signo de 32 bits creado mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="d4580-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="d4580-112">Por ejemplo, el FOURCC ' abcd ' se representa en un sistema Little-Endian como 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="d4580-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="d4580-113">FOURCCs puede contener caracteres de espacio, por lo que ' ABC ' es un FOURCC válido.</span><span class="sxs-lookup"><span data-stu-id="d4580-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="d4580-114">El formato de archivo AVI usa códigos FOURCC para identificar tipos de secuencias, fragmentos de datos, entradas de índice y otra información.</span><span class="sxs-lookup"><span data-stu-id="d4580-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="d4580-115">Formato de archivo RIFF</span><span class="sxs-lookup"><span data-stu-id="d4580-115">RIFF File Format</span></span>

<span data-ttu-id="d4580-116">El formato de archivo AVI se basa en el formato de documento RIFF (formato de archivo de intercambio de recursos).</span><span class="sxs-lookup"><span data-stu-id="d4580-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="d4580-117">Un archivo RIFF está formado por un encabezado RIFF seguido de cero o más *listas* y *fragmentos*.</span><span class="sxs-lookup"><span data-stu-id="d4580-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="d4580-118">El encabezado RIFF tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4580-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="d4580-119">donde ' RIFF ' es el código FOURCC literal ' RIFF ', `fileSize` es un valor de 4 bytes que asigna el tamaño de los datos en el archivo y `fileType` es un FourCC que identifica el tipo de archivo específico.</span><span class="sxs-lookup"><span data-stu-id="d4580-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="d4580-120">El valor de `fileSize` incluye el tamaño del `fileType` FourCC más el tamaño de los datos siguientes, pero no incluye el tamaño del FourCC ' riff ' ni el tamaño de `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="d4580-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="d4580-121">Los datos de archivo se componen de fragmentos y listas, en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="d4580-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="d4580-122">Un fragmento tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4580-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="d4580-123">donde `ckID` es un FourCC que identifica los datos contenidos en el fragmento, `ckSize` es un valor de 4 bytes que asigna el tamaño de los datos `ckData` y `ckData` es cero o más bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="d4580-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="d4580-124">Los datos siempre se rellenan hasta el límite de la **palabra** más cercana.</span><span class="sxs-lookup"><span data-stu-id="d4580-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="d4580-125">`ckSize` proporciona el tamaño de los datos válidos en el fragmento; no incluye el relleno, el tamaño `ckID` o el tamaño de `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="d4580-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="d4580-126">Una lista tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4580-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="d4580-127">donde ' LIST ' es el código FOURCC literal ' LIST ', `listSize` es un valor de 4 bytes que proporciona el tamaño de la lista, `listType` es un código FourCC y `listData` consta de fragmentos o listas, en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="d4580-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="d4580-128">El valor de `listSize` incluye el tamaño de `listType` más el tamaño de `listData` ; no incluye el FourCC ' List ' o el tamaño de `listSize` .</span><span class="sxs-lookup"><span data-stu-id="d4580-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="d4580-129">En el resto de esta sección se usa la siguiente notación para describir fragmentos RIFF:</span><span class="sxs-lookup"><span data-stu-id="d4580-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="d4580-130">donde el tamaño del fragmento es implícito.</span><span class="sxs-lookup"><span data-stu-id="d4580-130">where the chunk size is implicit.</span></span> <span data-ttu-id="d4580-131">Con esta notación, una lista se puede representar como:</span><span class="sxs-lookup"><span data-stu-id="d4580-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="d4580-132">Los elementos opcionales se colocan entre corchetes: `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="d4580-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="d4580-133">Forma de AVI RIFF</span><span class="sxs-lookup"><span data-stu-id="d4580-133">AVI RIFF Form</span></span>

<span data-ttu-id="d4580-134">Los archivos AVI se identifican mediante el FOURCC ' AVI ' en el encabezado RIFF.</span><span class="sxs-lookup"><span data-stu-id="d4580-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="d4580-135">Todos los archivos AVI incluyen dos fragmentos de lista obligatorios, que definen el formato de las secuencias y los datos de la secuencia, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d4580-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="d4580-136">Un archivo AVI también puede incluir un fragmento de índice, que proporciona la ubicación de los fragmentos de datos dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="d4580-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="d4580-137">Un archivo AVI con estos componentes tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="d4580-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="d4580-138">La lista ' HDRL ' define el formato de los datos y es el primer fragmento de lista necesario.</span><span class="sxs-lookup"><span data-stu-id="d4580-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="d4580-139">La lista ' movi ' contiene los datos de la secuencia AVI y es el segundo fragmento de lista necesario.</span><span class="sxs-lookup"><span data-stu-id="d4580-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="d4580-140">La lista ' idx1 ' contiene el índice.</span><span class="sxs-lookup"><span data-stu-id="d4580-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="d4580-141">Los archivos AVI deben mantener estos tres componentes en la secuencia adecuada.</span><span class="sxs-lookup"><span data-stu-id="d4580-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="d4580-142">Las extensiones OpenDML definen otro tipo de índice, identificado por el FOURCC ' indx '.</span><span class="sxs-lookup"><span data-stu-id="d4580-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="d4580-143">Las listas "HDRL" y "movi" usan subfragmentos para sus datos.</span><span class="sxs-lookup"><span data-stu-id="d4580-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="d4580-144">En el ejemplo siguiente se muestra la forma de AVI RIFF expandida con los fragmentos necesarios para completar estas listas:</span><span class="sxs-lookup"><span data-stu-id="d4580-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="d4580-145">Encabezado principal de AVI</span><span class="sxs-lookup"><span data-stu-id="d4580-145">AVI Main Header</span></span>

<span data-ttu-id="d4580-146">La lista ' HDRL ' comienza con el encabezado AVI principal, que se encuentra en un fragmento ' AVIH '.</span><span class="sxs-lookup"><span data-stu-id="d4580-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="d4580-147">El encabezado principal contiene información global del archivo AVI completo, como el número de flujos dentro del archivo y el ancho y el alto de la secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="d4580-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="d4580-148">El fragmento del encabezado principal se compone de una estructura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="d4580-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="d4580-149">Encabezados de secuencia AVI</span><span class="sxs-lookup"><span data-stu-id="d4580-149">AVI Stream Headers</span></span>

<span data-ttu-id="d4580-150">Una o más listas ' strl ' siguen el encabezado principal.</span><span class="sxs-lookup"><span data-stu-id="d4580-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="d4580-151">Se requiere una lista ' strl ' para cada flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="d4580-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="d4580-152">Cada lista ' strl ' contiene información sobre una secuencia en el archivo y debe contener un fragmento de encabezado de secuencia (' strh ') y un fragmento de formato de secuencia (' strf ').</span><span class="sxs-lookup"><span data-stu-id="d4580-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="d4580-153">Además, una lista ' strl ' podría contener un fragmento de datos de encabezado de flujo (' StrD ') y un fragmento de nombre de flujo (' STRN ').</span><span class="sxs-lookup"><span data-stu-id="d4580-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="d4580-154">El fragmento de encabezado de secuencia (' strh ') se compone de una estructura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .</span><span class="sxs-lookup"><span data-stu-id="d4580-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="d4580-155">Un fragmento de formato de secuencia (' strf ') debe seguir el fragmento de encabezado de flujo.</span><span class="sxs-lookup"><span data-stu-id="d4580-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="d4580-156">El fragmento de formato de secuencia describe el formato de los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d4580-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="d4580-157">Los datos contenidos en este fragmento dependen del tipo de flujo.</span><span class="sxs-lookup"><span data-stu-id="d4580-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="d4580-158">En el caso de las secuencias de vídeo, la información es una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluida la información de la paleta si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d4580-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="d4580-159">En el caso de las secuencias de audio, la información es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d4580-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="d4580-160">Si el fragmento de datos de encabezado de secuencia (' StrD ') está presente, sigue el fragmento de formato de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d4580-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="d4580-161">El formato y el contenido de este fragmento se definen mediante el controlador del códec.</span><span class="sxs-lookup"><span data-stu-id="d4580-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="d4580-162">Normalmente, los controladores usan esta información para la configuración.</span><span class="sxs-lookup"><span data-stu-id="d4580-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="d4580-163">No es necesario que las aplicaciones que leen y escriben archivos AVI interpreten esta información; simplemente lo transfieren al controlador como un bloque de memoria y desde él.</span><span class="sxs-lookup"><span data-stu-id="d4580-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="d4580-164">El fragmento opcional ' STRN ' contiene una cadena de texto terminada en null que describe la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d4580-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="d4580-165">Los encabezados de la secuencia de la lista ' HDRL ' se asocian con los datos de la secuencia de la lista ' movi ' según el orden de los fragmentos ' strl '.</span><span class="sxs-lookup"><span data-stu-id="d4580-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="d4580-166">El primer fragmento ' strl ' se aplica al flujo 0, el segundo se aplica a la secuencia 1, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d4580-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="d4580-167">Streaming de datos (lista ' movi ')</span><span class="sxs-lookup"><span data-stu-id="d4580-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="d4580-168">La información de encabezado siguiente es una lista de "movi" que contiene los datos reales de las secuencias, es decir, los fotogramas de vídeo y ejemplos de audio.</span><span class="sxs-lookup"><span data-stu-id="d4580-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="d4580-169">Los fragmentos de datos pueden residir directamente en la lista ' movi ' o pueden estar agrupados en listas de ' Rec '.</span><span class="sxs-lookup"><span data-stu-id="d4580-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="d4580-170">La agrupación ' Rec ' implica que los fragmentos agrupados se deben leer del disco todos a la vez y está destinado a los archivos que se intercalan en el CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d4580-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="d4580-171">El FOURCC que identifica cada fragmento de datos consta de un número de secuencia de dos dígitos seguido de un código de dos caracteres que define el tipo de información del fragmento.</span><span class="sxs-lookup"><span data-stu-id="d4580-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="d4580-172">Código de dos caracteres</span><span class="sxs-lookup"><span data-stu-id="d4580-172">Two-character code</span></span> | <span data-ttu-id="d4580-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4580-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="d4580-174">db</span><span class="sxs-lookup"><span data-stu-id="d4580-174">db</span></span>                 | <span data-ttu-id="d4580-175">Fotograma de vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="d4580-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="d4580-176">dc</span><span class="sxs-lookup"><span data-stu-id="d4580-176">dc</span></span>                 | <span data-ttu-id="d4580-177">Fotograma de vídeo comprimido</span><span class="sxs-lookup"><span data-stu-id="d4580-177">Compressed video frame</span></span>   |
| <span data-ttu-id="d4580-178">pc</span><span class="sxs-lookup"><span data-stu-id="d4580-178">pc</span></span>                 | <span data-ttu-id="d4580-179">Cambio de paleta</span><span class="sxs-lookup"><span data-stu-id="d4580-179">Palette change</span></span>           |
| <span data-ttu-id="d4580-180">Pulsa</span><span class="sxs-lookup"><span data-stu-id="d4580-180">wb</span></span>                 | <span data-ttu-id="d4580-181">Datos de audio</span><span class="sxs-lookup"><span data-stu-id="d4580-181">Audio data</span></span>               |



 

<span data-ttu-id="d4580-182">Por ejemplo, si la secuencia 0 contiene audio, los fragmentos de datos de esa secuencia tendrían el valor de FOURCC ' 00wb '.</span><span class="sxs-lookup"><span data-stu-id="d4580-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="d4580-183">Si el flujo 1 contiene vídeo, los fragmentos de datos de esa secuencia tendrían el FOURCC ' 01dB ' o ' 01dc '.</span><span class="sxs-lookup"><span data-stu-id="d4580-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="d4580-184">Los fragmentos de datos de vídeo también pueden definir nuevas entradas de la paleta para actualizar la paleta durante una secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="d4580-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="d4580-185">Cada fragmento de cambio de paleta (' xxpc ') contiene una estructura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) .</span><span class="sxs-lookup"><span data-stu-id="d4580-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="d4580-186">Si una secuencia contiene cambios de paleta, establezca la marca **AVISF \_ video \_ PALCHANGES** en el miembro **dwFlags** de la estructura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) para esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="d4580-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="d4580-187">Los flujos de texto pueden usar códigos de dos caracteres arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="d4580-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="d4580-188">Entradas de índice AVI</span><span class="sxs-lookup"><span data-stu-id="d4580-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="d4580-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Índice de AVI 1,0</span><span class="sxs-lookup"><span data-stu-id="d4580-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="d4580-190">Un fragmento de índice opcional (' idx1 ') puede seguir la lista ' movi '.</span><span class="sxs-lookup"><span data-stu-id="d4580-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="d4580-191">El índice contiene una lista de los fragmentos de datos y su ubicación en el archivo.</span><span class="sxs-lookup"><span data-stu-id="d4580-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="d4580-192">Consta de una estructura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) con entradas para cada fragmento de datos, incluidos fragmentos "REC".</span><span class="sxs-lookup"><span data-stu-id="d4580-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="d4580-193">Si el archivo contiene un índice, establezca la marca **AVIF \_ HASINDEX** en el miembro **DwFlags** de la estructura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="d4580-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4580-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Índice de AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="d4580-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="d4580-195">Un índice AVI 2,0 puede aparecer como un solo fragmento.</span><span class="sxs-lookup"><span data-stu-id="d4580-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="d4580-196">Como alternativa, los segmentos de índice se pueden intercalar dentro del fragmento ' movi '.</span><span class="sxs-lookup"><span data-stu-id="d4580-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="d4580-197">Si los segmentos del índice se colocan en el fragmento "movi", un superíndice contiene un índice de los segmentos del índice.</span><span class="sxs-lookup"><span data-stu-id="d4580-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="d4580-198">La estructura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) es la estructura base de los segmentos de índice y del superíndice.</span><span class="sxs-lookup"><span data-stu-id="d4580-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="d4580-199">Para obtener más información, vea las *extensiones de formato de archivo AVI de OpenDML*, publicadas por el Subcomité formato de archivo AVI M-JPEG de OpenDML.</span><span class="sxs-lookup"><span data-stu-id="d4580-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="d4580-200">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="d4580-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="d4580-201">Otros fragmentos de datos</span><span class="sxs-lookup"><span data-stu-id="d4580-201">Other Data Chunks</span></span>

<span data-ttu-id="d4580-202">Los datos se pueden alinear en un archivo AVI insertando fragmentos ' no deseado ' según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d4580-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="d4580-203">Las aplicaciones deben omitir el contenido de un fragmento de "correo no deseado".</span><span class="sxs-lookup"><span data-stu-id="d4580-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4580-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4580-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4580-205">Formato de archivo AVI</span><span class="sxs-lookup"><span data-stu-id="d4580-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
