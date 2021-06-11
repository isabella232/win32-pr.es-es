---
description: Obtenga información sobre los ejemplos de medios en Microsoft Media Foundation. Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Ejemplos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989160"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="374a8-104">Ejemplos de medios (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="374a8-104">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="374a8-105">Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.</span><span class="sxs-lookup"><span data-stu-id="374a8-105">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="374a8-106">Los ejemplos de medios exponen la [**interfaz DESAMPLESample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)</span><span class="sxs-lookup"><span data-stu-id="374a8-106">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="374a8-107">La cantidad de datos contenidos en una muestra depende del componente que crea la muestra y del tipo de datos de los búferes.</span><span class="sxs-lookup"><span data-stu-id="374a8-107">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="374a8-108">En el caso del vídeo sin comprimir, un ejemplo suele contener un único fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="374a8-108">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="374a8-109">En el caso del audio sin comprimir, la cantidad de datos puede variar, pero normalmente un fotograma de audio no abarca dos muestras.</span><span class="sxs-lookup"><span data-stu-id="374a8-109">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="374a8-110">En el caso de los datos comprimidos, es posible que estas directrices no se apliquen.</span><span class="sxs-lookup"><span data-stu-id="374a8-110">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="374a8-111">Una sola muestra puede contener varios búferes por motivos de eficiencia.</span><span class="sxs-lookup"><span data-stu-id="374a8-111">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="374a8-112">Por ejemplo, en un archivo ASF, un fotograma de vídeo a menudo se distribuye entre varios paquetes ASF.</span><span class="sxs-lookup"><span data-stu-id="374a8-112">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="374a8-113">El origen de medios podría leer los paquetes en varios búferes.</span><span class="sxs-lookup"><span data-stu-id="374a8-113">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="374a8-114">En lugar de copiar cada fragmento en un búfer, el origen simplemente coloca todos los búferes en una muestra.</span><span class="sxs-lookup"><span data-stu-id="374a8-114">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="374a8-115">Los componentes de nivel inferior pueden decidir si se copian los búferes más pequeños en un búfer contiguo.</span><span class="sxs-lookup"><span data-stu-id="374a8-115">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="374a8-116">Por lo general, si está escribiendo un componente de canalización, debe suponer que cualquier ejemplo puede contener más de un búfer.</span><span class="sxs-lookup"><span data-stu-id="374a8-116">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="374a8-117">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="374a8-117">This section contains the following topics.</span></span>



| <span data-ttu-id="374a8-118">Tema</span><span class="sxs-lookup"><span data-stu-id="374a8-118">Topic</span></span>                                                        | <span data-ttu-id="374a8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="374a8-119">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="374a8-120">Trabajar con ejemplos multimedia</span><span class="sxs-lookup"><span data-stu-id="374a8-120">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="374a8-121">Describe el comportamiento general de los ejemplos multimedia.</span><span class="sxs-lookup"><span data-stu-id="374a8-121">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="374a8-122">Ejemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="374a8-122">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="374a8-123">Describe una implementación especializada [**deSAMPLESample diseñada**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para contener fotogramas de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="374a8-123">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="374a8-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="374a8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="374a8-125">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="374a8-125">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="374a8-126">Media Foundation primitivos</span><span class="sxs-lookup"><span data-stu-id="374a8-126">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



