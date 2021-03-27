---
title: DST-vs
description: Calcula un vector de distancia. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914345"
---
# <a name="dst---vs"></a><span data-ttu-id="57acb-104">DST-vs</span><span class="sxs-lookup"><span data-stu-id="57acb-104">dst - vs</span></span>

<span data-ttu-id="57acb-105">Calcula un vector de distancia.</span><span class="sxs-lookup"><span data-stu-id="57acb-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="57acb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57acb-106">Syntax</span></span>



| <span data-ttu-id="57acb-107">DST Dest, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="57acb-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="57acb-108">, donde</span><span class="sxs-lookup"><span data-stu-id="57acb-108">where</span></span>

-   <span data-ttu-id="57acb-109">dest es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="57acb-109">dest is the destination register.</span></span>
-   <span data-ttu-id="57acb-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="57acb-110">src0 is a source register.</span></span>
-   <span data-ttu-id="57acb-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="57acb-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="57acb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57acb-112">Remarks</span></span>



| <span data-ttu-id="57acb-113">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="57acb-113">Vertex shader versions</span></span> | <span data-ttu-id="57acb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="57acb-114">1\_1</span></span> | <span data-ttu-id="57acb-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57acb-115">2\_0</span></span> | <span data-ttu-id="57acb-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="57acb-116">2\_x</span></span> | <span data-ttu-id="57acb-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="57acb-117">2\_sw</span></span> | <span data-ttu-id="57acb-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="57acb-118">3\_0</span></span> | <span data-ttu-id="57acb-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="57acb-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="57acb-120">DST</span><span class="sxs-lookup"><span data-stu-id="57acb-120">dst</span></span>                    | <span data-ttu-id="57acb-121">x</span><span class="sxs-lookup"><span data-stu-id="57acb-121">x</span></span>    | <span data-ttu-id="57acb-122">x</span><span class="sxs-lookup"><span data-stu-id="57acb-122">x</span></span>    | <span data-ttu-id="57acb-123">x</span><span class="sxs-lookup"><span data-stu-id="57acb-123">x</span></span>    | <span data-ttu-id="57acb-124">x</span><span class="sxs-lookup"><span data-stu-id="57acb-124">x</span></span>     | <span data-ttu-id="57acb-125">x</span><span class="sxs-lookup"><span data-stu-id="57acb-125">x</span></span>    | <span data-ttu-id="57acb-126">x</span><span class="sxs-lookup"><span data-stu-id="57acb-126">x</span></span>     |



 

<span data-ttu-id="57acb-127">En el siguiente fragmento de código se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="57acb-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="57acb-128">Se supone que el primer operando de origen (src0) es el vector (omitido, d d \* , d d \* , omitido) y el segundo operando de origen (SRC1) es el vector (omitido, 1/d, omitido, 1/d).</span><span class="sxs-lookup"><span data-stu-id="57acb-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="57acb-129">El destino (DEST) es el vector del resultado (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="57acb-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="57acb-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57acb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57acb-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="57acb-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




