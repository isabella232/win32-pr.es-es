---
title: m3x2-PS
description: Multiplica un vector de tres componentes por una matriz de 3x2. | m3x2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986688"
---
# <a name="m3x2---ps"></a><span data-ttu-id="1b029-104">m3x2-PS</span><span class="sxs-lookup"><span data-stu-id="1b029-104">m3x2 - ps</span></span>

<span data-ttu-id="1b029-105">Multiplica un vector de tres componentes por una matriz de 3x2.</span><span class="sxs-lookup"><span data-stu-id="1b029-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b029-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b029-106">Syntax</span></span>



| <span data-ttu-id="1b029-107">m3x2 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="1b029-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="1b029-108">, donde</span><span class="sxs-lookup"><span data-stu-id="1b029-108">where</span></span>

-   <span data-ttu-id="1b029-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="1b029-109">dst is the destination register.</span></span> <span data-ttu-id="1b029-110">El resultado es un vector de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="1b029-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="1b029-111">src0 es un registro de origen que representa un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="1b029-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="1b029-112">SRC1 es un registro de origen que representa una matriz de 3x2, que corresponde al primer de 2 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1b029-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b029-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b029-113">Remarks</span></span>



| <span data-ttu-id="1b029-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1b029-114">Pixel shader versions</span></span> | <span data-ttu-id="1b029-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="1b029-115">1\_1</span></span> | <span data-ttu-id="1b029-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="1b029-116">1\_2</span></span> | <span data-ttu-id="1b029-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1b029-117">1\_3</span></span> | <span data-ttu-id="1b029-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="1b029-118">1\_4</span></span> | <span data-ttu-id="1b029-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b029-119">2\_0</span></span> | <span data-ttu-id="1b029-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1b029-120">2\_x</span></span> | <span data-ttu-id="1b029-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b029-121">2\_sw</span></span> | <span data-ttu-id="1b029-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b029-122">3\_0</span></span> | <span data-ttu-id="1b029-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1b029-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1b029-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="1b029-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="1b029-125">x</span><span class="sxs-lookup"><span data-stu-id="1b029-125">x</span></span>    | <span data-ttu-id="1b029-126">x</span><span class="sxs-lookup"><span data-stu-id="1b029-126">x</span></span>    | <span data-ttu-id="1b029-127">x</span><span class="sxs-lookup"><span data-stu-id="1b029-127">x</span></span>     | <span data-ttu-id="1b029-128">x</span><span class="sxs-lookup"><span data-stu-id="1b029-128">x</span></span>    | <span data-ttu-id="1b029-129">x</span><span class="sxs-lookup"><span data-stu-id="1b029-129">x</span></span>     |



 

<span data-ttu-id="1b029-130">La máscara XY es necesaria para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="1b029-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="1b029-131">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="1b029-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="1b029-132">Las ecuaciones siguientes muestran cómo funciona la instrucción:</span><span class="sxs-lookup"><span data-stu-id="1b029-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="1b029-133">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="1b029-133">The input vector is in register src0.</span></span> <span data-ttu-id="1b029-134">La matriz de 3x2 de entrada se encuentra en el registro SRC1 y en el siguiente registro superior en el mismo archivo de registro, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="1b029-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="1b029-135">Se genera un resultado 2D, lo que no afecta a los demás elementos del registro de destino (dest. z y dest. w).</span><span class="sxs-lookup"><span data-stu-id="1b029-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="1b029-136">Esta operación se utiliza normalmente para las transformaciones 2D.</span><span class="sxs-lookup"><span data-stu-id="1b029-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="1b029-137">Esta instrucción se implementa como un par de productos DOT como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="1b029-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="1b029-138">Los modificadores swizzle y Negate no son válidos para el registro SRC1.</span><span class="sxs-lookup"><span data-stu-id="1b029-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="1b029-139">El registro de DST y src0, o cualquiera de los registros de SRC1 + i, no puede ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="1b029-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b029-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b029-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b029-141">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1b029-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




