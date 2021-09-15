---
description: Sombreador que se invoca cuando está habilitado y se ha determinado el impacto más cercano o se ha finalizado la búsqueda de intersección de rayos.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570913"
---
# <a name="closest-hit-shader"></a>Sombreador del acierto más cercano

Sombreador que se invoca cuando está habilitado y se ha determinado el impacto más cercano o se ha finalizado la búsqueda de intersección de rayos. Este sombreador es donde normalmente se producirá el sombreado de superficie y la generación de rayos adicionales.  Los sombreadores de impacto más cercanos deben declarar un parámetro de carga, seguido de un parámetro attributes.  Cada debe ser un tipo de estructura definido por el usuario que coincida [](intersection-attributes.md) con los tipos usados para [**TraceRay**](traceray-function.md) y [**ReportHit**](reporthit-function.md) respectivamente, o la estructura de atributos de intersección cuando se usa la intersección de triángulos de función fija.

## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


```
[shader("closesthit")]
```



## <a name="example"></a>Ejemplo

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

 

 




