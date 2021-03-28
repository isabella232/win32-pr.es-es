---
title: EXP-PS
description: Proporciona el doble de precisión exponencial. | EXP-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083626"
---
# <a name="exp---ps"></a><span data-ttu-id="f5d25-104">EXP-PS</span><span class="sxs-lookup"><span data-stu-id="f5d25-104">exp - ps</span></span>

<span data-ttu-id="f5d25-105">Proporciona una precisión completa exponencial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="f5d25-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d25-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d25-106">Syntax</span></span>



| <span data-ttu-id="f5d25-107">EXP DST, src</span><span class="sxs-lookup"><span data-stu-id="f5d25-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="f5d25-108">, donde</span><span class="sxs-lookup"><span data-stu-id="f5d25-108">where</span></span>

-   <span data-ttu-id="f5d25-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="f5d25-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f5d25-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="f5d25-110">src is a source register.</span></span> <span data-ttu-id="f5d25-111">El registro de origen requiere el uso explícito de replicate swizzle; es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="f5d25-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="f5d25-112">Consulte [source Register permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="f5d25-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d25-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5d25-113">Remarks</span></span>



| <span data-ttu-id="f5d25-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f5d25-114">Pixel shader versions</span></span> | <span data-ttu-id="f5d25-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f5d25-115">1\_1</span></span> | <span data-ttu-id="f5d25-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="f5d25-116">1\_2</span></span> | <span data-ttu-id="f5d25-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f5d25-117">1\_3</span></span> | <span data-ttu-id="f5d25-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="f5d25-118">1\_4</span></span> | <span data-ttu-id="f5d25-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5d25-119">2\_0</span></span> | <span data-ttu-id="f5d25-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f5d25-120">2\_x</span></span> | <span data-ttu-id="f5d25-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5d25-121">2\_sw</span></span> | <span data-ttu-id="f5d25-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5d25-122">3\_0</span></span> | <span data-ttu-id="f5d25-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5d25-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f5d25-124">exp</span><span class="sxs-lookup"><span data-stu-id="f5d25-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="f5d25-125">x</span><span class="sxs-lookup"><span data-stu-id="f5d25-125">x</span></span>    | <span data-ttu-id="f5d25-126">x</span><span class="sxs-lookup"><span data-stu-id="f5d25-126">x</span></span>    | <span data-ttu-id="f5d25-127">x</span><span class="sxs-lookup"><span data-stu-id="f5d25-127">x</span></span>     | <span data-ttu-id="f5d25-128">x</span><span class="sxs-lookup"><span data-stu-id="f5d25-128">x</span></span>    | <span data-ttu-id="f5d25-129">x</span><span class="sxs-lookup"><span data-stu-id="f5d25-129">x</span></span>     |



 

<span data-ttu-id="f5d25-130">En el fragmento de código siguiente se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="f5d25-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="f5d25-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5d25-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d25-132">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f5d25-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




