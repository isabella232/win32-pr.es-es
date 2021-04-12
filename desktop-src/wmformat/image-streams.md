---
title: Flujos de imagen
description: Flujos de imagen
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- SDK de Windows Media Format, flujos de imagen
- Advanced Systems Format (ASF), stream Image
- ASF (formato de sistemas avanzados), flujos de imagen
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos de imagen, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357505"
---
# <a name="image-streams"></a><span data-ttu-id="d39c4-110">Flujos de imagen</span><span class="sxs-lookup"><span data-stu-id="d39c4-110">Image Streams</span></span>

<span data-ttu-id="d39c4-111">Un flujo de imagen es un tipo especial de flujo que contiene imágenes fijas asignadas a los tiempos de presentación.</span><span class="sxs-lookup"><span data-stu-id="d39c4-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="d39c4-112">Una aplicación puede mostrar las imágenes en una secuencia de imágenes como se desea, pero la implementación típica es mostrar cada imagen hasta que se entregue la siguiente imagen, como una presentación.</span><span class="sxs-lookup"><span data-stu-id="d39c4-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="d39c4-113">Normalmente, una secuencia de imágenes se codifica en un archivo con una secuencia de audio para generar una presentación simple de imágenes sincronizadas con música o voz.</span><span class="sxs-lookup"><span data-stu-id="d39c4-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="d39c4-114">Los flujos de imágenes son similares a las secuencias de vídeo en que se crean a partir de muestras sin comprimir que se comprimen como parte del proceso de escritura de archivos, pero también son como secuencias arbitrarias porque debe asignar una velocidad de bits y una ventana de búfer adecuados para el contenido sin depender de las propiedades asignadas por códecs.</span><span class="sxs-lookup"><span data-stu-id="d39c4-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d39c4-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d39c4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d39c4-116">**Flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="d39c4-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="d39c4-117">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="d39c4-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="d39c4-118">**Secuencias de audio y vídeo**</span><span class="sxs-lookup"><span data-stu-id="d39c4-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="d39c4-119">**Escribir secuencias de imagen**</span><span class="sxs-lookup"><span data-stu-id="d39c4-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




