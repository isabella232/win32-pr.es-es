---
title: callnz Pred-PS
description: Llame a con un predicado, si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994829"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="2f5ff-105">callnz Pred-PS</span><span class="sxs-lookup"><span data-stu-id="2f5ff-105">callnz pred - ps</span></span>

<span data-ttu-id="2f5ff-106">Llame a con un predicado, si no es cero.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="2f5ff-107">Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="2f5ff-108">Predication usa un valor booleano para determinar si no se va a realizar la instrucción.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5ff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f5ff-109">Syntax</span></span>



| <span data-ttu-id="2f5ff-110">callnz l \# , \[ ! \] P0. x1</span><span class="sxs-lookup"><span data-stu-id="2f5ff-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="2f5ff-111">sí</span><span class="sxs-lookup"><span data-stu-id="2f5ff-111">y\</span></span>|<span data-ttu-id="2f5ff-112">z</span><span class="sxs-lookup"><span data-stu-id="2f5ff-112">z\</span></span>|<span data-ttu-id="2f5ff-113">con</span><span class="sxs-lookup"><span data-stu-id="2f5ff-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="2f5ff-114">Donde:</span><span class="sxs-lookup"><span data-stu-id="2f5ff-114">Where:</span></span>

-   <span data-ttu-id="2f5ff-115">donde l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="2f5ff-116">\[!\] es un modificador opcional Negate.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="2f5ff-117">P0 es el registro del predicado.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-117">p0 is the predicate register.</span></span> <span data-ttu-id="2f5ff-118">Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2f5ff-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="2f5ff-119">{x \| y \| z \| w} es el swizzle de replicación necesario en P0.</span><span class="sxs-lookup"><span data-stu-id="2f5ff-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5ff-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f5ff-120">Remarks</span></span>



| <span data-ttu-id="2f5ff-121">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2f5ff-121">Pixel shader versions</span></span> | <span data-ttu-id="2f5ff-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="2f5ff-122">1\_1</span></span> | <span data-ttu-id="2f5ff-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="2f5ff-123">1\_2</span></span> | <span data-ttu-id="2f5ff-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2f5ff-124">1\_3</span></span> | <span data-ttu-id="2f5ff-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="2f5ff-125">1\_4</span></span> | <span data-ttu-id="2f5ff-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5ff-126">2\_0</span></span> | <span data-ttu-id="2f5ff-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f5ff-127">2\_x</span></span> | <span data-ttu-id="2f5ff-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f5ff-128">2\_sw</span></span> | <span data-ttu-id="2f5ff-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5ff-129">3\_0</span></span> | <span data-ttu-id="2f5ff-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f5ff-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2f5ff-131">callnz Pred</span><span class="sxs-lookup"><span data-stu-id="2f5ff-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="2f5ff-132">x</span><span class="sxs-lookup"><span data-stu-id="2f5ff-132">x</span></span>    | <span data-ttu-id="2f5ff-133">x</span><span class="sxs-lookup"><span data-stu-id="2f5ff-133">x</span></span>     | <span data-ttu-id="2f5ff-134">x</span><span class="sxs-lookup"><span data-stu-id="2f5ff-134">x</span></span>    | <span data-ttu-id="2f5ff-135">x</span><span class="sxs-lookup"><span data-stu-id="2f5ff-135">x</span></span>     |



 

<span data-ttu-id="2f5ff-136">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2f5ff-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="2f5ff-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f5ff-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f5ff-138">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2f5ff-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




