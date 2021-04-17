---
description: Los códecs de Windows Media Audio y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Códecs de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697978"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="fb690-103">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="fb690-103">Windows Media Codecs</span></span>

<span data-ttu-id="fb690-104">Los códecs de Windows Media Audio y vídeo son una colección de objetos que puede usar para comprimir y descomprimir datos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="fb690-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="fb690-105">Cada códec consta de dos objetos, un codificador y un descodificador.</span><span class="sxs-lookup"><span data-stu-id="fb690-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="fb690-106">En esta parte de la documentación se describe cómo usar las características de los códecs de Windows Media Audio y vídeo para generar y consumir flujos de datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="fb690-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="fb690-107">Esta documentación está dirigida principalmente a los desarrolladores que quieren usar códecs de Windows Media en sus aplicaciones multimedia basadas en C++.</span><span class="sxs-lookup"><span data-stu-id="fb690-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="fb690-108">Para obtener información general técnica de las características de los códecs de Windows Media, consulte [acerca de los códecs de Windows Media](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="fb690-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="fb690-109">El término *codec* es una fusión de los términos compresor y descompresor.</span><span class="sxs-lookup"><span data-stu-id="fb690-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="fb690-110">Normalmente, un códec se implementa como un par de objetos COM: uno para codificar el contenido y otro para descodificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="fb690-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="fb690-111">En algunos casos, los objetos COM ocupan la misma biblioteca vinculada dinámicamente (DLL).</span><span class="sxs-lookup"><span data-stu-id="fb690-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="fb690-112">Cada objeto codec implementa dos interfaces independientes pero similares:</span><span class="sxs-lookup"><span data-stu-id="fb690-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="fb690-113">Interfaz</span><span class="sxs-lookup"><span data-stu-id="fb690-113">Interface</span></span>                              | <span data-ttu-id="fb690-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb690-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="fb690-115">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="fb690-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="fb690-116">Compatible con Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fb690-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="fb690-117">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="fb690-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="fb690-118">Compatible con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fb690-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="fb690-119">No solo hay códecs diferentes para audio y vídeo, sino también distintos códecs para diferentes tipos de contenido que puede incluir en un archivo de audio o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb690-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="fb690-120">Los algoritmos que se usan para comprimir y descomprimir datos de palabras pronunciadas difieren de los algoritmos usados para comprimir y descomprimir los datos de música.</span><span class="sxs-lookup"><span data-stu-id="fb690-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="fb690-121">Descripciones de códecs</span><span class="sxs-lookup"><span data-stu-id="fb690-121">Codec Descriptions</span></span>

<span data-ttu-id="fb690-122">En la tabla siguiente se describen los usos previstos de los códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fb690-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="fb690-123">Códec</span><span class="sxs-lookup"><span data-stu-id="fb690-123">Codec</span></span>                                                                     | <span data-ttu-id="fb690-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb690-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb690-125">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="fb690-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="fb690-126">Un códec de audio que admite tres categorías de contenido codificado: estándar, profesional y sin pérdida de información.</span><span class="sxs-lookup"><span data-stu-id="fb690-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="fb690-127">Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="fb690-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="fb690-128">Códec de audio optimizado para codificar las proporciones de la voz humana a alta compresión.</span><span class="sxs-lookup"><span data-stu-id="fb690-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="fb690-129">Este es el códec preferido para las secuencias que se componen principalmente de palabras pronunciadas.</span><span class="sxs-lookup"><span data-stu-id="fb690-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="fb690-130">En el caso de contenido que está mezclado con música y voz, este códec puede cambiar dinámicamente el algoritmo de codificación utilizado para obtener una calidad óptima.</span><span class="sxs-lookup"><span data-stu-id="fb690-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="fb690-131">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fb690-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="fb690-132">Un códec de vídeo que admite cuatro categorías de contenido codificado: perfil simple, perfil principal, perfil avanzado e imagen.</span><span class="sxs-lookup"><span data-stu-id="fb690-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="fb690-133">Pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="fb690-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="fb690-134">Códec de vídeo optimizado para codificar capturas de pantalla secuenciales desde monitores de equipos.</span><span class="sxs-lookup"><span data-stu-id="fb690-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="fb690-135">Este códec se usa a menudo para aprendizaje o soporte técnico de software mediante la grabación de imágenes de supervisión mientras se usan las aplicaciones para equipos.</span><span class="sxs-lookup"><span data-stu-id="fb690-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="fb690-136">Las versiones más recientes de los objetos codec también habilitan el acceso a algunos códecs heredados, como Windows Media Video 7 y 8, Windows Media screen 7, los códecs MPEG-4 de Microsoft anteriores y los códecs ISO MPEG-4 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb690-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="fb690-137">En esta documentación no se tratan estos códecs heredados; solo incluye las versiones actuales de los códecs.</span><span class="sxs-lookup"><span data-stu-id="fb690-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="fb690-138">En el caso de los códecs anteriores, utilice los mismos procedimientos que al usar los códecs actuales; sin embargo, recuerde que no todas las características se admiten en todos los códecs.</span><span class="sxs-lookup"><span data-stu-id="fb690-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb690-139">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fb690-139">In this section</span></span>

-   [<span data-ttu-id="fb690-140">Acerca de los códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="fb690-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="fb690-141">Usar el códec y los objetos DSP</span><span class="sxs-lookup"><span data-stu-id="fb690-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="fb690-142">Métodos de codificación</span><span class="sxs-lookup"><span data-stu-id="fb690-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="fb690-143">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="fb690-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="fb690-144">El modelo de búfer de depósito con fugas</span><span class="sxs-lookup"><span data-stu-id="fb690-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="fb690-145">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="fb690-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="fb690-146">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="fb690-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="fb690-147">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="fb690-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="fb690-148">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="fb690-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="fb690-149">Almacenar medios comprimidos en archivos AVI</span><span class="sxs-lookup"><span data-stu-id="fb690-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="fb690-150">Usar la codificación VBR</span><span class="sxs-lookup"><span data-stu-id="fb690-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="fb690-151">Uso de la codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="fb690-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="fb690-152">Obtener estadísticas de codificación</span><span class="sxs-lookup"><span data-stu-id="fb690-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="fb690-153">Uso de extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="fb690-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="fb690-154">Constantes IPropertyBag de códec y DSP</span><span class="sxs-lookup"><span data-stu-id="fb690-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="fb690-155">Analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="fb690-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="fb690-156">Preguntas más frecuentes sobre códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="fb690-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="fb690-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb690-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb690-158">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb690-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="fb690-159">[Tecnologías multimedia para Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="fb690-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
