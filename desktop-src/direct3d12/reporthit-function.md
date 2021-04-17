---
description: Lo llama un sombreador de intersección para notificar una intersección de rayo.
ms.assetid: ''
title: Función ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705365"
---
# <a name="reporthit-function"></a><span data-ttu-id="cbd46-103">Función ReportHit</span><span class="sxs-lookup"><span data-stu-id="cbd46-103">ReportHit function</span></span>

<span data-ttu-id="cbd46-104">Lo llama un [sombreador de intersección](intersection-shader.md) para notificar una intersección de rayo.</span><span class="sxs-lookup"><span data-stu-id="cbd46-104">Called by an [intersection shader](intersection-shader.md) to report a ray intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd46-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbd46-105">Syntax</span></span>
<span data-ttu-id="cbd46-106">Esta definición de función intrínseca es equivalente a la siguiente plantilla de función:</span><span class="sxs-lookup"><span data-stu-id="cbd46-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a><span data-ttu-id="cbd46-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbd46-107">Parameters</span></span>

`THit`

<span data-ttu-id="cbd46-108">Un valor de tipo float que especifica la distancia paramétrica de la intersección.</span><span class="sxs-lookup"><span data-stu-id="cbd46-108">A float value specifying the parametric distance of the intersection..</span></span>

`HitKind`

<span data-ttu-id="cbd46-109">Entero sin signo que identifica el tipo de acierto que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="cbd46-109">An unsigned integer that identifies the type of hit that occurred.</span></span>  <span data-ttu-id="cbd46-110">Este es un valor especificado por el usuario en el intervalo de 0-127.</span><span class="sxs-lookup"><span data-stu-id="cbd46-110">This is a user-specified value in the range of 0-127.</span></span>  <span data-ttu-id="cbd46-111">El valor se puede leer en [cualquier](any-hit-shader.md) sombreado de posicionamiento o de [posicionamiento más cercano](closest-hit-shader.md) con el intrínseco **HitKind** .</span><span class="sxs-lookup"><span data-stu-id="cbd46-111">The value can be read by [any hit](any-hit-shader.md) or [closest hit](closest-hit-shader.md) shaders with the **HitKind** intrinsic.</span></span>

`Attributes`

<span data-ttu-id="cbd46-112">Estructura del atributo de [**intersección**](intersection-attributes.md) definido por el usuario que especifica los atributos de intersección.</span><span class="sxs-lookup"><span data-stu-id="cbd46-112">The user-defined [**Intersection Attribute Structure**](intersection-attributes.md) structure specifying the intersection attributes.</span></span>  

## <a name="return-value"></a><span data-ttu-id="cbd46-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbd46-113">Return Value</span></span>

<span data-ttu-id="cbd46-114">**booleano** True si se aceptó el acierto.</span><span class="sxs-lookup"><span data-stu-id="cbd46-114">**bool** True if the hit was accepted.</span></span>  <span data-ttu-id="cbd46-115">Se rechaza una visita si *THit* está fuera del intervalo de rayo actual, o el sombreador de aciertos llama a [**IgnoreHit**](ignorehit-function.md).</span><span class="sxs-lookup"><span data-stu-id="cbd46-115">A hit is rejected if *THit* is outside the current ray interval, or the any hit shader calls [**IgnoreHit**](ignorehit-function.md).</span></span>  <span data-ttu-id="cbd46-116">El intervalo de rayo actual está definido por **RayTMin** y **RayTCurrent**.</span><span class="sxs-lookup"><span data-stu-id="cbd46-116">The current ray interval is defined by **RayTMin** and **RayTCurrent**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd46-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbd46-117">Remarks</span></span>

<span data-ttu-id="cbd46-118">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="cbd46-118">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="cbd46-119">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="cbd46-119">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="cbd46-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbd46-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd46-121">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="cbd46-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




