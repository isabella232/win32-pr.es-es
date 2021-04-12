---
title: Formatos
description: Formatos
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, entradas
- Windows Media Format SDK, secuencias
- Windows Media Format SDK, salidas
- Windows Media Format SDK, formatos
- Advanced Systems Format (ASF), INPUTS
- ASF (formato de sistemas avanzados), entradas
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- Advanced Systems Format (ASF), salidas
- ASF (formato de sistemas avanzados), salidas
- Advanced Systems Format (ASF), Formats
- ASF (formato de sistemas avanzados), formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357475"
---
# <a name="formats"></a><span data-ttu-id="16b93-115">Formatos</span><span class="sxs-lookup"><span data-stu-id="16b93-115">Formats</span></span>

<span data-ttu-id="16b93-116">La información en un formato describe todo lo que necesita saber sobre un tipo de medio determinado.</span><span class="sxs-lookup"><span data-stu-id="16b93-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="16b93-117">Cada formato tiene un tipo principal, como audio o vídeo, y puede tener un subtipo.</span><span class="sxs-lookup"><span data-stu-id="16b93-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="16b93-118">Los formatos contienen información diferente en función del tipo principal.</span><span class="sxs-lookup"><span data-stu-id="16b93-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="16b93-119">Los formatos de audio y vídeo requieren mucha más información que otros tipos.</span><span class="sxs-lookup"><span data-stu-id="16b93-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="16b93-120">Del mismo modo que los objetos del SDK de Windows Media Format diferencian entre los números de entrada, los números de flujo y los números de salida (vea [entradas, secuencias y salidas](inputs-streams-and-outputs.md)), existen diferencias importantes entre los formatos de entrada, los formatos de flujo y los formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="16b93-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="16b93-121">Estas diferencias se describen aquí:</span><span class="sxs-lookup"><span data-stu-id="16b93-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="16b93-122">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="16b93-122">Input Formats</span></span>

<span data-ttu-id="16b93-123">Un formato de entrada describe los medios digitales que se pasan al objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="16b93-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="16b93-124">Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="16b93-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="16b93-125">Al usar los códecs de Windows Media Audio y vídeo, puede enumerar los formatos de entrada admitidos mediante el objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="16b93-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="16b93-126">Al escribir un archivo, usted es responsable de seleccionar un formato de entrada que coincida con los medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="16b93-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="16b93-127">Aunque el formato del medio de entrada debe ser compatible con el códec que comprimirá los datos, es necesario que algunos valores de configuración de formato de entrada no coincidan con el formato de flujo.</span><span class="sxs-lookup"><span data-stu-id="16b93-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="16b93-128">Por ejemplo, el formato de entrada de un flujo de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de flujo.</span><span class="sxs-lookup"><span data-stu-id="16b93-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="16b93-129">El códec realizará las conversiones en estos casos.</span><span class="sxs-lookup"><span data-stu-id="16b93-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="16b93-130">Formatos de secuencia</span><span class="sxs-lookup"><span data-stu-id="16b93-130">Stream Formats</span></span>

<span data-ttu-id="16b93-131">Un formato de secuencia describe la forma del medio tal como se almacena en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="16b93-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="16b93-132">El formato de flujo es el formato descrito en el perfil y puede o no ser el mismo que el formato de entrada y el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="16b93-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="16b93-133">Si se usa un códec para comprimir los datos de una secuencia, el formato del flujo será diferente de los formatos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="16b93-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="16b93-134">Al usar los códecs de Windows Media Audio y vídeo, debe obtener una lista de formatos de secuencia compatibles del códec para asegurarse de que no está intentando especificar un formato no admitido por el código.</span><span class="sxs-lookup"><span data-stu-id="16b93-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="16b93-135">Algunos valores de configuración de formato, como el tamaño y la profundidad de color de un fotograma de vídeo, deben configurarse manualmente una vez recuperado el formato del códec.</span><span class="sxs-lookup"><span data-stu-id="16b93-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="16b93-136">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="16b93-136">Output Formats</span></span>

<span data-ttu-id="16b93-137">Un formato de salida describe el medio digital que el lector (o lector sincrónico) entrega a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="16b93-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="16b93-138">Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="16b93-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="16b93-139">Al usar los códecs de Windows Media Audio y vídeo, puede enumerar los formatos de salida admitidos mediante el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="16b93-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="16b93-140">Cada uno de los códecs de Windows Media tiene un formato de salida predeterminado, pero puede seleccionar cualquier formato de salida compatible para la entrega de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="16b93-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="16b93-141">Aunque el formato del medio de salida debe ser compatible con el códec que ha comprimido los datos, no es necesario que alguna configuración de formato de salida coincida con el formato de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="16b93-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="16b93-142">Por ejemplo, el formato de salida de una secuencia de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de flujo.</span><span class="sxs-lookup"><span data-stu-id="16b93-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="16b93-143">El códec realizará las conversiones en estos casos.</span><span class="sxs-lookup"><span data-stu-id="16b93-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16b93-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16b93-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b93-145">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="16b93-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




