---
description: Devuelve el valor que se pasa como parámetro HitKind a ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648167"
---
# <a name="hitkind"></a><span data-ttu-id="e7896-103">HitKind</span><span class="sxs-lookup"><span data-stu-id="e7896-103">HitKind</span></span>

<span data-ttu-id="e7896-104">Devuelve el valor que se pasa como parámetro **HitKind** a [**ReportHit**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="e7896-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7896-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7896-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="e7896-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7896-106">Remarks</span></span>

<span data-ttu-id="e7896-107">Si la intersección se ha comunicado mediante la intersección de triangular de función fija, **HitKind** será uno de los tipos de golpe de la **\_ \_ \_ \_ cara frontal** (254) o el triángulo de la **\_ especie \_ \_ posterior \_** (255).</span><span class="sxs-lookup"><span data-stu-id="e7896-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="e7896-108">Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:</span><span class="sxs-lookup"><span data-stu-id="e7896-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="e7896-109">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="e7896-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="e7896-110">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="e7896-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="e7896-111">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="e7896-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="e7896-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7896-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7896-113">Reference de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="e7896-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




