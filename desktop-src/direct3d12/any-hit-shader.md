---
description: Sombreador que se invoca cuando las intersecciones de rayo no son opacas.
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
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714815"
---
# <a name="any-hit-shader"></a>Sombreador de cualquier acierto

Sombreador que se invoca cuando las intersecciones de rayo no son opacas. 

Cualquier sombreador de posicionamiento debe declarar un parámetro de carga seguido de un parámetro de atributos. Cada uno de estos parámetros debe ser un tipo de estructura definido por el usuario que coincida con los tipos que se usan para [**TraceRay**](traceray-function.md) y [**ReportHit**](reporthit-function.md) , respectivamente, o la [**estructura de atributos de intersección**](intersection-attributes.md) cuando se usa la intersección de triángulo de función fija.

Cualquier sombreador de posicionamiento puede realizar los siguientes tipos de operaciones:

*   Lea y modifique la carga de Ray: (INOUT payload_t rayPayload)
*   Leer los atributos de intersección: (en attr_t atributos)
*   Llame a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), que acepta el acierto actual, finaliza el [sombreador de posicionamiento](any-hit-shader.md), finaliza el [sombreador de intersección](intersection-shader.md) si uno está presente y ejecuta el [sombreador de posicionamiento más cercano](closest-hit-shader.md) en el acierto más cercano si está activo.
*   Llame a [**IgnoreHit**](ignorehit-function.md), que finaliza cualquier sombreador de posicionamiento y indica al sistema que continúe buscando aciertos, incluida la devolución del control a un sombreador de intersección, si se está ejecutando actualmente, devolviendo false desde el sitio de llamada de [**ReportHit**](reporthit-function.md)*. 
*   Devuelve sin llamar a ninguno de estos intrínsecos, que acepta el acierto actual e indica al sistema que continúe buscando aciertos, incluida la devolución del control al sombreador de intersección, si hay alguno, devolviendo true en el sitio de llamada [**ReportHit**](reporthit-function.md) para indicar que se aceptó el acierto.

Incluso si una invocación de un sombreador de posicionamiento ha finalizado por [**IgnoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), las modificaciones que se realicen en la carga de rayo hasta ahora se deben conservar.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador

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
