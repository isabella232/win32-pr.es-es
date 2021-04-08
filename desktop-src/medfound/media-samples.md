---
description: Ejemplos de medios
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Ejemplos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003383"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="b1d2f-103">Ejemplos de medios (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="b1d2f-103">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b1d2f-104">Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-104">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="b1d2f-105">Los ejemplos de medios exponen la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="b1d2f-105">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="b1d2f-106">La cantidad de datos contenida en una muestra depende del componente que crea el ejemplo y del tipo de datos de los búferes.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-106">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="b1d2f-107">En el caso de los vídeos sin comprimir, un ejemplo suele contener un único fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-107">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="b1d2f-108">En el caso de audio sin comprimir, la cantidad de datos puede variar, pero normalmente una trama de audio no abarca dos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-108">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="b1d2f-109">En el caso de los datos comprimidos, es posible que estas instrucciones no se apliquen.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-109">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="b1d2f-110">Un único ejemplo puede contener varios búferes por motivos de eficacia.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-110">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="b1d2f-111">Por ejemplo, en un archivo ASF, a menudo se distribuye un fotograma de vídeo entre varios paquetes ASF.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-111">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="b1d2f-112">El origen multimedia podría leer los paquetes en varios búferes.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-112">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="b1d2f-113">En lugar de copiar cada fragmento en un búfer, el origen simplemente coloca todos los búferes en un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-113">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="b1d2f-114">Los componentes de nivel inferior pueden decidir después si se copian los búferes más pequeños en un búfer contiguo.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-114">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="b1d2f-115">Por lo general, si está escribiendo un componente de canalización, debe suponer que cualquier ejemplo puede contener más de un búfer.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-115">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="b1d2f-116">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-116">This section contains the following topics.</span></span>



| <span data-ttu-id="b1d2f-117">Tema</span><span class="sxs-lookup"><span data-stu-id="b1d2f-117">Topic</span></span>                                                        | <span data-ttu-id="b1d2f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1d2f-118">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1d2f-119">Trabajar con ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="b1d2f-119">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="b1d2f-120">Describe el comportamiento general de los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-120">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="b1d2f-121">Ejemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="b1d2f-121">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="b1d2f-122">Describe una implementación especializada de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) diseñada para contener fotogramas de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b1d2f-122">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b1d2f-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1d2f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d2f-124">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="b1d2f-124">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="b1d2f-125">Media Foundation primitivas</span><span class="sxs-lookup"><span data-stu-id="b1d2f-125">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



