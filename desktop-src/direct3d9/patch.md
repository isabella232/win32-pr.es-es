---
description: Define una revisión de \# control de Bézier B&233;. La matriz define los puntos de control para la revisión.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906327"
---
# <a name="patch"></a><span data-ttu-id="1c639-104">Revisión</span><span class="sxs-lookup"><span data-stu-id="1c639-104">Patch</span></span>

<span data-ttu-id="1c639-105">Define una revisión de control Bezier.</span><span class="sxs-lookup"><span data-stu-id="1c639-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="1c639-106">La matriz define los puntos de control para la revisión.</span><span class="sxs-lookup"><span data-stu-id="1c639-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="1c639-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="1c639-107">Where:</span></span>

-   <span data-ttu-id="1c639-108">nControlIndices: número de índices de punto de control.</span><span class="sxs-lookup"><span data-stu-id="1c639-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="1c639-109">array DWORD controlIndices \[ nControlIndices \] : matriz de índices de punto de control.</span><span class="sxs-lookup"><span data-stu-id="1c639-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="1c639-110">El tipo de revisión se define por el número de puntos de control, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1c639-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="1c639-111">Número de puntos de control</span><span class="sxs-lookup"><span data-stu-id="1c639-111">Number of control points</span></span> | <span data-ttu-id="1c639-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c639-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="1c639-113">10</span><span class="sxs-lookup"><span data-stu-id="1c639-113">10</span></span>                       | <span data-ttu-id="1c639-114">Revisión triangular Bézier cúbica</span><span class="sxs-lookup"><span data-stu-id="1c639-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="1c639-115">15</span><span class="sxs-lookup"><span data-stu-id="1c639-115">15</span></span>                       | <span data-ttu-id="1c639-116">Revisión triangular de Bézier de cuartil</span><span class="sxs-lookup"><span data-stu-id="1c639-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="1c639-117">16</span><span class="sxs-lookup"><span data-stu-id="1c639-117">16</span></span>                       | <span data-ttu-id="1c639-118">Revisión Bézier cúbica de rectángulo cuádruple</span><span class="sxs-lookup"><span data-stu-id="1c639-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="1c639-119">El orden de los puntos de control se proporciona en un patrón de espiral, tal como se muestra en los diagramas siguientes para las revisiones triangulares y rectangulares.</span><span class="sxs-lookup"><span data-stu-id="1c639-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="1c639-120">Las revisiones triangulares usan el siguiente patrón.</span><span class="sxs-lookup"><span data-stu-id="1c639-120">Triangular patches use the following pattern.</span></span>

![diagrama del patrón para las revisiones triangulares](images/tripatch.png)

<span data-ttu-id="1c639-122">Las revisiones rectangulares usan el siguiente patrón.</span><span class="sxs-lookup"><span data-stu-id="1c639-122">Rectangular patches use the following pattern.</span></span>

![diagrama del patrón para las revisiones rectangulares](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="1c639-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c639-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c639-125">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="1c639-125">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



