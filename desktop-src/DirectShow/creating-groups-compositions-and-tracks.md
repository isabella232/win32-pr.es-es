---
description: Creación de composiciones y seguimientos de grupos
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: Creación de composiciones y seguimientos de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906856"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="f0184-103">Creación de composiciones y seguimientos de grupos</span><span class="sxs-lookup"><span data-stu-id="f0184-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="f0184-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f0184-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f0184-105">Los grupos, las composiciones y las pistas son las capas intermedias entre la escala de tiempo y los clips de origen.</span><span class="sxs-lookup"><span data-stu-id="f0184-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="f0184-106">Se distinguen por el tipo de objeto que pueden contener.</span><span class="sxs-lookup"><span data-stu-id="f0184-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="f0184-107">Las pistas contienen objetos de origen.</span><span class="sxs-lookup"><span data-stu-id="f0184-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="f0184-108">Las composiciones contienen pistas y otras composiciones, pero no objetos de origen.</span><span class="sxs-lookup"><span data-stu-id="f0184-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="f0184-109">Los grupos son composiciones de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="f0184-109">Groups are top-level compositions.</span></span> <span data-ttu-id="f0184-110">Los grupos contienen composiciones y pistas, pero las composiciones no pueden contener grupos.</span><span class="sxs-lookup"><span data-stu-id="f0184-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="f0184-111">Una *pista virtual* es cualquier objeto que puede residir dentro de una composición o un grupo.</span><span class="sxs-lookup"><span data-stu-id="f0184-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="f0184-112">Esto incluye las pistas y las composiciones.</span><span class="sxs-lookup"><span data-stu-id="f0184-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="f0184-113">Estos objetos exponen las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="f0184-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="f0184-114">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f0184-114">Interface</span></span>                                                  | <span data-ttu-id="f0184-115">Expuesto por</span><span class="sxs-lookup"><span data-stu-id="f0184-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="f0184-116">**IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="f0184-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="f0184-117">Pistas</span><span class="sxs-lookup"><span data-stu-id="f0184-117">Tracks</span></span>               |
| [<span data-ttu-id="f0184-118">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="f0184-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="f0184-119">Pistas, composiciones</span><span class="sxs-lookup"><span data-stu-id="f0184-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="f0184-120">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="f0184-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="f0184-121">Composiciones, grupos</span><span class="sxs-lookup"><span data-stu-id="f0184-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="f0184-122">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="f0184-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="f0184-123">Grupos</span><span class="sxs-lookup"><span data-stu-id="f0184-123">Groups</span></span>               |



 

<span data-ttu-id="f0184-124">Estas interfaces contienen los métodos para agregar objetos a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0184-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="f0184-125">[**IAMTimeline:: addgroup**](iamtimeline-addgroup.md): inserta un grupo en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0184-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="f0184-126">[**IAMTimelineComp:: VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): inserta una pista virtual en una composición o un grupo.</span><span class="sxs-lookup"><span data-stu-id="f0184-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="f0184-127">[**IAMTimelineTrack:: SrcAdd**](iamtimelinetrack-srcadd.md): inserta un origen en una pista.</span><span class="sxs-lookup"><span data-stu-id="f0184-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="f0184-128">Por ejemplo, el código siguiente inserta una nueva pista en un grupo.</span><span class="sxs-lookup"><span data-stu-id="f0184-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="f0184-129">Como se muestra en la tabla anterior, un grupo se considera un tipo de composición y una pista es un tipo de pista virtual. Por lo tanto, para insertar la pista en el grupo, debe consultar el grupo de su interfaz **IAMTimelineComp** y llamar al método **IAMTimelineComp:: VTrackInsBefore** .</span><span class="sxs-lookup"><span data-stu-id="f0184-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="f0184-130">El segundo parámetro de **VTrackInsBefore** especifica la prioridad de la pista virtual. Los niveles de prioridad comienzan en cero.</span><span class="sxs-lookup"><span data-stu-id="f0184-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="f0184-131">Si especifica el valor-1, se insertará la pista virtual al final de la lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="f0184-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="f0184-132">Si especifica un valor en el que ya existe una pista virtual, todo desde ese punto se desplaza hacia abajo en la lista en un nivel de prioridad.</span><span class="sxs-lookup"><span data-stu-id="f0184-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="f0184-133">No inserte una pista virtual con una prioridad mayor que el número de pistas virtuales, porque provocará un comportamiento no definido.</span><span class="sxs-lookup"><span data-stu-id="f0184-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="f0184-134">Para eliminar un objeto de forma permanente de la escala de tiempo, llame a [**IAMTimelineObj:: RemoveAll**](iamtimelineobj-removeall.md) en el objeto.</span><span class="sxs-lookup"><span data-stu-id="f0184-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="f0184-135">Este método quita el objeto y todos sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f0184-135">This method removes the object and all its children.</span></span> <span data-ttu-id="f0184-136">Para quitar un objeto con el fin de volver a insertarlo en otra parte de la escala de tiempo, llame a [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f0184-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="f0184-137">A diferencia de **RemoveAll**, este método no elimina los elementos secundarios del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0184-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="f0184-138">Para quitar todo de la escala de tiempo, llame a [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md).</span><span class="sxs-lookup"><span data-stu-id="f0184-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0184-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0184-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0184-140">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="f0184-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



