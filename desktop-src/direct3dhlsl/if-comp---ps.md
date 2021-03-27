---
title: if_comp-PS
description: Iniciar un IF bool-PS... Else-PS... bloque endif-PS, con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784888"
---
# <a name="if_comp---ps"></a><span data-ttu-id="74066-104">Si \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="74066-104">if\_comp - ps</span></span>

<span data-ttu-id="74066-105">Iniciar un [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... bloque [endif-PS](endif---ps.md) , con una condición basada en valores que podrían calcularse en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="74066-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="74066-106">Esta instrucción se usa para omitir un bloque de código, en función de una condición.</span><span class="sxs-lookup"><span data-stu-id="74066-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="74066-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74066-107">Syntax</span></span>



| <span data-ttu-id="74066-108">If \_ COMP src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="74066-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="74066-109">Donde:</span><span class="sxs-lookup"><span data-stu-id="74066-109">Where:</span></span>

-   <span data-ttu-id="74066-110">\_Comp es una comparación entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="74066-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="74066-111">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="74066-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="74066-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74066-112">Syntax</span></span> | <span data-ttu-id="74066-113">De comparación</span><span class="sxs-lookup"><span data-stu-id="74066-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="74066-114">\_bruto</span><span class="sxs-lookup"><span data-stu-id="74066-114">\_gt</span></span>   | <span data-ttu-id="74066-115">Mayor que</span><span class="sxs-lookup"><span data-stu-id="74066-115">Greater than</span></span>          |
    | <span data-ttu-id="74066-116">\_plazo</span><span class="sxs-lookup"><span data-stu-id="74066-116">\_lt</span></span>   | <span data-ttu-id="74066-117">Menor que</span><span class="sxs-lookup"><span data-stu-id="74066-117">Less than</span></span>             |
    | <span data-ttu-id="74066-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="74066-118">\_ge</span></span>   | <span data-ttu-id="74066-119">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="74066-119">Greater than or equal</span></span> |
    | <span data-ttu-id="74066-120">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="74066-120">\_le</span></span>   | <span data-ttu-id="74066-121">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="74066-121">Less than or equal</span></span>    |
    | <span data-ttu-id="74066-122">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="74066-122">\_eq</span></span>   | <span data-ttu-id="74066-123">Igual a</span><span class="sxs-lookup"><span data-stu-id="74066-123">Equal to</span></span>              |
    | <span data-ttu-id="74066-124">\_&</span><span class="sxs-lookup"><span data-stu-id="74066-124">\_ne</span></span>   | <span data-ttu-id="74066-125">No es igual a</span><span class="sxs-lookup"><span data-stu-id="74066-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="74066-126">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="74066-126">src0 is a source register.</span></span> <span data-ttu-id="74066-127">La replicación de swizzle es necesaria para seleccionar un componente.</span><span class="sxs-lookup"><span data-stu-id="74066-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="74066-128">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="74066-128">src1 is a source register.</span></span> <span data-ttu-id="74066-129">La replicación de swizzle es necesaria para seleccionar un componente.</span><span class="sxs-lookup"><span data-stu-id="74066-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="74066-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74066-130">Remarks</span></span>



| <span data-ttu-id="74066-131">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="74066-131">Pixel shader versions</span></span> | <span data-ttu-id="74066-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="74066-132">1\_1</span></span> | <span data-ttu-id="74066-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="74066-133">1\_2</span></span> | <span data-ttu-id="74066-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="74066-134">1\_3</span></span> | <span data-ttu-id="74066-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="74066-135">1\_4</span></span> | <span data-ttu-id="74066-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74066-136">2\_0</span></span> | <span data-ttu-id="74066-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="74066-137">2\_x</span></span> | <span data-ttu-id="74066-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="74066-138">2\_sw</span></span> | <span data-ttu-id="74066-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74066-139">3\_0</span></span> | <span data-ttu-id="74066-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="74066-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="74066-141">If \_ COMP</span><span class="sxs-lookup"><span data-stu-id="74066-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="74066-142">x</span><span class="sxs-lookup"><span data-stu-id="74066-142">x</span></span>    | <span data-ttu-id="74066-143">x</span><span class="sxs-lookup"><span data-stu-id="74066-143">x</span></span>     | <span data-ttu-id="74066-144">x</span><span class="sxs-lookup"><span data-stu-id="74066-144">x</span></span>    | <span data-ttu-id="74066-145">x</span><span class="sxs-lookup"><span data-stu-id="74066-145">x</span></span>     |



 

<span data-ttu-id="74066-146">Esta instrucción se usa para omitir un bloque de código, en función de una condición.</span><span class="sxs-lookup"><span data-stu-id="74066-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="74066-147">Tenga cuidado al usar los modos de comparación es igual a y no es igual a los números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="74066-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="74066-148">Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor de épsilon (número pequeño distinto de cero) para evitar errores.</span><span class="sxs-lookup"><span data-stu-id="74066-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="74066-149">Entre las restricciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="74066-149">Restrictions include:</span></span>

-   <span data-ttu-id="74066-150">If \_ comp... [else-PS](else---ps.md)... los bloques [endif-PS](endif---ps.md) (junto con los bloques [If](if-bool---ps.md) de predicado) se pueden anidar hasta 24 capas de profundidad.</span><span class="sxs-lookup"><span data-stu-id="74066-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="74066-151">los registros de src0 y SRC1 requieren un swizzle de replicación.</span><span class="sxs-lookup"><span data-stu-id="74066-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="74066-152">Si los \_ bloques de COMP deben terminar con una instrucción [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="74066-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="74066-153">If \_ comp... [else-PS](else---ps.md)... los bloques [endif-PS](endif---ps.md) no pueden ocupar un bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="74066-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="74066-154">El \_ bloque if COMP debe estar completamente dentro o fuera del bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="74066-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="74066-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74066-155">Example</span></span>

<span data-ttu-id="74066-156">Esta instrucción proporciona el control de flujo dinámico condicional.</span><span class="sxs-lookup"><span data-stu-id="74066-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="74066-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74066-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74066-158">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="74066-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




