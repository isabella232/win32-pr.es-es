---
description: Sombreador que se utiliza para implementar primitivas de intersección personalizadas para los rayos que intersectan con un volumen de límite asociado (rectángulo de selección).
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714891"
---
# <a name="intersection-shader"></a>Sombreador de intersección

Sombreador que se utiliza para implementar primitivas de intersección personalizadas para los rayos que intersectan con un volumen de límite asociado (rectángulo de selección). 

El sombreador de intersección no tiene acceso a la carga de Ray, pero define los atributos de intersección para cada golpe a través de una llamada a [**ReportHit**](reporthit-function.md).  El control de **ReportHit** puede detener el sombreador de intersección al principio, si la marca de rayo de la marca de rayo **\_ \_ acepta \_ primero \_ HIT_ \AND \_ \END \_** se establece o se llama a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) desde cualquier sombreador de posicionamiento.  De lo contrario, devuelve true si se aceptó la aceptación o false si se rechazó el acierto.  Esto significa que cualquier sombreador de posicionamiento, si está presente, debe ejecutarse antes de que el control devuelva condicionalmente al sombreador de intersección.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


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

 

 




