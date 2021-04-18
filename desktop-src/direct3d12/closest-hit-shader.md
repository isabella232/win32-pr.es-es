---
description: Sombreador que se invoca cuando está habilitado y se ha determinado el acierto más cercano o ha finalizado la búsqueda de interseccións de Ray.
ms.assetid: ''
title: Sombreador del acierto más cercano
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714881"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="4e710-103">Sombreador del acierto más cercano</span><span class="sxs-lookup"><span data-stu-id="4e710-103">Closest Hit Shader</span></span>

<span data-ttu-id="4e710-104">Sombreador que se invoca cuando está habilitado y se ha determinado el acierto más cercano o ha finalizado la búsqueda de interseccións de Ray.</span><span class="sxs-lookup"><span data-stu-id="4e710-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="4e710-105">Este sombreador es donde normalmente se producirá el sombreado de superficie y la generación de rayo adicional.</span><span class="sxs-lookup"><span data-stu-id="4e710-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="4e710-106">Los sombreadores de posicionamiento más cercanos deben declarar un parámetro de carga, seguido de un parámetro de atributos.</span><span class="sxs-lookup"><span data-stu-id="4e710-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="4e710-107">Cada debe ser un tipo de estructura definido por el usuario que coincida con los tipos que se usan para [**TraceRay**](traceray-function.md) y [**ReportHit**](reporthit-function.md) , respectivamente, o la [**estructura de atributos de intersección**](intersection-attributes.md) cuando se usa la intersección de triángulo de función fija.</span><span class="sxs-lookup"><span data-stu-id="4e710-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="4e710-108">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4e710-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="4e710-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e710-109">Example</span></span>

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




