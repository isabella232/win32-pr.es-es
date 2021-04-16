---
description: Obtiene la ubicación actual en el ancho, el alto y la profundidad obtenida con el valor intrínseco del sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "105695800"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="10f2e-103">DispatchRaysIndex </span><span class="sxs-lookup"><span data-stu-id="10f2e-103">DispatchRaysIndex</span></span>

<span data-ttu-id="10f2e-104">Obtiene la ubicación actual en el ancho, el alto y la profundidad obtenida con el valor intrínseco del sistema [**DispatchRaysDimensions**](dispatchraysdimensions.md) .</span><span class="sxs-lookup"><span data-stu-id="10f2e-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10f2e-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="10f2e-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10f2e-106">Remarks</span></span>

<span data-ttu-id="10f2e-107">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing.</span><span class="sxs-lookup"><span data-stu-id="10f2e-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="10f2e-108">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="10f2e-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="10f2e-109">**Sombreador al que se puede llamar**</span><span class="sxs-lookup"><span data-stu-id="10f2e-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="10f2e-110">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="10f2e-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="10f2e-111">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="10f2e-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="10f2e-112">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="10f2e-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="10f2e-113">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="10f2e-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="10f2e-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f2e-114">See also</span></span>

* [<span data-ttu-id="10f2e-115">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="10f2e-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
