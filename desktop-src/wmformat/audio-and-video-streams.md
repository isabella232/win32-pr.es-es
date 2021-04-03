---
title: Secuencias de audio y vídeo
description: Secuencias de audio y vídeo
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- SDK de Windows Media Format, secuencias de audio
- Advanced Systems Format (ASF), secuencias de audio
- ASF (formato de sistemas avanzados), secuencias de audio
- SDK de Windows Media Format, secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- secuencias de audio, acerca de
- secuencias de vídeo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075653"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="ccb71-114">Secuencias de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="ccb71-114">Audio and Video Streams</span></span>

<span data-ttu-id="ccb71-115">Los tipos de secuencias más comunes que se usan en los archivos creados con el SDK de Windows Media Format son secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="ccb71-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="ccb71-116">Las representaciones digitales de los datos de audio y vídeo son complejas y ocupan grandes cantidades de memoria.</span><span class="sxs-lookup"><span data-stu-id="ccb71-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="ccb71-117">En la mayoría de los casos, el audio y el vídeo se comprimen antes de agregarse a un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ccb71-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="ccb71-118">La compresión se realiza mediante un compresor/descompresor (códec).</span><span class="sxs-lookup"><span data-stu-id="ccb71-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="ccb71-119">Con este SDK se incluyen varios códecs de Windows Media, que proporcionan una compresión de calidad excelente para los medios digitales.</span><span class="sxs-lookup"><span data-stu-id="ccb71-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="ccb71-120">Para obtener más información acerca de los códecs de Windows Media, consulte [características de códec](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="ccb71-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="ccb71-121">Muchos otros códecs están disponibles desde diversos orígenes.</span><span class="sxs-lookup"><span data-stu-id="ccb71-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="ccb71-122">Puede usar cualquier códec que desee al crear archivos ASF, pero solo los objetos de este SDK admiten directamente los códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ccb71-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="ccb71-123">Para usar otros códecs, debe comprimir los ejemplos y pasarlos al objeto escritor como datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="ccb71-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="ccb71-124">La diferencia más importante entre las secuencias de audio o vídeo y las secuencias arbitrarias es que los objetos del SDK de Windows Media Format validan las secuencias que contienen datos de audio o vídeo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ccb71-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="ccb71-125">Los flujos de datos arbitrarios no se validan automáticamente, por lo que la aplicación debe comprobar su integridad.</span><span class="sxs-lookup"><span data-stu-id="ccb71-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="ccb71-126">Las propiedades de una secuencia de audio o de vídeo se describen en el perfil que se usa para crear el archivo.</span><span class="sxs-lookup"><span data-stu-id="ccb71-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccb71-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccb71-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccb71-128">**Flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="ccb71-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="ccb71-129">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="ccb71-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="ccb71-130">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="ccb71-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




