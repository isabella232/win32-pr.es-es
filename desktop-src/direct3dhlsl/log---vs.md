---
title: log-vs
description: ₂ de registro de precisión completa (x). | log-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280082"
---
# <a name="log---vs"></a><span data-ttu-id="bb05a-104">log-vs</span><span class="sxs-lookup"><span data-stu-id="bb05a-104">log - vs</span></span>

<span data-ttu-id="bb05a-105">₂ de registro de precisión completa (x).</span><span class="sxs-lookup"><span data-stu-id="bb05a-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb05a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb05a-106">Syntax</span></span>



| <span data-ttu-id="bb05a-107">DST de registro, src</span><span class="sxs-lookup"><span data-stu-id="bb05a-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="bb05a-108">, donde</span><span class="sxs-lookup"><span data-stu-id="bb05a-108">where</span></span>

-   <span data-ttu-id="bb05a-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bb05a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bb05a-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="bb05a-110">src is a source register.</span></span> <span data-ttu-id="bb05a-111">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="bb05a-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb05a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb05a-112">Remarks</span></span>



| <span data-ttu-id="bb05a-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="bb05a-113">Vertex shader versions</span></span> | <span data-ttu-id="bb05a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="bb05a-114">1\_1</span></span> | <span data-ttu-id="bb05a-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb05a-115">2\_0</span></span> | <span data-ttu-id="bb05a-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bb05a-116">2\_x</span></span> | <span data-ttu-id="bb05a-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bb05a-117">2\_sw</span></span> | <span data-ttu-id="bb05a-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bb05a-118">3\_0</span></span> | <span data-ttu-id="bb05a-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bb05a-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bb05a-120">log</span><span class="sxs-lookup"><span data-stu-id="bb05a-120">log</span></span>                    | <span data-ttu-id="bb05a-121">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-121">x</span></span>    | <span data-ttu-id="bb05a-122">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-122">x</span></span>    | <span data-ttu-id="bb05a-123">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-123">x</span></span>    | <span data-ttu-id="bb05a-124">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-124">x</span></span>     | <span data-ttu-id="bb05a-125">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-125">x</span></span>    | <span data-ttu-id="bb05a-126">x</span><span class="sxs-lookup"><span data-stu-id="bb05a-126">x</span></span>     |



 

<span data-ttu-id="bb05a-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="bb05a-127">The following code fragment shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="bb05a-128">Esta instrucción acepta un origen escalar cuyo bit de signo se omite.</span><span class="sxs-lookup"><span data-stu-id="bb05a-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="bb05a-129">El resultado se replica en los cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="bb05a-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="bb05a-130">Esta instrucción proporciona 21 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="bb05a-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb05a-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb05a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb05a-132">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="bb05a-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




