---
description: Constantes utilizadas para establecer la prioridad de un recurso en SetPriority.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280271"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="17bfc-103">Prioridad de los recursos de D3D9 \_ \_</span><span class="sxs-lookup"><span data-stu-id="17bfc-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="17bfc-104">Constantes utilizadas para establecer la prioridad de un recurso en [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span><span class="sxs-lookup"><span data-stu-id="17bfc-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="17bfc-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="17bfc-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="17bfc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="17bfc-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="17bfc-107"><dt>**D3D9 \_ 0x28000000 \_ \_ mínima de prioridad de recursos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="17bfc-108">El recurso tiene la prioridad más baja posible.</span><span class="sxs-lookup"><span data-stu-id="17bfc-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="17bfc-109">Esta constante marca el recurso como no utilizado y para la expulsión.</span><span class="sxs-lookup"><span data-stu-id="17bfc-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="17bfc-110">El recurso debe expulsarse en cuanto otro recurso requiera el espacio de memoria que ocupa el recurso.</span><span class="sxs-lookup"><span data-stu-id="17bfc-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="17bfc-111"><dt>**D3D9 \_ Prioridad de recursos \_ \_ bajo**</dt> <dt>0x50000000</dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="17bfc-112">El recurso está programado con prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="17bfc-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="17bfc-113">La colocación del recurso no es crítica y el sistema operativo realiza un trabajo mínimo para encontrar una ubicación para el recurso.</span><span class="sxs-lookup"><span data-stu-id="17bfc-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="17bfc-114">Marcar un recurso como de prioridad baja permite que otros recursos más críticos ocupen la memoria más rápida.</span><span class="sxs-lookup"><span data-stu-id="17bfc-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="17bfc-115"><dt>**D3D9 \_ 0x78000000 \_ \_ normal de prioridad de recursos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="17bfc-116">El recurso se programa con prioridad normal.</span><span class="sxs-lookup"><span data-stu-id="17bfc-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="17bfc-117">La colocación del recurso es importante para el rendimiento, pero no es fundamental.</span><span class="sxs-lookup"><span data-stu-id="17bfc-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="17bfc-118">El sistema operativo debe intentar colocar el recurso que está marcado como normal en la ubicación preferida del recurso en lugar de un recurso de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="17bfc-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="17bfc-119">Normalmente, las texturas se marcan como normales.</span><span class="sxs-lookup"><span data-stu-id="17bfc-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="17bfc-120"><dt>**D3D9 \_ Prioridad de recursos \_ \_ alta**</dt> <dt>0xa0000000</dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="17bfc-121">El recurso está programado con prioridad alta.</span><span class="sxs-lookup"><span data-stu-id="17bfc-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="17bfc-122">La colocación del recurso es fundamental para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="17bfc-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="17bfc-123">El sistema operativo siempre intenta colocar el recurso marcado como alto en la ubicación preferida del recurso en lugar de un recurso de prioridad baja o normal.</span><span class="sxs-lookup"><span data-stu-id="17bfc-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="17bfc-124">Normalmente, los destinos de representación se marcan como alto.</span><span class="sxs-lookup"><span data-stu-id="17bfc-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="17bfc-125"><dt>**D3D9 \_ \_ \_ Número máximo de prioridades de recursos**</dt> <dt>0xc8000000</dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="17bfc-126">El recurso tiene la máxima prioridad posible.</span><span class="sxs-lookup"><span data-stu-id="17bfc-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="17bfc-127">Esta constante marca la prioridad del recurso como anclado flexible.</span><span class="sxs-lookup"><span data-stu-id="17bfc-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="17bfc-128">Un recurso anclado provisional se expulsa de la memoria solo si no hay otra manera de resolver los requisitos de memoria de un búfer DMA.</span><span class="sxs-lookup"><span data-stu-id="17bfc-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="17bfc-129">El sistema operativo intenta dividir un búfer DMA a su tamaño mínimo y expulsar todos los demás recursos que no están anclados y no se anclan de software antes de expulsar un recurso anclado de software.</span><span class="sxs-lookup"><span data-stu-id="17bfc-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="17bfc-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17bfc-130">Remarks</span></span>

<span data-ttu-id="17bfc-131">El programador trata los valores distintos de la **\_ prioridad del recurso D3D9 \_ \_ Minimum** y **D3D9 \_ \_ \_ Maximum Priority** como sugerencias.</span><span class="sxs-lookup"><span data-stu-id="17bfc-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="17bfc-132">Puede usar niveles de prioridad distintos de los definidos anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="17bfc-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="17bfc-133">Por ejemplo, al marcar un recurso con un nivel de prioridad de 0x78000001, se indica que la prioridad del recurso está ligeramente por encima de lo normal.</span><span class="sxs-lookup"><span data-stu-id="17bfc-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="17bfc-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17bfc-134">Requirements</span></span>



| <span data-ttu-id="17bfc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17bfc-135">Requirement</span></span> | <span data-ttu-id="17bfc-136">Value</span><span class="sxs-lookup"><span data-stu-id="17bfc-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17bfc-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17bfc-137">Header</span></span><br/> | <dl> <span data-ttu-id="17bfc-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="17bfc-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17bfc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="17bfc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bfc-140">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="17bfc-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
