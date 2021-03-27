---
title: break_comp-vs
description: Divida condicionalmente el bucle actual en el ENDLOOP-vs o endrep-vs más cercano.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904290"
---
# <a name="break_comp---vs"></a><span data-ttu-id="767e5-103">Break \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="767e5-103">break\_comp - vs</span></span>

<span data-ttu-id="767e5-104">Divida condicionalmente el bucle actual en el [ENDLOOP-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)más cercano.</span><span class="sxs-lookup"><span data-stu-id="767e5-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="767e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="767e5-105">Syntax</span></span>



| <span data-ttu-id="767e5-106">Break \_ COMP src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="767e5-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="767e5-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="767e5-107">Where:</span></span>

-   <span data-ttu-id="767e5-108">\_Comp es una comparación entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="767e5-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="767e5-109">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="767e5-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="767e5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="767e5-110">Syntax</span></span> | <span data-ttu-id="767e5-111">De comparación</span><span class="sxs-lookup"><span data-stu-id="767e5-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="767e5-112">\_bruto</span><span class="sxs-lookup"><span data-stu-id="767e5-112">\_gt</span></span>   | <span data-ttu-id="767e5-113">Mayor que</span><span class="sxs-lookup"><span data-stu-id="767e5-113">Greater than</span></span>          |
    | <span data-ttu-id="767e5-114">\_plazo</span><span class="sxs-lookup"><span data-stu-id="767e5-114">\_lt</span></span>   | <span data-ttu-id="767e5-115">Menor que</span><span class="sxs-lookup"><span data-stu-id="767e5-115">Less than</span></span>             |
    | <span data-ttu-id="767e5-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="767e5-116">\_ge</span></span>   | <span data-ttu-id="767e5-117">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="767e5-117">Greater than or equal</span></span> |
    | <span data-ttu-id="767e5-118">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="767e5-118">\_le</span></span>   | <span data-ttu-id="767e5-119">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="767e5-119">Less than or equal</span></span>    |
    | <span data-ttu-id="767e5-120">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="767e5-120">\_eq</span></span>   | <span data-ttu-id="767e5-121">Igual a</span><span class="sxs-lookup"><span data-stu-id="767e5-121">Equal to</span></span>              |
    | <span data-ttu-id="767e5-122">\_&</span><span class="sxs-lookup"><span data-stu-id="767e5-122">\_ne</span></span>   | <span data-ttu-id="767e5-123">No es igual a</span><span class="sxs-lookup"><span data-stu-id="767e5-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="767e5-124">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="767e5-124">src0 is a source register.</span></span> <span data-ttu-id="767e5-125">Replicate swizzle es necesario para seleccionar un componente único.</span><span class="sxs-lookup"><span data-stu-id="767e5-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="767e5-126">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="767e5-126">src1 is a source register.</span></span> <span data-ttu-id="767e5-127">Replicate swizzle es necesario para seleccionar un componente único.</span><span class="sxs-lookup"><span data-stu-id="767e5-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="767e5-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="767e5-128">Remarks</span></span>

<span data-ttu-id="767e5-129">Esta instrucción es compatible con las siguientes versiones.</span><span class="sxs-lookup"><span data-stu-id="767e5-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="767e5-130">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="767e5-130">Vertex shader versions</span></span> | <span data-ttu-id="767e5-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="767e5-131">1\_1</span></span> | <span data-ttu-id="767e5-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="767e5-132">2\_0</span></span> | <span data-ttu-id="767e5-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="767e5-133">2\_x</span></span> | <span data-ttu-id="767e5-134">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="767e5-134">2\_sw</span></span> | <span data-ttu-id="767e5-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="767e5-135">3\_0</span></span> | <span data-ttu-id="767e5-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="767e5-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="767e5-137">romper \_ COMP</span><span class="sxs-lookup"><span data-stu-id="767e5-137">break\_comp</span></span>            |      |      | <span data-ttu-id="767e5-138">x</span><span class="sxs-lookup"><span data-stu-id="767e5-138">x</span></span>    | <span data-ttu-id="767e5-139">x</span><span class="sxs-lookup"><span data-stu-id="767e5-139">x</span></span>     | <span data-ttu-id="767e5-140">x</span><span class="sxs-lookup"><span data-stu-id="767e5-140">x</span></span>    | <span data-ttu-id="767e5-141">x</span><span class="sxs-lookup"><span data-stu-id="767e5-141">x</span></span>     |



 

<span data-ttu-id="767e5-142">Cuando la comparación es true, se interrumpe el bucle actual, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="767e5-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="767e5-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="767e5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="767e5-144">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="767e5-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




