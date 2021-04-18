---
title: Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing
description: Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "105714493"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="4441c-103">Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="4441c-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="4441c-104">Los valores del sistema se recuperan mediante funciones intrínsecas especiales, en lugar de incluir parámetros con semántica especial en la firma de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4441c-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="4441c-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4441c-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="4441c-106">Valores del sistema de distribución de Ray</span><span class="sxs-lookup"><span data-stu-id="4441c-106">Ray dispatch system values</span></span>

| <span data-ttu-id="4441c-107">Tema</span><span class="sxs-lookup"><span data-stu-id="4441c-107">Topic</span></span> | <span data-ttu-id="4441c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4441c-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="4441c-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="4441c-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="4441c-110">Obtiene la ubicación x e y actual en el ancho y el alto obtenidos con el valor intrínseco del sistema **DispatchRaysDimensions** .</span><span class="sxs-lookup"><span data-stu-id="4441c-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="4441c-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="4441c-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="4441c-112">Los valores de ancho, alto y profundidad de la estructura de D3D12 de los **\_ \_ rayos \_ de distribución** de la serie especificada en la llamada de **DispatchRays** de origen.</span><span class="sxs-lookup"><span data-stu-id="4441c-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="4441c-113">Valores del sistema Ray</span><span class="sxs-lookup"><span data-stu-id="4441c-113">Ray system values</span></span>

| <span data-ttu-id="4441c-114">Tema</span><span class="sxs-lookup"><span data-stu-id="4441c-114">Topic</span></span> | <span data-ttu-id="4441c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4441c-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="4441c-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="4441c-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="4441c-117">El origen de espacio mundial del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="4441c-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="4441c-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="4441c-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="4441c-119">Dirección de espacio mundial del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="4441c-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="4441c-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="4441c-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="4441c-121">Un valor de tipo float que representa el punto inicial paramétrico actual del rayo.</span><span class="sxs-lookup"><span data-stu-id="4441c-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="4441c-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="4441c-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="4441c-123">Un valor de tipo float que representa el punto final paramétrico actual del rayo.</span><span class="sxs-lookup"><span data-stu-id="4441c-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="4441c-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="4441c-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="4441c-125">Entero sin signo que contiene las marcas de **ray_flag** actuales.</span><span class="sxs-lookup"><span data-stu-id="4441c-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="4441c-126">Valores del sistema de espacio de objetos primitivos</span><span class="sxs-lookup"><span data-stu-id="4441c-126">Primitive/object space system values</span></span>

| <span data-ttu-id="4441c-127">Tema</span><span class="sxs-lookup"><span data-stu-id="4441c-127">Topic</span></span> | <span data-ttu-id="4441c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4441c-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="4441c-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="4441c-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="4441c-130">Índice generado automáticamente de la instancia actual en la estructura de nivel superior raytracing de aceleración.</span><span class="sxs-lookup"><span data-stu-id="4441c-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="4441c-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="4441c-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="4441c-132">El identificador proporcionado por el usuario para la instancia en la instancia de la estructura de aceleración de nivel inferior dentro de la estructura de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4441c-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="4441c-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="4441c-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="4441c-134">Índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4441c-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="4441c-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="4441c-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="4441c-136">El origen del espacio de objeto del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="4441c-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="4441c-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="4441c-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="4441c-138">Dirección del espacio de objeto del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="4441c-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="4441c-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="4441c-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="4441c-140">Matriz que se va a transformar del espacio de objeto a espacio universal.</span><span class="sxs-lookup"><span data-stu-id="4441c-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="4441c-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="4441c-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="4441c-142">Matriz que se va a transformar del espacio de objeto a espacio universal.</span><span class="sxs-lookup"><span data-stu-id="4441c-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="4441c-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="4441c-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="4441c-144">Matriz para transformar de espacio universal a objeto-espacio</span><span class="sxs-lookup"><span data-stu-id="4441c-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="4441c-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="4441c-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="4441c-146">Matriz para transformar de espacio universal a objeto-espacio</span><span class="sxs-lookup"><span data-stu-id="4441c-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="4441c-147">Valores del sistema específicos de la visita</span><span class="sxs-lookup"><span data-stu-id="4441c-147">Hit-specific system values</span></span>

| <span data-ttu-id="4441c-148">Tema</span><span class="sxs-lookup"><span data-stu-id="4441c-148">Topic</span></span> | <span data-ttu-id="4441c-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="4441c-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="4441c-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="4441c-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="4441c-151">Devuelve el valor que se pasa como parámetro **HitKind** a [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="4441c-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="4441c-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4441c-152">Related topics</span></span>

* [<span data-ttu-id="4441c-153">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="4441c-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="4441c-154">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4441c-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
