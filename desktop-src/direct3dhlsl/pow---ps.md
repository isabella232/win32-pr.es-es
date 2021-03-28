---
title: Pow-PS
description: SRC1 de precisión completa ABS (src0). | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986295"
---
# <a name="pow---ps"></a><span data-ttu-id="33097-104">Pow-PS</span><span class="sxs-lookup"><span data-stu-id="33097-104">pow - ps</span></span>

<span data-ttu-id="33097-105"><sup>SRC1</sup>de precisión completa ABS (src0).</span><span class="sxs-lookup"><span data-stu-id="33097-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="33097-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33097-106">Syntax</span></span>



| <span data-ttu-id="33097-107">Pow DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="33097-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="33097-108">, donde</span><span class="sxs-lookup"><span data-stu-id="33097-108">where</span></span>

-   <span data-ttu-id="33097-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="33097-109">dst is the destination register.</span></span>
-   <span data-ttu-id="33097-110">src0 es un registro de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="33097-110">src0 is an input source register.</span></span> <span data-ttu-id="33097-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="33097-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="33097-112">SRC1 es un registro de origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="33097-112">src1 is an input source register.</span></span> <span data-ttu-id="33097-113">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="33097-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="33097-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33097-114">Remarks</span></span>



| <span data-ttu-id="33097-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="33097-115">Pixel shader versions</span></span> | <span data-ttu-id="33097-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="33097-116">1\_1</span></span> | <span data-ttu-id="33097-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="33097-117">1\_2</span></span> | <span data-ttu-id="33097-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="33097-118">1\_3</span></span> | <span data-ttu-id="33097-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="33097-119">1\_4</span></span> | <span data-ttu-id="33097-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="33097-120">2\_0</span></span> | <span data-ttu-id="33097-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="33097-121">2\_x</span></span> | <span data-ttu-id="33097-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="33097-122">2\_sw</span></span> | <span data-ttu-id="33097-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="33097-123">3\_0</span></span> | <span data-ttu-id="33097-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="33097-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="33097-125">pow</span><span class="sxs-lookup"><span data-stu-id="33097-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="33097-126">x</span><span class="sxs-lookup"><span data-stu-id="33097-126">x</span></span>    | <span data-ttu-id="33097-127">x</span><span class="sxs-lookup"><span data-stu-id="33097-127">x</span></span>    | <span data-ttu-id="33097-128">x</span><span class="sxs-lookup"><span data-stu-id="33097-128">x</span></span>     | <span data-ttu-id="33097-129">x</span><span class="sxs-lookup"><span data-stu-id="33097-129">x</span></span>    | <span data-ttu-id="33097-130">x</span><span class="sxs-lookup"><span data-stu-id="33097-130">x</span></span>     |



 

<span data-ttu-id="33097-131">Esta instrucción funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="33097-131">This instruction works as follows:</span></span>

<span data-ttu-id="33097-132">dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>SRC1</sup>;</span><span class="sxs-lookup"><span data-stu-id="33097-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="33097-133">Se trata de una instrucción escalar, por lo que los registros de origen deben tener replicar swizzles para indicar qué canales se usan.</span><span class="sxs-lookup"><span data-stu-id="33097-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="33097-134">La potencia de entrada (SRC1) debe ser un escalar.</span><span class="sxs-lookup"><span data-stu-id="33097-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="33097-135">El resultado escalar se replica en los cuatro canales de salida.</span><span class="sxs-lookup"><span data-stu-id="33097-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="33097-136">Esta instrucción se puede expandir como exp (SRC1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="33097-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="33097-137">El registro de DST debe ser un registro temporal y no debe ser el mismo registro que SRC1.</span><span class="sxs-lookup"><span data-stu-id="33097-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33097-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33097-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33097-139">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="33097-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




