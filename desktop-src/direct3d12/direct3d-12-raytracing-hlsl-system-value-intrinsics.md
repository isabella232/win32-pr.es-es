---
title: Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen funciones intrínsecas de valor del sistema de lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396440"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="74fd6-103">Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="74fd6-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="74fd6-104">Los valores del sistema se recuperan mediante funciones intrínsecas especiales, en lugar de incluir parámetros con semántica especial en la firma de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="74fd6-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="74fd6-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="74fd6-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="74fd6-106">Valores del sistema de distribución de Ray</span><span class="sxs-lookup"><span data-stu-id="74fd6-106">Ray dispatch system values</span></span>

| <span data-ttu-id="74fd6-107">Tema</span><span class="sxs-lookup"><span data-stu-id="74fd6-107">Topic</span></span> | <span data-ttu-id="74fd6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="74fd6-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="74fd6-109">**DispatchRaysIndex**</span><span class="sxs-lookup"><span data-stu-id="74fd6-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="74fd6-110">Obtiene la ubicación x e y actual dentro del ancho y alto obtenidos con el valor intrínseco del sistema **DispatchRaysDimensions.**</span><span class="sxs-lookup"><span data-stu-id="74fd6-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="74fd6-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="74fd6-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="74fd6-112">Los valores de ancho, alto y profundidad de la estructura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** especificada en la **llamada dispatchRays de** origen.</span><span class="sxs-lookup"><span data-stu-id="74fd6-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="74fd6-113">Valores del sistema ray</span><span class="sxs-lookup"><span data-stu-id="74fd6-113">Ray system values</span></span>

| <span data-ttu-id="74fd6-114">Tema</span><span class="sxs-lookup"><span data-stu-id="74fd6-114">Topic</span></span> | <span data-ttu-id="74fd6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="74fd6-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="74fd6-116">**WorldRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="74fd6-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="74fd6-117">Origen del espacio mundial del rayo actual.</span><span class="sxs-lookup"><span data-stu-id="74fd6-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="74fd6-118">**WorldRayDirection**</span><span class="sxs-lookup"><span data-stu-id="74fd6-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="74fd6-119">Dirección del espacio del mundo para el rayo actual.</span><span class="sxs-lookup"><span data-stu-id="74fd6-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="74fd6-120">**RayTMin**</span><span class="sxs-lookup"><span data-stu-id="74fd6-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="74fd6-121">Un valor float que representa el punto inicial paramétrico actual para el rayo.</span><span class="sxs-lookup"><span data-stu-id="74fd6-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="74fd6-122">**RayTCurrent**</span><span class="sxs-lookup"><span data-stu-id="74fd6-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="74fd6-123">Float que representa el punto final paramétrico actual del rayo.</span><span class="sxs-lookup"><span data-stu-id="74fd6-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="74fd6-124">**RayFlags**</span><span class="sxs-lookup"><span data-stu-id="74fd6-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="74fd6-125">Entero sin signo que contiene las marcas **ray_flag** actuales.</span><span class="sxs-lookup"><span data-stu-id="74fd6-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="74fd6-126">Valores primitivos o del sistema de espacio de objetos</span><span class="sxs-lookup"><span data-stu-id="74fd6-126">Primitive/object space system values</span></span>

| <span data-ttu-id="74fd6-127">Tema</span><span class="sxs-lookup"><span data-stu-id="74fd6-127">Topic</span></span> | <span data-ttu-id="74fd6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="74fd6-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="74fd6-129">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="74fd6-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="74fd6-130">Índice generado automáticamente de la instancia actual en la estructura de aceleración de rayos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="74fd6-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="74fd6-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74fd6-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="74fd6-132">Identificador proporcionado por el usuario para la instancia de en la instancia de la estructura de aceleración de nivel inferior dentro de la estructura de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="74fd6-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="74fd6-133">**PrimitiveIndex**</span><span class="sxs-lookup"><span data-stu-id="74fd6-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="74fd6-134">Índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="74fd6-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="74fd6-135">**ObjectRayOrigin**</span><span class="sxs-lookup"><span data-stu-id="74fd6-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="74fd6-136">Origen del espacio de objetos para el rayo actual.</span><span class="sxs-lookup"><span data-stu-id="74fd6-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="74fd6-137">**ObjectRayDirection**</span><span class="sxs-lookup"><span data-stu-id="74fd6-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="74fd6-138">Dirección del espacio del objeto para el rayo actual.</span><span class="sxs-lookup"><span data-stu-id="74fd6-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="74fd6-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="74fd6-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="74fd6-140">Matriz para transformar del espacio de objetos al espacio del mundo.</span><span class="sxs-lookup"><span data-stu-id="74fd6-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="74fd6-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="74fd6-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="74fd6-142">Matriz para transformar del espacio de objetos al espacio del mundo.</span><span class="sxs-lookup"><span data-stu-id="74fd6-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="74fd6-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="74fd6-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="74fd6-144">Matriz para la transformación del espacio del mundo al espacio de objetos</span><span class="sxs-lookup"><span data-stu-id="74fd6-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="74fd6-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="74fd6-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="74fd6-146">Matriz para la transformación del espacio del mundo al espacio de objetos</span><span class="sxs-lookup"><span data-stu-id="74fd6-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="74fd6-147">Valores del sistema específicos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="74fd6-147">Hit-specific system values</span></span>

| <span data-ttu-id="74fd6-148">Tema</span><span class="sxs-lookup"><span data-stu-id="74fd6-148">Topic</span></span> | <span data-ttu-id="74fd6-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="74fd6-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="74fd6-150">**HitKind**</span><span class="sxs-lookup"><span data-stu-id="74fd6-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="74fd6-151">Devuelve el valor pasado como parámetro **HitKind** a [**ReportHit.**](reporthit-function.md)</span><span class="sxs-lookup"><span data-stu-id="74fd6-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="74fd6-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74fd6-152">Related topics</span></span>

* [<span data-ttu-id="74fd6-153">Referencia principal</span><span class="sxs-lookup"><span data-stu-id="74fd6-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="74fd6-154">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="74fd6-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
