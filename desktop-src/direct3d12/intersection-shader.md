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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465557"
---
# <a name="intersection-shader"></a>Sombreador de intersección

Sombreador que se usa para implementar primitivas de intersección personalizadas para los rayos que intersecan con un volumen de límite asociado (rectángulo de selección). 

El sombreador de intersección no tiene acceso a la carga del rayo, pero define los atributos de intersección para cada impacto a través de una llamada a [**ReportHit**](reporthit-function.md).  El control de **ReportHit** puede detener el sombreador de intersección al principio, si se establece la marca de rayo **RAY FLAG ACCEPT FIRST \_ \_ \_ \_ HIT_\AND \_ \END \_ SEARCH,** o si se llama a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) desde cualquier sombreador de llamadas.  De lo contrario, devuelve true si se aceptó el hit o false si se rechazó.  Esto significa que cualquier sombreador de acceso, si está presente, debe ejecutarse antes de que el control vuelva condicionalmente al sombreador de intersección.

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

 

 




