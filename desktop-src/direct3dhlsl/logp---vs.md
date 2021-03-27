---
title: logP-vs
description: Precisión parcial logP ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077101"
---
# <a name="logp---vs"></a><span data-ttu-id="a1ea1-103">logP-vs</span><span class="sxs-lookup"><span data-stu-id="a1ea1-103">logp - vs</span></span>

<span data-ttu-id="a1ea1-104">Precisión parcial logP ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="a1ea1-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ea1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1ea1-105">Syntax</span></span>



| <span data-ttu-id="a1ea1-106">logP DST, src</span><span class="sxs-lookup"><span data-stu-id="a1ea1-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="a1ea1-107">, donde</span><span class="sxs-lookup"><span data-stu-id="a1ea1-107">where</span></span>

-   <span data-ttu-id="a1ea1-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a1ea1-108">dst is the destination register.</span></span>
-   <span data-ttu-id="a1ea1-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="a1ea1-109">src is a source register.</span></span> <span data-ttu-id="a1ea1-110">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="a1ea1-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ea1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1ea1-111">Remarks</span></span>



| <span data-ttu-id="a1ea1-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a1ea1-112">Vertex shader versions</span></span> | <span data-ttu-id="a1ea1-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1ea1-113">1\_1</span></span> | <span data-ttu-id="a1ea1-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1ea1-114">2\_0</span></span> | <span data-ttu-id="a1ea1-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-115">2\_x</span></span> | <span data-ttu-id="a1ea1-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1ea1-116">2\_sw</span></span> | <span data-ttu-id="a1ea1-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1ea1-117">3\_0</span></span> | <span data-ttu-id="a1ea1-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1ea1-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1ea1-119">logp</span><span class="sxs-lookup"><span data-stu-id="a1ea1-119">logp</span></span>                   | <span data-ttu-id="a1ea1-120">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-120">x</span></span>    | <span data-ttu-id="a1ea1-121">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-121">x</span></span>    | <span data-ttu-id="a1ea1-122">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-122">x</span></span>    | <span data-ttu-id="a1ea1-123">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-123">x</span></span>     | <span data-ttu-id="a1ea1-124">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-124">x</span></span>    | <span data-ttu-id="a1ea1-125">x</span><span class="sxs-lookup"><span data-stu-id="a1ea1-125">x</span></span>     |



 

<span data-ttu-id="a1ea1-126">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="a1ea1-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="a1ea1-127">Esta instrucción proporciona una precisión parcial del logaritmo en base 2, hasta 10 bits.</span><span class="sxs-lookup"><span data-stu-id="a1ea1-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1ea1-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1ea1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ea1-129">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a1ea1-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




