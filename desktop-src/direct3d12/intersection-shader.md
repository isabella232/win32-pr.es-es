---
description: Sombreador que se usa para implementar primitivas de intersección personalizadas para los rayos que intersecan con un volumen de límite asociado (rectángulo de selección).
ms.assetid: ''
title: Sombreador de intersección
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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850885"
---
# <a name="intersection-shader"></a>Sombreador de intersección

Sombreador que se usa para implementar primitivas de intersección personalizadas para los rayos que intersecan con un volumen de límite asociado (rectángulo de selección). 

El sombreador de intersección no tiene acceso a la carga del rayo, pero define los atributos de intersección para cada impacto a través de una llamada a [**ReportHit**](reporthit-function.md).  El control de **ReportHit** puede detener el sombreador de intersección al principio, si se establece la marca de rayo **RAY FLAG ACCEPT FIRST \_ \_ \_ \_ HIT_\AND \_ \END \_ SEARCH,** o bien se llama a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) desde cualquier sombreador de llamadas.  De lo contrario, devuelve true si se aceptó el hit o false si se rechazó.  Esto significa que cualquier sombreador de acceso, si está presente, debe ejecutarse antes de que el control vuelva condicionalmente al sombreador de intersección.

## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador


```
[shader("intersection")]
```



## <a name="example"></a>Ejemplo

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




