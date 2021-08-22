---
description: Sombreador que se invoca cuando las intersecciones de rayos no son opacas.
ms.assetid: ''
title: Sombreador de cualquier acierto
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 127c12c6d87ca76ddac5b5c5e013414c96651e56ee762156e7435811ff275a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124390"
---
# <a name="any-hit-shader"></a>Sombreador de cualquier acierto

Sombreador que se invoca cuando las intersecciones de rayos no son opacas. 

Los sombreadores de impacto deben declarar un parámetro de carga seguido de un parámetro attributes. Cada uno de estos parámetros debe ser un tipo de estructura definido por el [](intersection-attributes.md) usuario que coincida con los tipos usados para [**TraceRay**](traceray-function.md) y [**ReportHit**](reporthit-function.md) respectivamente, o la estructura de atributos de intersección cuando se usa la intersección de triángulo de función fija.

Los sombreadores de impacto pueden realizar los siguientes tipos de operaciones:

*   Leer y modificar la carga del rayo: (inout payload_t rayPayload)
*   Lea los atributos de intersección: (en attr_t atributos)
*   Llame a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), que acepta la llamada actual, [](intersection-shader.md) finaliza cualquier sombreador de [llamadas,](any-hit-shader.md)finaliza el sombreador de intersección si hay alguno y ejecuta el sombreador de llamadas más cercano en el punto más cercano hasta ahora si está activo. [](closest-hit-shader.md)
*   Llame [**a IgnoreHit**](ignorehit-function.md), que finaliza cualquier sombreador de llamadas e indica al sistema que siga buscando aciertos, incluida la devolución del control a un sombreador de intersección, si se está ejecutando actualmente, devolviendo false desde el sitio de llamada [**de ReportHit**](reporthit-function.md)*. 
*   Vuelva sin llamar a ninguno de estos intrínsecos, que acepta el acierto actual e indica al sistema que siga buscando aciertos, incluida la devolución del control al sombreador de intersección si hay alguno, devolviendo true en el sitio de llamada de [**ReportHit**](reporthit-function.md) para indicar que se aceptó el acierto.

Incluso si [**ignoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)finalizan una invocación del sombreador de llamadas, las modificaciones realizadas hasta ahora en la carga del rayo deben conservarse.

## <a name="shader-type-attribute"></a>Atributo Tipo de sombreador

```
[shader("anyhit")]
```

## <a name="example"></a>Ejemplo

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
