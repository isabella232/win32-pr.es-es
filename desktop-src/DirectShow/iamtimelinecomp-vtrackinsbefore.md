---
description: El método VTrackInsBefore inserta una pista virtual en la composición con la prioridad especificada.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp:: VTrackInsBefore (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680969"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="df162-103">IAMTimelineComp:: VTrackInsBefore (método)</span><span class="sxs-lookup"><span data-stu-id="df162-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="df162-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="df162-104">\[Deprecated.</span></span> <span data-ttu-id="df162-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df162-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="df162-106">El `VTrackInsBefore` método inserta una pista virtual en la composición con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="df162-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="df162-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df162-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="df162-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df162-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="df162-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="df162-110">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.</span><span class="sxs-lookup"><span data-stu-id="df162-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="df162-111">*Prioridad*</span><span class="sxs-lookup"><span data-stu-id="df162-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="df162-112">Prioridad con la que se va a insertar la pista virtual, o – 1 para insertar la pista virtual al final de la lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="df162-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="df162-113">La lista prioridad determina qué clips están visibles.</span><span class="sxs-lookup"><span data-stu-id="df162-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="df162-114">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="df162-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df162-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df162-115">Return value</span></span>

<span data-ttu-id="df162-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="df162-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="df162-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="df162-117">Return code</span></span>                                                                                   | <span data-ttu-id="df162-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="df162-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="df162-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="df162-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df162-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="df162-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="df162-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df162-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df162-122">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="df162-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="df162-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="df162-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="df162-124">El objeto no es una pista virtual.</span><span class="sxs-lookup"><span data-stu-id="df162-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df162-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df162-125">Remarks</span></span>

<span data-ttu-id="df162-126">Cada pista virtual de la composición tiene un nivel de prioridad único.</span><span class="sxs-lookup"><span data-stu-id="df162-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="df162-127">Los niveles de prioridad van de 0 a *n* -1, donde *n* es el número de pistas virtuales en la composición.</span><span class="sxs-lookup"><span data-stu-id="df162-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="df162-128">En el caso de los grupos de vídeo, una pista virtual oculta cualquier pista virtual con un nivel de prioridad inferior, excepto en los lugares donde la pista está vacía o contiene una transición.</span><span class="sxs-lookup"><span data-stu-id="df162-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="df162-129">Puede considerar las pistas virtuales como capas en la composición final.</span><span class="sxs-lookup"><span data-stu-id="df162-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="df162-130">El seguimiento 1 está superpuesto a la pista 0, el seguimiento 2 se superpone a la pista 1, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="df162-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="df162-131">Si especifica-1 para el parámetro *Priority* , la pista virtual se inserta al final de la lista, con un valor de prioridad mayor que el de las pistas existentes.</span><span class="sxs-lookup"><span data-stu-id="df162-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="df162-132">Si especifica un valor de prioridad que ya existe en la composición, cada pista con una prioridad igual o mayor sube un nivel de prioridad.</span><span class="sxs-lookup"><span data-stu-id="df162-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="df162-133">**Ejemplo**: Track A tiene prioridad 0 y Track B tiene prioridad 1.</span><span class="sxs-lookup"><span data-stu-id="df162-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="df162-134">Si el seguimiento C se inserta en la prioridad 0, el seguimiento de se desplaza a la prioridad 1 y el seguimiento de B se desplaza a la prioridad 2.</span><span class="sxs-lookup"><span data-stu-id="df162-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="df162-135">Si la prioridad especificada es mayor que el número actual de pistas en la composición, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="df162-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="df162-136">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="df162-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="df162-137">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="df162-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="df162-138">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="df162-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df162-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df162-139">Requirements</span></span>



| <span data-ttu-id="df162-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="df162-140">Requirement</span></span> | <span data-ttu-id="df162-141">Value</span><span class="sxs-lookup"><span data-stu-id="df162-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df162-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df162-142">Header</span></span><br/>  | <dl> <span data-ttu-id="df162-143"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="df162-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="df162-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df162-144">Library</span></span><br/> | <dl> <span data-ttu-id="df162-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df162-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df162-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="df162-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df162-147">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="df162-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="df162-148">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="df162-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




