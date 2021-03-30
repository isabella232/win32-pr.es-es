---
title: callnz bool-PS
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998280"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="56eb6-105">callnz bool-PS</span><span class="sxs-lookup"><span data-stu-id="56eb6-105">callnz bool - ps</span></span>

<span data-ttu-id="56eb6-106">Llame a si no es cero.</span><span class="sxs-lookup"><span data-stu-id="56eb6-106">Call if not zero.</span></span> <span data-ttu-id="56eb6-107">Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="56eb6-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="56eb6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56eb6-108">Syntax</span></span>



| <span data-ttu-id="56eb6-109">callnz l \# , \[ ! \] b\#</span><span class="sxs-lookup"><span data-stu-id="56eb6-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="56eb6-110">Donde:</span><span class="sxs-lookup"><span data-stu-id="56eb6-110">Where:</span></span>

-   <span data-ttu-id="56eb6-111">l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="56eb6-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="56eb6-112">\[!\] es un modificador opcional Negate.</span><span class="sxs-lookup"><span data-stu-id="56eb6-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="56eb6-113">b \# identifica un [registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="56eb6-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56eb6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56eb6-114">Remarks</span></span>



| <span data-ttu-id="56eb6-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="56eb6-115">Pixel shader versions</span></span> | <span data-ttu-id="56eb6-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="56eb6-116">1\_1</span></span> | <span data-ttu-id="56eb6-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="56eb6-117">1\_2</span></span> | <span data-ttu-id="56eb6-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="56eb6-118">1\_3</span></span> | <span data-ttu-id="56eb6-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="56eb6-119">1\_4</span></span> | <span data-ttu-id="56eb6-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56eb6-120">2\_0</span></span> | <span data-ttu-id="56eb6-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="56eb6-121">2\_x</span></span> | <span data-ttu-id="56eb6-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56eb6-122">2\_sw</span></span> | <span data-ttu-id="56eb6-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56eb6-123">3\_0</span></span> | <span data-ttu-id="56eb6-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56eb6-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="56eb6-125">callnz bool</span><span class="sxs-lookup"><span data-stu-id="56eb6-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="56eb6-126">x</span><span class="sxs-lookup"><span data-stu-id="56eb6-126">x</span></span>    | <span data-ttu-id="56eb6-127">x</span><span class="sxs-lookup"><span data-stu-id="56eb6-127">x</span></span>     | <span data-ttu-id="56eb6-128">x</span><span class="sxs-lookup"><span data-stu-id="56eb6-128">x</span></span>    | <span data-ttu-id="56eb6-129">x</span><span class="sxs-lookup"><span data-stu-id="56eb6-129">x</span></span>     |



 

<span data-ttu-id="56eb6-130">Esta instrucción hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56eb6-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="56eb6-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56eb6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56eb6-132">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="56eb6-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




