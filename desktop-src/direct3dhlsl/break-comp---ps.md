---
title: break_comp-PS
description: Salga del bucle actual en el ENDLOOP-PS o endrep-PS más cercano, en función de una comparación por componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148995"
---
# <a name="break_comp---ps"></a><span data-ttu-id="28970-103">Break \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="28970-103">break\_comp - ps</span></span>

<span data-ttu-id="28970-104">Salga del bucle actual en el [ENDLOOP-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)más cercano, en función de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="28970-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="28970-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28970-105">Syntax</span></span>



| <span data-ttu-id="28970-106">Break \_ COMP src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="28970-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="28970-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="28970-107">Where:</span></span>

-   <span data-ttu-id="28970-108">\_Comp es una comparación escalar (o única) entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="28970-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="28970-109">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="28970-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="28970-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28970-110">Syntax</span></span> | <span data-ttu-id="28970-111">De comparación</span><span class="sxs-lookup"><span data-stu-id="28970-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="28970-112">\_bruto</span><span class="sxs-lookup"><span data-stu-id="28970-112">\_gt</span></span>   | <span data-ttu-id="28970-113">Mayor que</span><span class="sxs-lookup"><span data-stu-id="28970-113">Greater than</span></span>          |
    | <span data-ttu-id="28970-114">\_plazo</span><span class="sxs-lookup"><span data-stu-id="28970-114">\_lt</span></span>   | <span data-ttu-id="28970-115">Menor que</span><span class="sxs-lookup"><span data-stu-id="28970-115">Less than</span></span>             |
    | <span data-ttu-id="28970-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="28970-116">\_ge</span></span>   | <span data-ttu-id="28970-117">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="28970-117">Greater than or equal</span></span> |
    | <span data-ttu-id="28970-118">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="28970-118">\_le</span></span>   | <span data-ttu-id="28970-119">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="28970-119">Less than or equal</span></span>    |
    | <span data-ttu-id="28970-120">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="28970-120">\_eq</span></span>   | <span data-ttu-id="28970-121">Igual a</span><span class="sxs-lookup"><span data-stu-id="28970-121">Equal to</span></span>              |
    | <span data-ttu-id="28970-122">\_&</span><span class="sxs-lookup"><span data-stu-id="28970-122">\_ne</span></span>   | <span data-ttu-id="28970-123">No es igual a</span><span class="sxs-lookup"><span data-stu-id="28970-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="28970-124">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="28970-124">src0 is a source register.</span></span> <span data-ttu-id="28970-125">La replicación de swizzle es necesaria si se selecciona un único componente.</span><span class="sxs-lookup"><span data-stu-id="28970-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="28970-126">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="28970-126">src1 is a source register.</span></span> <span data-ttu-id="28970-127">La replicación de swizzle es necesaria si se selecciona un único componente.</span><span class="sxs-lookup"><span data-stu-id="28970-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="28970-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28970-128">Remarks</span></span>

<span data-ttu-id="28970-129">Esta instrucción es compatible con las siguientes versiones.</span><span class="sxs-lookup"><span data-stu-id="28970-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="28970-130">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="28970-130">Pixel shader versions</span></span> | <span data-ttu-id="28970-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="28970-131">1\_1</span></span> | <span data-ttu-id="28970-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="28970-132">1\_2</span></span> | <span data-ttu-id="28970-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="28970-133">1\_3</span></span> | <span data-ttu-id="28970-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="28970-134">1\_4</span></span> | <span data-ttu-id="28970-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28970-135">2\_0</span></span> | <span data-ttu-id="28970-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="28970-136">2\_x</span></span> | <span data-ttu-id="28970-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28970-137">2\_sw</span></span> | <span data-ttu-id="28970-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="28970-138">3\_0</span></span> | <span data-ttu-id="28970-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="28970-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="28970-140">romper \_ COMP</span><span class="sxs-lookup"><span data-stu-id="28970-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="28970-141">x</span><span class="sxs-lookup"><span data-stu-id="28970-141">x</span></span>    | <span data-ttu-id="28970-142">x</span><span class="sxs-lookup"><span data-stu-id="28970-142">x</span></span>     | <span data-ttu-id="28970-143">x</span><span class="sxs-lookup"><span data-stu-id="28970-143">x</span></span>    | <span data-ttu-id="28970-144">x</span><span class="sxs-lookup"><span data-stu-id="28970-144">x</span></span>     |



 

<span data-ttu-id="28970-145">Cuando la comparación es true, se interrumpe el bucle actual, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="28970-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="28970-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28970-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28970-147">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="28970-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




