---
title: Pow-vs
description: SRC1 de precisión completa ABS (src0). | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279980"
---
# <a name="pow---vs"></a><span data-ttu-id="00ef5-104">Pow-vs</span><span class="sxs-lookup"><span data-stu-id="00ef5-104">pow - vs</span></span>

<span data-ttu-id="00ef5-105"><sup>SRC1</sup>de precisión completa ABS (src0).</span><span class="sxs-lookup"><span data-stu-id="00ef5-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ef5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00ef5-106">Syntax</span></span>



| <span data-ttu-id="00ef5-107">Pow DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="00ef5-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="00ef5-108">, donde</span><span class="sxs-lookup"><span data-stu-id="00ef5-108">where</span></span>

-   <span data-ttu-id="00ef5-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="00ef5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="00ef5-110">src0 es un registro de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="00ef5-110">src0 is an input source register.</span></span> <span data-ttu-id="00ef5-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="00ef5-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="00ef5-112">SRC1 es un registro de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="00ef5-112">src1 is an input source register.</span></span> <span data-ttu-id="00ef5-113">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="00ef5-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ef5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00ef5-114">Remarks</span></span>



| <span data-ttu-id="00ef5-115">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="00ef5-115">Vertex shader versions</span></span> | <span data-ttu-id="00ef5-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="00ef5-116">1\_1</span></span> | <span data-ttu-id="00ef5-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00ef5-117">2\_0</span></span> | <span data-ttu-id="00ef5-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="00ef5-118">2\_x</span></span> | <span data-ttu-id="00ef5-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="00ef5-119">2\_sw</span></span> | <span data-ttu-id="00ef5-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00ef5-120">3\_0</span></span> | <span data-ttu-id="00ef5-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="00ef5-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="00ef5-122">pow</span><span class="sxs-lookup"><span data-stu-id="00ef5-122">pow</span></span>                    |      | <span data-ttu-id="00ef5-123">x</span><span class="sxs-lookup"><span data-stu-id="00ef5-123">x</span></span>    | <span data-ttu-id="00ef5-124">x</span><span class="sxs-lookup"><span data-stu-id="00ef5-124">x</span></span>    | <span data-ttu-id="00ef5-125">x</span><span class="sxs-lookup"><span data-stu-id="00ef5-125">x</span></span>     | <span data-ttu-id="00ef5-126">x</span><span class="sxs-lookup"><span data-stu-id="00ef5-126">x</span></span>    | <span data-ttu-id="00ef5-127">x</span><span class="sxs-lookup"><span data-stu-id="00ef5-127">x</span></span>     |



 

<span data-ttu-id="00ef5-128">Esta instrucción funciona como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="00ef5-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="00ef5-129">Se trata de una instrucción escalar, por lo que los registros de origen deben tener replicar swizzles para indicar qué canales se usan.</span><span class="sxs-lookup"><span data-stu-id="00ef5-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="00ef5-130">El resultado escalar se replica en los cuatro canales de salida.</span><span class="sxs-lookup"><span data-stu-id="00ef5-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="00ef5-131">Esta instrucción se puede expandir como exp (SRC1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="00ef5-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="00ef5-132">La precisión no es inferior a 15 bits.</span><span class="sxs-lookup"><span data-stu-id="00ef5-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="00ef5-133">El registro de destino debe ser un registro temporal y no debe ser el mismo registro que SRC1.</span><span class="sxs-lookup"><span data-stu-id="00ef5-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ef5-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00ef5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ef5-135">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="00ef5-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




