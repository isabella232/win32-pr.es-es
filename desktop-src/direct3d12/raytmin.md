---
description: Un valor de tipo float que representa el punto inicial paramétrico actual del rayo.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705339"
---
# <a name="raytmin"></a><span data-ttu-id="a49ff-103">RayTMin</span><span class="sxs-lookup"><span data-stu-id="a49ff-103">RayTMin</span></span>

<span data-ttu-id="a49ff-104">Un valor de tipo float que representa el punto inicial paramétrico actual del rayo.</span><span class="sxs-lookup"><span data-stu-id="a49ff-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="a49ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a49ff-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="a49ff-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a49ff-106">Remarks</span></span>

<span data-ttu-id="a49ff-107">**RayTMin** define el punto inicial del rayo según la fórmula siguiente: Origin + (Direction \* RayTMin).</span><span class="sxs-lookup"><span data-stu-id="a49ff-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="a49ff-108">El *origen* y la *Dirección* pueden estar en el espacio de objeto o en el mundo, lo que da como resultado un punto de partida de un mundo o un espacio de objeto.</span><span class="sxs-lookup"><span data-stu-id="a49ff-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="a49ff-109">**RayTMin** se especifica en la llamada a [**TraceRay**](traceray-function.md)y es constante mientras dure la llamada.</span><span class="sxs-lookup"><span data-stu-id="a49ff-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="a49ff-110">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="a49ff-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="a49ff-111">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="a49ff-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="a49ff-112">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="a49ff-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="a49ff-113">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="a49ff-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="a49ff-114">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="a49ff-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="a49ff-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a49ff-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49ff-116">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="a49ff-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




