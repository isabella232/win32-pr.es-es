---
title: 'registro: PS'
description: '₂ de registro de precisión completa (x). | registro: PS'
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986689"
---
# <a name="log---ps"></a><span data-ttu-id="e4070-104">registro: PS</span><span class="sxs-lookup"><span data-stu-id="e4070-104">log - ps</span></span>

<span data-ttu-id="e4070-105">₂ de registro de precisión completa (x).</span><span class="sxs-lookup"><span data-stu-id="e4070-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4070-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4070-106">Syntax</span></span>



| <span data-ttu-id="e4070-107">DST de registro, src</span><span class="sxs-lookup"><span data-stu-id="e4070-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e4070-108">, donde</span><span class="sxs-lookup"><span data-stu-id="e4070-108">where</span></span>

-   <span data-ttu-id="e4070-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e4070-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e4070-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="e4070-110">src is a source register.</span></span> <span data-ttu-id="e4070-111">El registro de origen requiere el uso explícito de replicate swizzle; es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="e4070-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4070-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4070-112">Remarks</span></span>



| <span data-ttu-id="e4070-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e4070-113">Pixel shader versions</span></span> | <span data-ttu-id="e4070-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e4070-114">1\_1</span></span> | <span data-ttu-id="e4070-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e4070-115">1\_2</span></span> | <span data-ttu-id="e4070-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e4070-116">1\_3</span></span> | <span data-ttu-id="e4070-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e4070-117">1\_4</span></span> | <span data-ttu-id="e4070-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4070-118">2\_0</span></span> | <span data-ttu-id="e4070-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e4070-119">2\_x</span></span> | <span data-ttu-id="e4070-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4070-120">2\_sw</span></span> | <span data-ttu-id="e4070-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4070-121">3\_0</span></span> | <span data-ttu-id="e4070-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e4070-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e4070-123">log</span><span class="sxs-lookup"><span data-stu-id="e4070-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="e4070-124">x</span><span class="sxs-lookup"><span data-stu-id="e4070-124">x</span></span>    | <span data-ttu-id="e4070-125">x</span><span class="sxs-lookup"><span data-stu-id="e4070-125">x</span></span>    | <span data-ttu-id="e4070-126">x</span><span class="sxs-lookup"><span data-stu-id="e4070-126">x</span></span>     | <span data-ttu-id="e4070-127">x</span><span class="sxs-lookup"><span data-stu-id="e4070-127">x</span></span>    | <span data-ttu-id="e4070-128">x</span><span class="sxs-lookup"><span data-stu-id="e4070-128">x</span></span>     |



 

<span data-ttu-id="e4070-129">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="e4070-129">The following code snippet shows the operations performed.</span></span>


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



<span data-ttu-id="e4070-130">Esta instrucción acepta un origen escalar cuyo bit de signo se omite.</span><span class="sxs-lookup"><span data-stu-id="e4070-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="e4070-131">El resultado se replica en los cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="e4070-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4070-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4070-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4070-133">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e4070-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




