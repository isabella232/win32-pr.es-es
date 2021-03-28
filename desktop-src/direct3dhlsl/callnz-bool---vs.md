---
title: callnz bool-vs
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998275"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="24419-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="24419-105">callnz bool - vs</span></span>

<span data-ttu-id="24419-106">Llame a si no es cero.</span><span class="sxs-lookup"><span data-stu-id="24419-106">Call if not zero.</span></span> <span data-ttu-id="24419-107">Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="24419-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="24419-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24419-108">Syntax</span></span>



| <span data-ttu-id="24419-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="24419-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="24419-110">donde:</span><span class="sxs-lookup"><span data-stu-id="24419-110">where:</span></span>

-   <span data-ttu-id="24419-111">donde l \# es una [etiqueta,](label---vs.md) que marca el principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="24419-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="24419-112">\[!\] es el modificador booleano opcional NOT.</span><span class="sxs-lookup"><span data-stu-id="24419-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="24419-113">b \# identifica un [registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="24419-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="24419-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24419-114">Remarks</span></span>



| <span data-ttu-id="24419-115">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="24419-115">Vertex shader versions</span></span> | <span data-ttu-id="24419-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="24419-116">1\_1</span></span> | <span data-ttu-id="24419-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24419-117">2\_0</span></span> | <span data-ttu-id="24419-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="24419-118">2\_x</span></span> | <span data-ttu-id="24419-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24419-119">2\_sw</span></span> | <span data-ttu-id="24419-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24419-120">3\_0</span></span> | <span data-ttu-id="24419-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="24419-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="24419-122">callnz bool</span><span class="sxs-lookup"><span data-stu-id="24419-122">callnz bool</span></span>            |      | <span data-ttu-id="24419-123">x</span><span class="sxs-lookup"><span data-stu-id="24419-123">x</span></span>    | <span data-ttu-id="24419-124">x</span><span class="sxs-lookup"><span data-stu-id="24419-124">x</span></span>    | <span data-ttu-id="24419-125">x</span><span class="sxs-lookup"><span data-stu-id="24419-125">x</span></span>     | <span data-ttu-id="24419-126">x</span><span class="sxs-lookup"><span data-stu-id="24419-126">x</span></span>    | <span data-ttu-id="24419-127">x</span><span class="sxs-lookup"><span data-stu-id="24419-127">x</span></span>     |



 

<span data-ttu-id="24419-128">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="24419-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="24419-129">Esta instrucción usa una ranura de instrucciones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="24419-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24419-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24419-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24419-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="24419-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




