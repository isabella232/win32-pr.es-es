---
description: En esta información general se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en los archivos. wav. RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Formato de archivo para intercambio de recursos (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717140"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="e69f1-104">Formato de archivo para intercambio de recursos (RIFF)</span><span class="sxs-lookup"><span data-stu-id="e69f1-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="e69f1-105">En esta información general se describe el formato de archivo de intercambio de recursos (RIFF), que se usa en los archivos. wav.</span><span class="sxs-lookup"><span data-stu-id="e69f1-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="e69f1-106">RIFF es el formato típico desde el que se cargarán los datos de audio de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e69f1-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="e69f1-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="e69f1-107">RIFF</span></span>

<span data-ttu-id="e69f1-108">Un archivo RIFF se compone de varias secciones discretas de datos denominados *fragmentos*.</span><span class="sxs-lookup"><span data-stu-id="e69f1-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="e69f1-109">Identificadores FOURCC</span><span class="sxs-lookup"><span data-stu-id="e69f1-109">FOURCC Identifiers</span></span>

<span data-ttu-id="e69f1-110">El tipo de datos de un fragmento se indica mediante un identificador de código de cuatro caracteres (FOURCC).</span><span class="sxs-lookup"><span data-stu-id="e69f1-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="e69f1-111">Un FOURCC es un entero sin signo de 32 bits creado mediante la concatenación de cuatro caracteres ASCII que se usan para identificar tipos de fragmentos en un archivo RIFF.</span><span class="sxs-lookup"><span data-stu-id="e69f1-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="e69f1-112">Por ejemplo, el FOURCC "ABCD" se representa en un sistema Little-Endian como 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="e69f1-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="e69f1-113">FOURCCs puede contener caracteres de espacio, por lo que "ABC" es un FOURCC válido.</span><span class="sxs-lookup"><span data-stu-id="e69f1-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="e69f1-114">Los archivos de audio usan códigos FOURCC para identificar fragmentos de formato de audio, fragmentos de datos de audio y cualquier otro fragmento específico del formato de audio.</span><span class="sxs-lookup"><span data-stu-id="e69f1-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="e69f1-115">En la tabla siguiente se muestran los identificadores FOURCC que se pueden esperar en los formatos de audio admitidos por XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e69f1-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="e69f1-116">Formato</span><span class="sxs-lookup"><span data-stu-id="e69f1-116">Format</span></span> | <span data-ttu-id="e69f1-117">Identificadores FOURCC</span><span class="sxs-lookup"><span data-stu-id="e69f1-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="e69f1-118">Información adicional</span><span class="sxs-lookup"><span data-stu-id="e69f1-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69f1-119">PCM</span><span class="sxs-lookup"><span data-stu-id="e69f1-119">PCM</span></span>    | <span data-ttu-id="e69f1-120">"RIFF", "FMT", "Data"</span><span class="sxs-lookup"><span data-stu-id="e69f1-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="e69f1-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="e69f1-121">ADPCM</span></span>  | <span data-ttu-id="e69f1-122">"RIFF", "FMT", "Data", "smpl", "wsmpl"</span><span class="sxs-lookup"><span data-stu-id="e69f1-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="e69f1-123">Consulte [información general de ADPCM](adpcm-overview.md) para obtener una descripción de los identificadores FourCC específicos de ADPCM.</span><span class="sxs-lookup"><span data-stu-id="e69f1-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="e69f1-124">Los identificadores de FOURCC "RIFF", "FMT" y "Data" son comunes a todos los formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="e69f1-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="e69f1-125">En la tabla siguiente se describen los identificadores FOURCC que se encuentran en todos los formatos admitidos.</span><span class="sxs-lookup"><span data-stu-id="e69f1-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="e69f1-126">Identificador FOURCC</span><span class="sxs-lookup"><span data-stu-id="e69f1-126">FOURCC identifier</span></span> | <span data-ttu-id="e69f1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="e69f1-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69f1-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="e69f1-128">"RIFF"</span></span>            | <span data-ttu-id="e69f1-129">Fragmento RIFF estándar que contiene un tipo de archivo con el valor "WAVE" o "XWMA" en los primeros cuatro bytes de su sección de datos y los demás fragmentos del archivo en el resto de los datos.</span><span class="sxs-lookup"><span data-stu-id="e69f1-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="e69f1-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="e69f1-130">"fmt"</span></span>             | <span data-ttu-id="e69f1-131">Contiene el encabezado de formato del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="e69f1-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="e69f1-132">Los datos de este fragmento se corresponden con una de las siguientes estructuras: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span><span class="sxs-lookup"><span data-stu-id="e69f1-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="e69f1-133">"data"</span><span class="sxs-lookup"><span data-stu-id="e69f1-133">"data"</span></span>            | <span data-ttu-id="e69f1-134">Contiene datos de audio para el archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="e69f1-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="e69f1-135">En XAudio2, el contenido del fragmento de datos se leerá en un búfer y se pasará a una voz de origen como el miembro **pAudioData** de una estructura de [**\_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="e69f1-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="e69f1-136">Chunks</span><span class="sxs-lookup"><span data-stu-id="e69f1-136">Chunks</span></span>

<span data-ttu-id="e69f1-137">Un archivo RIFF se compone de un fragmento RIFF que contiene cero o más fragmentos.</span><span class="sxs-lookup"><span data-stu-id="e69f1-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="e69f1-138">El fragmento RIFF tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="e69f1-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="e69f1-139">"RIFF", archivo, fileType, datos</span><span class="sxs-lookup"><span data-stu-id="e69f1-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="e69f1-140">Donde "RIFF" es el código de FOURCC literal "RIFF" *, el tamaño de archivo es* un valor de 4 bytes que asigna el tamaño de los datos en el archivo y *FILETYPE* es un FourCC que identifica el tipo de archivo específico.</span><span class="sxs-lookup"><span data-stu-id="e69f1-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="e69f1-141">El valor de *fileing* incluye el tamaño de *filetype* FourCC más el tamaño de los datos siguientes, pero no incluye el tamaño del FourCC "Riff" o el tamaño de *los archivos*.</span><span class="sxs-lookup"><span data-stu-id="e69f1-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="e69f1-142">Los datos se componen de fragmentos en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="e69f1-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="e69f1-143">Otros fragmentos tienen el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="e69f1-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="e69f1-144">Donde *chunkID* es un FourCC que identifica los datos contenidos en el fragmento, *chunkSize* es un valor de 4 bytes que asigna el tamaño de la sección de datos del fragmento y los datos son cero o más bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="e69f1-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="e69f1-145">Los datos siempre se rellenan hasta el límite de palabras más cercano.</span><span class="sxs-lookup"><span data-stu-id="e69f1-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="e69f1-146">*chunkSize* proporciona el tamaño de los datos válidos en el fragmento.</span><span class="sxs-lookup"><span data-stu-id="e69f1-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="e69f1-147">No incluye el relleno, el tamaño de *chunkID* o el tamaño de *chunkSize*.</span><span class="sxs-lookup"><span data-stu-id="e69f1-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e69f1-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e69f1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e69f1-149">Introducción</span><span class="sxs-lookup"><span data-stu-id="e69f1-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="e69f1-150">Cómo: reproducir un sonido con XAudio2</span><span class="sxs-lookup"><span data-stu-id="e69f1-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="e69f1-151">Referencia de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e69f1-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



