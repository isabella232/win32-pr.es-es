---
title: if_comp-vs
description: 'Iniciar una expresión if bool-vs... Else-vs... endif: bloque de vs, con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.'
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996848"
---
# <a name="if_comp---vs"></a><span data-ttu-id="f2991-104">If \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="f2991-104">if\_comp - vs</span></span>

<span data-ttu-id="f2991-105">Iniciar una expresión [If bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif:](endif---vs.md) bloque de vs, con una condición basada en valores que podrían calcularse en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="f2991-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="f2991-106">Esta instrucción se usa para omitir un bloque de código, en función de una condición.</span><span class="sxs-lookup"><span data-stu-id="f2991-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2991-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2991-107">Syntax</span></span>



| <span data-ttu-id="f2991-108">If \_ COMP src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="f2991-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f2991-109">Donde:</span><span class="sxs-lookup"><span data-stu-id="f2991-109">Where:</span></span>

-   <span data-ttu-id="f2991-110">\_Comp es una comparación entre los dos registros de origen.</span><span class="sxs-lookup"><span data-stu-id="f2991-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="f2991-111">Puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2991-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="f2991-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2991-112">Syntax</span></span> | <span data-ttu-id="f2991-113">De comparación</span><span class="sxs-lookup"><span data-stu-id="f2991-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="f2991-114">\_bruto</span><span class="sxs-lookup"><span data-stu-id="f2991-114">\_gt</span></span>   | <span data-ttu-id="f2991-115">Mayor que</span><span class="sxs-lookup"><span data-stu-id="f2991-115">Greater than</span></span>          |
    | <span data-ttu-id="f2991-116">\_plazo</span><span class="sxs-lookup"><span data-stu-id="f2991-116">\_lt</span></span>   | <span data-ttu-id="f2991-117">Menor que</span><span class="sxs-lookup"><span data-stu-id="f2991-117">Less than</span></span>             |
    | <span data-ttu-id="f2991-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="f2991-118">\_ge</span></span>   | <span data-ttu-id="f2991-119">Mayor o igual que</span><span class="sxs-lookup"><span data-stu-id="f2991-119">Greater than or equal</span></span> |
    | <span data-ttu-id="f2991-120">\_cuarto</span><span class="sxs-lookup"><span data-stu-id="f2991-120">\_le</span></span>   | <span data-ttu-id="f2991-121">Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="f2991-121">Less than or equal</span></span>    |
    | <span data-ttu-id="f2991-122">\_ajustes</span><span class="sxs-lookup"><span data-stu-id="f2991-122">\_eq</span></span>   | <span data-ttu-id="f2991-123">Igual a</span><span class="sxs-lookup"><span data-stu-id="f2991-123">Equal to</span></span>              |
    | <span data-ttu-id="f2991-124">\_&</span><span class="sxs-lookup"><span data-stu-id="f2991-124">\_ne</span></span>   | <span data-ttu-id="f2991-125">No es igual a</span><span class="sxs-lookup"><span data-stu-id="f2991-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="f2991-126">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f2991-126">src0 is a source register.</span></span> <span data-ttu-id="f2991-127">La replicación de swizzle es necesaria para seleccionar un componente.</span><span class="sxs-lookup"><span data-stu-id="f2991-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="f2991-128">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f2991-128">src1 is a source register.</span></span> <span data-ttu-id="f2991-129">La replicación de swizzle es necesaria para seleccionar un componente.</span><span class="sxs-lookup"><span data-stu-id="f2991-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2991-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2991-130">Remarks</span></span>



| <span data-ttu-id="f2991-131">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f2991-131">Vertex shader versions</span></span> | <span data-ttu-id="f2991-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="f2991-132">1\_1</span></span> | <span data-ttu-id="f2991-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2991-133">2\_0</span></span> | <span data-ttu-id="f2991-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f2991-134">2\_x</span></span> | <span data-ttu-id="f2991-135">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f2991-135">2\_sw</span></span> | <span data-ttu-id="f2991-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2991-136">3\_0</span></span> | <span data-ttu-id="f2991-137">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f2991-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f2991-138">If \_ COMP</span><span class="sxs-lookup"><span data-stu-id="f2991-138">if\_comp</span></span>               |      |      | <span data-ttu-id="f2991-139">x</span><span class="sxs-lookup"><span data-stu-id="f2991-139">x</span></span>    | <span data-ttu-id="f2991-140">x</span><span class="sxs-lookup"><span data-stu-id="f2991-140">x</span></span>     | <span data-ttu-id="f2991-141">x</span><span class="sxs-lookup"><span data-stu-id="f2991-141">x</span></span>    | <span data-ttu-id="f2991-142">x</span><span class="sxs-lookup"><span data-stu-id="f2991-142">x</span></span>     |



 

<span data-ttu-id="f2991-143">Esta instrucción se usa para omitir un bloque de código, en función de una condición.</span><span class="sxs-lookup"><span data-stu-id="f2991-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="f2991-144">Tenga cuidado al usar los modos de comparación es igual a y no es igual a los números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f2991-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="f2991-145">Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor de épsilon (número pequeño distinto de cero) para evitar errores.</span><span class="sxs-lookup"><span data-stu-id="f2991-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="f2991-146">Entre las restricciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f2991-146">Restrictions include:</span></span>

-   <span data-ttu-id="f2991-147">If \_ comp... [else-vs](else---vs.md)... [endif:](endif---vs.md) los bloques vs (junto con los bloques if de predicado) se pueden anidar hasta 24 capas de profundidad.</span><span class="sxs-lookup"><span data-stu-id="f2991-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="f2991-148">los registros de src0 y SRC1 requieren un swizzle de replicación.</span><span class="sxs-lookup"><span data-stu-id="f2991-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="f2991-149">Si los \_ bloques de COMP deben terminar con una instrucción [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f2991-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="f2991-150">If \_ comp... [else-vs](else---vs.md)... [endif: los bloques de vs](endif---vs.md) no pueden ocupar un bloque de bucle.</span><span class="sxs-lookup"><span data-stu-id="f2991-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="f2991-151">El \_ bloque if COMP debe estar completamente dentro o fuera del bloque [Loop-vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f2991-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="f2991-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2991-152">Example</span></span>

<span data-ttu-id="f2991-153">Esta instrucción proporciona el control de flujo dinámico condicional.</span><span class="sxs-lookup"><span data-stu-id="f2991-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="f2991-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2991-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2991-155">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f2991-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




