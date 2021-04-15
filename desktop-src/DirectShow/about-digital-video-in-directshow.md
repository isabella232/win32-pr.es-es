---
description: Acerca de vídeo digital en DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Acerca de vídeo digital en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569409"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="a4869-103">Acerca de vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4869-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="a4869-104">El vídeo digital (DV) se puede capturar desde una cámara DV, almacenarse en un archivo en el equipo del usuario o almacenarse en cinta con una grabadora de cintas de vídeo (VTR).</span><span class="sxs-lookup"><span data-stu-id="a4869-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="a4869-105">Por lo tanto, las operaciones que puede realizar una aplicación en una secuencia DV incluyen:</span><span class="sxs-lookup"><span data-stu-id="a4869-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="a4869-106">Capturar vídeo en directo desde una cámara DV.</span><span class="sxs-lookup"><span data-stu-id="a4869-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="a4869-107">Transmita datos DV desde cinta VTR al equipo.</span><span class="sxs-lookup"><span data-stu-id="a4869-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="a4869-108">Transmita datos de DV del equipo al VTR.</span><span class="sxs-lookup"><span data-stu-id="a4869-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="a4869-109">Leer datos de DV desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="a4869-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="a4869-110">Escribir datos de DV en un archivo.</span><span class="sxs-lookup"><span data-stu-id="a4869-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="a4869-111">Representar el audio y el vídeo en un flujo DV.</span><span class="sxs-lookup"><span data-stu-id="a4869-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="a4869-112">DirectShow proporciona los siguientes filtros DV:</span><span class="sxs-lookup"><span data-stu-id="a4869-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="a4869-113">[Controlador MSDV](msdv-driver.md).</span><span class="sxs-lookup"><span data-stu-id="a4869-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="a4869-114">El controlador MSDV controla un dispositivo DV, como una videocámara.</span><span class="sxs-lookup"><span data-stu-id="a4869-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="a4869-115">El dispositivo puede tener una subunidad de cámara y una subunidad de VTR; MSDV controla ambas subunidads.</span><span class="sxs-lookup"><span data-stu-id="a4869-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="a4869-116">El controlador MSDV aparece en las aplicaciones como un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a4869-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="a4869-117">Filtro de [divisor DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a4869-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="a4869-118">Los fotogramas DV contienen audio y vídeo en el mismo fotograma.</span><span class="sxs-lookup"><span data-stu-id="a4869-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="a4869-119">El filtro de divisor DV extrae los datos de audio y los envía como uno o dos flujos de audio.</span><span class="sxs-lookup"><span data-stu-id="a4869-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="a4869-120">Genera los datos originales como una secuencia de vídeo DV independiente.</span><span class="sxs-lookup"><span data-stu-id="a4869-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="a4869-121">Filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a4869-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="a4869-122">Descodifica vídeo DV en vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a4869-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="a4869-123">Filtro de [codificador de vídeo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a4869-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="a4869-124">Codifica vídeo sin comprimir en vídeo codificado en DV.</span><span class="sxs-lookup"><span data-stu-id="a4869-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="a4869-125">[DV multiplexor](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a4869-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="a4869-126">Combina una secuencia de vídeo DV con uno o dos flujos de audio para crear una única secuencia DV intercalada.</span><span class="sxs-lookup"><span data-stu-id="a4869-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="a4869-127">El divisor de DV y el descodificador de vídeo DV funcionan juntos.</span><span class="sxs-lookup"><span data-stu-id="a4869-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="a4869-128">El divisor toma el flujo intercalado y genera secuencias de vídeo de audio y DV independientes.</span><span class="sxs-lookup"><span data-stu-id="a4869-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="a4869-129">El descodificador convierte el vídeo DV en vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a4869-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="a4869-130">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="a4869-130">The following image illustrates this process.</span></span>

![divisor DV y descodificador DV](images/dv-filters1.png)

<span data-ttu-id="a4869-132">El codificador de vídeo DV y el multiplexor DV invierten el proceso: el codificador convierte el vídeo sin comprimir en vídeo DV y el MUX combina audio y vídeo DV para crear una única secuencia intercalada, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4869-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![codificador DV y DV multiplexor](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="a4869-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4869-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4869-135">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4869-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



