---
title: callnz Pred-vs
description: Llame a si no es cero, con un predicado. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077092"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="c4089-105">callnz Pred-vs</span><span class="sxs-lookup"><span data-stu-id="c4089-105">callnz pred - vs</span></span>

<span data-ttu-id="c4089-106">Llame a si no es cero, con un predicado.</span><span class="sxs-lookup"><span data-stu-id="c4089-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="c4089-107">Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c4089-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="c4089-108">Predication usa un valor booleano para determinar si no se va a realizar la instrucción.</span><span class="sxs-lookup"><span data-stu-id="c4089-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4089-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4089-109">Syntax</span></span>



| <span data-ttu-id="c4089-110">callnz l \# , \[ ! \] P0. x1</span><span class="sxs-lookup"><span data-stu-id="c4089-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="c4089-111">sí</span><span class="sxs-lookup"><span data-stu-id="c4089-111">y\</span></span>|<span data-ttu-id="c4089-112">z</span><span class="sxs-lookup"><span data-stu-id="c4089-112">z\</span></span>|<span data-ttu-id="c4089-113">con</span><span class="sxs-lookup"><span data-stu-id="c4089-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="c4089-114">donde:</span><span class="sxs-lookup"><span data-stu-id="c4089-114">where:</span></span>

-   <span data-ttu-id="c4089-115">l \# es una [etiqueta, frente](label---vs.md) al marcado del principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="c4089-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="c4089-116">\[!\] es un modificador opcional Negate.</span><span class="sxs-lookup"><span data-stu-id="c4089-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="c4089-117">P0 es el [registro del predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c4089-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="c4089-118">{x \| y \| z \| w} es el swizzle de replicación necesario en P0.</span><span class="sxs-lookup"><span data-stu-id="c4089-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4089-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4089-119">Remarks</span></span>



| <span data-ttu-id="c4089-120">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c4089-120">Vertex shader versions</span></span> | <span data-ttu-id="c4089-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="c4089-121">1\_1</span></span> | <span data-ttu-id="c4089-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4089-122">2\_0</span></span> | <span data-ttu-id="c4089-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4089-123">2\_x</span></span> | <span data-ttu-id="c4089-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c4089-124">2\_sw</span></span> | <span data-ttu-id="c4089-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4089-125">3\_0</span></span> | <span data-ttu-id="c4089-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c4089-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c4089-127">callnz Pred</span><span class="sxs-lookup"><span data-stu-id="c4089-127">callnz pred</span></span>            |      |      | <span data-ttu-id="c4089-128">x</span><span class="sxs-lookup"><span data-stu-id="c4089-128">x</span></span>    | <span data-ttu-id="c4089-129">x</span><span class="sxs-lookup"><span data-stu-id="c4089-129">x</span></span>     | <span data-ttu-id="c4089-130">x</span><span class="sxs-lookup"><span data-stu-id="c4089-130">x</span></span>    | <span data-ttu-id="c4089-131">x</span><span class="sxs-lookup"><span data-stu-id="c4089-131">x</span></span>     |



 

<span data-ttu-id="c4089-132">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4089-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="c4089-133">Esta instrucción usa una ranura de instrucciones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="c4089-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4089-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4089-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4089-135">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c4089-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




