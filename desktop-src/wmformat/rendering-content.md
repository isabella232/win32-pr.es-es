---
title: Representación de contenido
description: Representación de contenido
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- SDK de Windows Media Format, representación de contenido
- Advanced Systems Format (ASF), representación de contenido
- ASF (formato de sistemas avanzados), representación de contenido
- Advanced Systems Format (ASF), representación de contenido
- ASF (formato de sistemas avanzados), representación de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903826"
---
# <a name="rendering-content"></a><span data-ttu-id="7620f-108">Representación de contenido</span><span class="sxs-lookup"><span data-stu-id="7620f-108">Rendering Content</span></span>

<span data-ttu-id="7620f-109">El SDK de Windows Media Format no proporciona rutinas para representar el contenido entregado por el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="7620f-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="7620f-110">Si escribe aplicaciones para reproducir el contenido en archivos ASF, debe implementar sus propias rutinas de representación.</span><span class="sxs-lookup"><span data-stu-id="7620f-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="7620f-111">Debe tener cuidado al representar contenido para asegurarse de que los ejemplos se representan en el orden del tiempo de presentación y que los ejemplos de diferentes flujos se sincronizan cuando se representan.</span><span class="sxs-lookup"><span data-stu-id="7620f-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="7620f-112">El método que se emplea para garantizar la sincronización de la secuencia dependerá de la técnica de representación que se utilice para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7620f-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="7620f-113">En general, si tiene secuencias de audio y vídeo, debe sincronizar con la secuencia de audio, ya que la incoherencia en la secuencia de audio es más perceptible que algunos fotogramas descartados en una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7620f-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7620f-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7620f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7620f-115">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="7620f-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="7620f-116">**Para recuperar ejemplos de medios con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="7620f-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="7620f-117">**Para recuperar ejemplos de medios con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="7620f-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




