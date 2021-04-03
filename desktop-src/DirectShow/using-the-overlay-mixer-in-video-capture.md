---
description: Usar el mezclador de superposición en la captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Usar el mezclador de superposición en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082949"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="79a04-103">Usar el mezclador de superposición en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="79a04-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="79a04-104">Hay determinados tipos de vídeo que el filtro de [representador de vídeo](video-renderer-filter.md) no puede mostrar por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="79a04-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="79a04-105">En estas situaciones, el representador de vídeo debe trabajar con el filtro de [mezclador de superposición](overlay-mixer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="79a04-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="79a04-106">El mezclador de superposición administra la representación, mientras que el representador de vídeo administra la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a04-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="79a04-107">El mezclador de superposición es necesario en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="79a04-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="79a04-108">Clavijas del puerto de vídeo (VP).</span><span class="sxs-lookup"><span data-stu-id="79a04-108">Video port (VP) pins.</span></span> <span data-ttu-id="79a04-109">Si el dispositivo de captura usa un puerto de vídeo, el mezclador de superposición administra la superposición de hardware.</span><span class="sxs-lookup"><span data-stu-id="79a04-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="79a04-110">Vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="79a04-110">Interlaced video.</span></span> <span data-ttu-id="79a04-111">En el caso del vídeo entrelazado, el descodificador requiere un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , que no es compatible con el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a04-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="79a04-112">Subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="79a04-112">Closed captions.</span></span> <span data-ttu-id="79a04-113">El texto de la leyenda se representa como mapa de bits de 8 bits por píxel, que el mezclador de superposición se superpone en el vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a04-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="79a04-114">El método **RenderStream** del generador de gráficos de captura inserta el mezclador de superposición siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="79a04-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="79a04-115">Sin embargo, si va a compilar el gráfico sin usar el generador de gráficos de captura, debe comprobar cada una de estas situaciones e insertar el mezclador de superposición usted mismo.</span><span class="sxs-lookup"><span data-stu-id="79a04-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="79a04-116">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="79a04-116">\[!Important\]</span></span>  
    > <span data-ttu-id="79a04-117">Si el dispositivo tiene una VP, debe conectar el mezclador de superposición, incluso si no necesita la funcionalidad de versión preliminar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="79a04-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="79a04-118">Con un puerto de vídeo, el dispositivo de captura siempre envía los datos de vídeo a la superposición de hardware, por lo que siempre es necesario el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="79a04-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="79a04-119">Los filtros de representador de combinación de vídeo (VMR-7 y VMR-9) admiten vídeo entrelazado y pueden mezclar mapas de bits de subtítulos cerrados en el vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="79a04-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="79a04-120">Si usa la VMR para esos escenarios, no es necesario usar el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="79a04-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="79a04-121">VMR-9 no es compatible con las conexiones de VP PIN.</span><span class="sxs-lookup"><span data-stu-id="79a04-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="79a04-122">VMR-7 admite las conexiones de VP PIN a través del filtro del administrador de puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a04-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="79a04-123">Sin embargo, es posible que algunos controladores no funcionen correctamente con el administrador de puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a04-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="79a04-124">Por ese motivo, todavía se recomienda usar el mezclador de superposición para VICEPRESIDENTEs.</span><span class="sxs-lookup"><span data-stu-id="79a04-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79a04-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79a04-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79a04-126">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="79a04-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="79a04-127">PIN de puerto de vídeo</span><span class="sxs-lookup"><span data-stu-id="79a04-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="79a04-128">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="79a04-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



