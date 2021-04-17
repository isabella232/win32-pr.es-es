---
description: Un valor de tipo float que representa el punto final paramétrico actual del rayo.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705340"
---
# <a name="raytcurrent"></a><span data-ttu-id="7fb42-103">RayTCurrent</span><span class="sxs-lookup"><span data-stu-id="7fb42-103">RayTCurrent</span></span>

<span data-ttu-id="7fb42-104">Un valor de tipo float que representa el punto final paramétrico actual del rayo.</span><span class="sxs-lookup"><span data-stu-id="7fb42-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="7fb42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fb42-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="7fb42-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fb42-106">Remarks</span></span>

<span data-ttu-id="7fb42-107">**RayTCurrent** define el punto final actual del rayo según la siguiente fórmula: Origin + (Direction \* RayTCurrent).</span><span class="sxs-lookup"><span data-stu-id="7fb42-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="7fb42-108">El *origen* y la *Dirección* pueden estar en el espacio de objeto o en el mundo, lo que da como resultado un punto de final de espacio de objeto o un mundo.</span><span class="sxs-lookup"><span data-stu-id="7fb42-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="7fb42-109">**RayTCurrent** se inicializa en la llamada a [**TraceRay**](traceray-function.md) de llamada con el valor [**RayDesc:: Tmax**](raydesc.md) y, a continuación, se actualiza durante la consulta de seguimiento, ya que las intersecciones se informan (en cualquier acierto) y se aceptan.</span><span class="sxs-lookup"><span data-stu-id="7fb42-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="7fb42-110">En el [sombreador de intersección](intersection-shader.md), representa la distancia a la intersección más cercana encontrada hasta el momento.</span><span class="sxs-lookup"><span data-stu-id="7fb42-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="7fb42-111">Se actualizará después de () al valor THit proporcionado si se aceptó el acierto.</span><span class="sxs-lookup"><span data-stu-id="7fb42-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="7fb42-112">En [cualquier sombreador de posicionamiento](any-hit-shader.md), representa la distancia a la intersección actual que se está informando.</span><span class="sxs-lookup"><span data-stu-id="7fb42-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="7fb42-113">En el [sombreador de posicionamiento más cercano](closest-hit-shader.md), representa la distancia a la intersección más cercana aceptada.</span><span class="sxs-lookup"><span data-stu-id="7fb42-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="7fb42-114">En el [sombreador de errores](miss-shader.md), es igual a *Tmax* pasado a la llamada a **TraceRay** .</span><span class="sxs-lookup"><span data-stu-id="7fb42-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="7fb42-115">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="7fb42-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="7fb42-116">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="7fb42-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="7fb42-117">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="7fb42-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="7fb42-118">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="7fb42-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="7fb42-119">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="7fb42-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="7fb42-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fb42-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fb42-121">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="7fb42-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




