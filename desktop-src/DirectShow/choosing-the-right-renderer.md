---
description: Elección del representador de vídeo correcto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Elección del representador de vídeo correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677193"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="da6f9-103">Elección del representador de vídeo correcto</span><span class="sxs-lookup"><span data-stu-id="da6f9-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="da6f9-104">DirectShow proporciona varios filtros de representador de vídeo, resumidos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="da6f9-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="da6f9-105">Filter</span><span class="sxs-lookup"><span data-stu-id="da6f9-105">Filter</span></span>                                                                  | <span data-ttu-id="da6f9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da6f9-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="da6f9-107">[**Representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="da6f9-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="da6f9-108">Usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="da6f9-108">Uses Direct3D 9.</span></span> <span data-ttu-id="da6f9-109">Requiere Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="da6f9-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="da6f9-110">[Procesador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="da6f9-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="da6f9-111">Usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="da6f9-111">Uses Direct3D 9.</span></span> <span data-ttu-id="da6f9-112">Requiere Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="da6f9-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="da6f9-113">[Filtro de combinación de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="da6f9-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="da6f9-114">Utiliza DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="da6f9-114">Uses DirectDraw.</span></span> <span data-ttu-id="da6f9-115">Requiere Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="da6f9-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="da6f9-116">Mezclador de superposición</span><span class="sxs-lookup"><span data-stu-id="da6f9-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="da6f9-117">Admite superposiciones de hardware a través de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="da6f9-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="da6f9-118">Filtro de [representador de vídeo](video-renderer-filter.md) heredado.</span><span class="sxs-lookup"><span data-stu-id="da6f9-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="da6f9-119">Utiliza DirectDraw o (rara vez) GDI</span><span class="sxs-lookup"><span data-stu-id="da6f9-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="da6f9-120">El representador que se va a usar depende en gran medida de las versiones de Windows que necesite admitir.</span><span class="sxs-lookup"><span data-stu-id="da6f9-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="da6f9-121">En Windows Vista y versiones posteriores, las aplicaciones deben usar EVR si el hardware lo admite.</span><span class="sxs-lookup"><span data-stu-id="da6f9-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="da6f9-122">De lo contrario, revertir a VMR-9 o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="da6f9-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="da6f9-123">EVR ofrece un mejor rendimiento y una mejor calidad de vídeo que los representadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="da6f9-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="da6f9-124">Además, está diseñado para funcionar con el Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="da6f9-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="da6f9-125">Antes de Windows Vista, use VMR-9 Si el hardware lo admite y la funcionalidad de puerto de vídeo no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="da6f9-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="da6f9-126">De lo contrario, use VMR-7.</span><span class="sxs-lookup"><span data-stu-id="da6f9-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="da6f9-127">En sistemas más antiguos, es posible que tenga que usar el mezclador de superposición (para la compatibilidad con el puerto de vídeo o la superposición de hardware) o el filtro de representador de vídeo heredado.</span><span class="sxs-lookup"><span data-stu-id="da6f9-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="da6f9-128">Los métodos [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) y [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usan de forma predeterminada VMR-7.</span><span class="sxs-lookup"><span data-stu-id="da6f9-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="da6f9-129">Si el hardware no admite la versión VMR-7, estos métodos se revierten al filtro de representador de vídeo heredado.</span><span class="sxs-lookup"><span data-stu-id="da6f9-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="da6f9-130">EVR y VMR-9 nunca son los representadores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="da6f9-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da6f9-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da6f9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da6f9-132">Representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="da6f9-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



