---
title: EXPP-vs
description: Proporciona el doble de precisión parcial exponencial.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784942"
---
# <a name="expp---vs"></a><span data-ttu-id="b6f96-103">EXPP-vs</span><span class="sxs-lookup"><span data-stu-id="b6f96-103">expp - vs</span></span>

<span data-ttu-id="b6f96-104">Proporciona una precisión parcial exponencial 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="b6f96-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6f96-105">Syntax</span></span>



| <span data-ttu-id="b6f96-106">EXPP DST, src. x1</span><span class="sxs-lookup"><span data-stu-id="b6f96-106">expp dst, src.{x\</span></span>|<span data-ttu-id="b6f96-107">sí</span><span class="sxs-lookup"><span data-stu-id="b6f96-107">y\</span></span>|<span data-ttu-id="b6f96-108">z</span><span class="sxs-lookup"><span data-stu-id="b6f96-108">z\</span></span>|<span data-ttu-id="b6f96-109">con</span><span class="sxs-lookup"><span data-stu-id="b6f96-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="b6f96-110">Donde:</span><span class="sxs-lookup"><span data-stu-id="b6f96-110">Where:</span></span>

-   <span data-ttu-id="b6f96-111">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b6f96-111">dst is the destination register.</span></span>
-   <span data-ttu-id="b6f96-112">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="b6f96-112">src is a source register.</span></span> <span data-ttu-id="b6f96-113">El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="b6f96-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="b6f96-114">{x \| y \| z \| w} es el swizzle de replicación necesario en el registro de código fuente.</span><span class="sxs-lookup"><span data-stu-id="b6f96-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f96-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6f96-115">Remarks</span></span>



| <span data-ttu-id="b6f96-116">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b6f96-116">Vertex shader versions</span></span> | <span data-ttu-id="b6f96-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="b6f96-117">1\_1</span></span> | <span data-ttu-id="b6f96-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6f96-118">2\_0</span></span> | <span data-ttu-id="b6f96-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b6f96-119">2\_x</span></span> | <span data-ttu-id="b6f96-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6f96-120">2\_sw</span></span> | <span data-ttu-id="b6f96-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6f96-121">3\_0</span></span> | <span data-ttu-id="b6f96-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6f96-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b6f96-123">expp</span><span class="sxs-lookup"><span data-stu-id="b6f96-123">expp</span></span>                   | <span data-ttu-id="b6f96-124">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-124">x</span></span>    | <span data-ttu-id="b6f96-125">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-125">x</span></span>    | <span data-ttu-id="b6f96-126">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-126">x</span></span>    | <span data-ttu-id="b6f96-127">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-127">x</span></span>     | <span data-ttu-id="b6f96-128">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-128">x</span></span>    | <span data-ttu-id="b6f96-129">x</span><span class="sxs-lookup"><span data-stu-id="b6f96-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="b6f96-130">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b6f96-130">vs\_1\_1</span></span>

<span data-ttu-id="b6f96-131">La instrucción [exp-vs](exp---vs.md) funciona de forma diferente en función de las versiones del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="b6f96-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="b6f96-132">En vs \_ 1 \_ 1, la instrucción EXPP proporciona los siguientes resultados:</span><span class="sxs-lookup"><span data-stu-id="b6f96-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="b6f96-133">En vs \_ 2 \_ 0 y up, la instrucción EXPP proporciona los siguientes resultados:</span><span class="sxs-lookup"><span data-stu-id="b6f96-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="b6f96-134">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6f96-134">vs\_2\_0</span></span>

<span data-ttu-id="b6f96-135">En vs \_ 2 \_ 0 y up, la instrucción funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b6f96-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="b6f96-136">La instrucción proporciona al menos 10 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="b6f96-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6f96-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6f96-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6f96-138">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b6f96-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




