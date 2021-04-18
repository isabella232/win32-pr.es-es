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
# <a name="any-hit-shader"></a><span data-ttu-id="436f3-103">Sombreador de cualquier acierto</span><span class="sxs-lookup"><span data-stu-id="436f3-103">Any Hit Shader</span></span>

<span data-ttu-id="436f3-104">Sombreador que se invoca cuando las intersecciones de rayo no son opacas.</span><span class="sxs-lookup"><span data-stu-id="436f3-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="436f3-105">Cualquier sombreador de posicionamiento debe declarar un parámetro de carga seguido de un parámetro de atributos.</span><span class="sxs-lookup"><span data-stu-id="436f3-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="436f3-106">Cada uno de estos parámetros debe ser un tipo de estructura definido por el usuario que coincida con los tipos que se usan para [**TraceRay**](traceray-function.md) y [**ReportHit**](reporthit-function.md) , respectivamente, o la [**estructura de atributos de intersección**](intersection-attributes.md) cuando se usa la intersección de triángulo de función fija.</span><span class="sxs-lookup"><span data-stu-id="436f3-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="436f3-107">Cualquier sombreador de posicionamiento puede realizar los siguientes tipos de operaciones:</span><span class="sxs-lookup"><span data-stu-id="436f3-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="436f3-108">Lea y modifique la carga de Ray: (INOUT payload_t rayPayload)</span><span class="sxs-lookup"><span data-stu-id="436f3-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="436f3-109">Leer los atributos de intersección: (en attr_t atributos)</span><span class="sxs-lookup"><span data-stu-id="436f3-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="436f3-110">Llame a [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), que acepta el acierto actual, finaliza el [sombreador de posicionamiento](any-hit-shader.md), finaliza el [sombreador de intersección](intersection-shader.md) si uno está presente y ejecuta el [sombreador de posicionamiento más cercano](closest-hit-shader.md) en el acierto más cercano si está activo.</span><span class="sxs-lookup"><span data-stu-id="436f3-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="436f3-111">Llame a [**IgnoreHit**](ignorehit-function.md), que finaliza cualquier sombreador de posicionamiento y indica al sistema que continúe buscando aciertos, incluida la devolución del control a un sombreador de intersección, si se está ejecutando actualmente, devolviendo false desde el sitio de llamada de [**ReportHit**](reporthit-function.md)\*.</span><span class="sxs-lookup"><span data-stu-id="436f3-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="436f3-112">Devuelve sin llamar a ninguno de estos intrínsecos, que acepta el acierto actual e indica al sistema que continúe buscando aciertos, incluida la devolución del control al sombreador de intersección, si hay alguno, devolviendo true en el sitio de llamada [**ReportHit**](reporthit-function.md) para indicar que se aceptó el acierto.</span><span class="sxs-lookup"><span data-stu-id="436f3-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="436f3-113">Incluso si una invocación de un sombreador de posicionamiento ha finalizado por [**IgnoreHit**](ignorehit-function.md) o [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), las modificaciones que se realicen en la carga de rayo hasta ahora se deben conservar.</span><span class="sxs-lookup"><span data-stu-id="436f3-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="436f3-114">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="436f3-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="436f3-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="436f3-115">Example</span></span>

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
