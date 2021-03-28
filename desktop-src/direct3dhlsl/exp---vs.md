---
title: EXP-vs
description: Proporciona el doble de precisión exponencial. | EXP-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998221"
---
# <a name="exp---vs"></a><span data-ttu-id="cc175-104">EXP-vs</span><span class="sxs-lookup"><span data-stu-id="cc175-104">exp - vs</span></span>

<span data-ttu-id="cc175-105">Proporciona una precisión completa exponencial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="cc175-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc175-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc175-106">Syntax</span></span>



| <span data-ttu-id="cc175-107">EXP DST, src</span><span class="sxs-lookup"><span data-stu-id="cc175-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="cc175-108">, donde</span><span class="sxs-lookup"><span data-stu-id="cc175-108">where</span></span>

-   <span data-ttu-id="cc175-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cc175-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cc175-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cc175-110">src is a source register.</span></span> <span data-ttu-id="cc175-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="cc175-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="cc175-112">Consulte [source Register permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="cc175-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc175-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc175-113">Remarks</span></span>



| <span data-ttu-id="cc175-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="cc175-114">Vertex shader versions</span></span> | <span data-ttu-id="cc175-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc175-115">1\_1</span></span> | <span data-ttu-id="cc175-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc175-116">2\_0</span></span> | <span data-ttu-id="cc175-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc175-117">2\_x</span></span> | <span data-ttu-id="cc175-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc175-118">2\_sw</span></span> | <span data-ttu-id="cc175-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc175-119">3\_0</span></span> | <span data-ttu-id="cc175-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc175-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cc175-121">exp</span><span class="sxs-lookup"><span data-stu-id="cc175-121">exp</span></span>                    | <span data-ttu-id="cc175-122">x</span><span class="sxs-lookup"><span data-stu-id="cc175-122">x</span></span>    | <span data-ttu-id="cc175-123">x</span><span class="sxs-lookup"><span data-stu-id="cc175-123">x</span></span>    | <span data-ttu-id="cc175-124">x</span><span class="sxs-lookup"><span data-stu-id="cc175-124">x</span></span>    | <span data-ttu-id="cc175-125">x</span><span class="sxs-lookup"><span data-stu-id="cc175-125">x</span></span>     | <span data-ttu-id="cc175-126">x</span><span class="sxs-lookup"><span data-stu-id="cc175-126">x</span></span>    | <span data-ttu-id="cc175-127">x</span><span class="sxs-lookup"><span data-stu-id="cc175-127">x</span></span>     |



 

<span data-ttu-id="cc175-128">Esta instrucción proporciona al menos 21 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="cc175-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="cc175-129">En el siguiente fragmento de código se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="cc175-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="cc175-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc175-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc175-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="cc175-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




