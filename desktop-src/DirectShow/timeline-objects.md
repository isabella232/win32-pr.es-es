---
description: Objetos Timeline
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: Objetos Timeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669957"
---
# <a name="timeline-objects"></a><span data-ttu-id="5c07c-103">Objetos Timeline</span><span class="sxs-lookup"><span data-stu-id="5c07c-103">Timeline Objects</span></span>

<span data-ttu-id="5c07c-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="5c07c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5c07c-105">Cada tipo de objeto de la escala de tiempo (origen, seguimiento, efecto, etc.) es un objeto COM distinto.</span><span class="sxs-lookup"><span data-stu-id="5c07c-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="5c07c-106">Sin embargo, una aplicación no las crea mediante la función **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="5c07c-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="5c07c-107">En su lugar, llama al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="5c07c-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="5c07c-108">Este método crea un objeto del tipo solicitado, lo inicializa y devuelve un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="5c07c-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="5c07c-109">Para obtener más información, consulte [crear una escala de tiempo](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="5c07c-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="5c07c-110">Cada objeto Timeline expone la interfaz [**IAMTimelineObj**](iamtimelineobj.md) .</span><span class="sxs-lookup"><span data-stu-id="5c07c-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="5c07c-111">Además, los distintos tipos de objetos admiten sus propias interfaces especializadas:</span><span class="sxs-lookup"><span data-stu-id="5c07c-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="5c07c-112">Origen: [ **IAMTimelineSrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="5c07c-113">Seguimiento: [ **IAMTimelineTrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="5c07c-114">Composición: [ **IAMTimelineComp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="5c07c-115">Grupo: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="5c07c-116">Efecto: [ **IAMTimelineEffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="5c07c-117">Transición: [ **IAMTimelineTrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="5c07c-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="5c07c-118">Tenga en cuenta que los grupos son un tipo de composición, por lo que admiten [**IAMTimelineComp**](iamtimelinecomp.md), así como su propia interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="5c07c-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="5c07c-119">Además de las interfaces enumeradas anteriormente, los objetos Timeline exponen otras interfaces secundarias.</span><span class="sxs-lookup"><span data-stu-id="5c07c-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="5c07c-120">Estas interfaces determinan las relaciones entre los tipos de objeto.</span><span class="sxs-lookup"><span data-stu-id="5c07c-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="5c07c-121">Interfaz</span><span class="sxs-lookup"><span data-stu-id="5c07c-121">Interface</span></span>                                                  | <span data-ttu-id="5c07c-122">Significado</span><span class="sxs-lookup"><span data-stu-id="5c07c-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="5c07c-123">Expuesto por</span><span class="sxs-lookup"><span data-stu-id="5c07c-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="5c07c-124">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="5c07c-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="5c07c-125">El objeto es una pista virtual. Las pistas virtuales pueden residir dentro de composiciones y contener otros objetos de escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5c07c-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="5c07c-126">Composición, seguimiento</span><span class="sxs-lookup"><span data-stu-id="5c07c-126">Composition, Track</span></span>                |
| [<span data-ttu-id="5c07c-127">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="5c07c-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="5c07c-128">El objeto puede tener efectos.</span><span class="sxs-lookup"><span data-stu-id="5c07c-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="5c07c-129">Composición, seguimiento, origen</span><span class="sxs-lookup"><span data-stu-id="5c07c-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="5c07c-130">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="5c07c-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="5c07c-131">El objeto puede tener transiciones.</span><span class="sxs-lookup"><span data-stu-id="5c07c-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="5c07c-132">Composición, seguimiento</span><span class="sxs-lookup"><span data-stu-id="5c07c-132">Composition, Track</span></span>                |
| [<span data-ttu-id="5c07c-133">**IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="5c07c-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="5c07c-134">El objeto se puede dividir en dos objetos.</span><span class="sxs-lookup"><span data-stu-id="5c07c-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="5c07c-135">Seguimiento, origen, efecto, transición</span><span class="sxs-lookup"><span data-stu-id="5c07c-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5c07c-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c07c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c07c-137">Información general de los componentes de la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="5c07c-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



