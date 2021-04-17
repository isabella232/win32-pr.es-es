---
description: La interfaz IAMTimelineComp inserta o recupera pistas virtuales en una composición en los servicios de edición de DirectShow (DES). Una composición es una colección de capas que actúa como una única pista compuesta.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaz IAMTimelineComp (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681260"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="4a0ad-103">Interfaz IAMTimelineComp</span><span class="sxs-lookup"><span data-stu-id="4a0ad-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="4a0ad-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-104">\[Deprecated.</span></span> <span data-ttu-id="4a0ad-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a0ad-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a0ad-106">La interfaz **IAMTimelineComp** inserta o recupera pistas virtuales en una composición en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4a0ad-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="4a0ad-107">Una composición es una colección de capas que actúa como una única *pista* compuesta. Por ejemplo, una composición que contiene dos pistas con una transición entre ellas actúa como una sola pista con la transición precompuesta.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="4a0ad-108">Una composición debe contener medios de un solo tipo (como audio o vídeo), pero esta limitación no se aplica.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="4a0ad-109">Una *pista virtual* es cualquier objeto que puede residir en una composición, incluidas las pistas y otras composiciones.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="4a0ad-110">Los nodos de nivel superior de la escala de tiempo son *grupos*.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="4a0ad-111">Los grupos implementan la `IAMTimelineComp` interfaz y la interfaz [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="4a0ad-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="4a0ad-112">Para crear un objeto de composición, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el tipo principal de la escala de tiempo de valor \_ \_ \_ compuesto.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="4a0ad-113">Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineComp` interfaz.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="4a0ad-114">Para obtener más información, vea [el modelo Timeline](the-timeline-model.md) y [crear una escala de tiempo](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="4a0ad-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="4a0ad-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a0ad-115">Members</span></span>

<span data-ttu-id="4a0ad-116">La interfaz **IAMTimelineComp** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a0ad-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a0ad-117">**IAMTimelineComp** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a0ad-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="4a0ad-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a0ad-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a0ad-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a0ad-119">Methods</span></span>

<span data-ttu-id="4a0ad-120">La interfaz **IAMTimelineComp** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="4a0ad-121">Método</span><span class="sxs-lookup"><span data-stu-id="4a0ad-121">Method</span></span>                                                                       | <span data-ttu-id="4a0ad-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a0ad-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a0ad-123">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="4a0ad-124">Recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="4a0ad-125">**GetNextVTrack**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="4a0ad-126">Recupera la siguiente pista virtual después de una pista virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="4a0ad-127">**GetRecursiveLayerOfType**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="4a0ad-128">Realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la *n*-ésima pista virtual de esa ordenación.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="4a0ad-129">**GetRecursiveLayerOfTypeI**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="4a0ad-130">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="4a0ad-131">**GetVTrack**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="4a0ad-132">Recupera la pista virtual con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4a0ad-133">**VTrackGetCount**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="4a0ad-134">Recupera el número de pistas virtuales contenidas en la composición.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="4a0ad-135">**VTrackInsBefore**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="4a0ad-136">Inserta una pista virtual en la composición con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="4a0ad-137">**VTrackSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="4a0ad-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="4a0ad-138">Cambia los niveles de prioridad de dos pistas.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="4a0ad-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a0ad-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a0ad-140">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a0ad-141">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a0ad-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a0ad-142">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a0ad-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a0ad-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0ad-143">Requirements</span></span>



| <span data-ttu-id="4a0ad-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a0ad-144">Requirement</span></span> | <span data-ttu-id="4a0ad-145">Value</span><span class="sxs-lookup"><span data-stu-id="4a0ad-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0ad-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a0ad-146">Header</span></span><br/>  | <dl> <span data-ttu-id="4a0ad-147"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a0ad-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a0ad-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a0ad-148">Library</span></span><br/> | <dl> <span data-ttu-id="4a0ad-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a0ad-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
