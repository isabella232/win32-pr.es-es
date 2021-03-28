---
title: m3x2-vs
description: Multiplica un vector de tres componentes por una matriz de 3x2. | m3x2-vs
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279999"
---
# <a name="m3x2---vs"></a><span data-ttu-id="a2a6b-104">m3x2-vs</span><span class="sxs-lookup"><span data-stu-id="a2a6b-104">m3x2 - vs</span></span>

<span data-ttu-id="a2a6b-105">Multiplica un vector de tres componentes por una matriz de 3x2.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a6b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2a6b-106">Syntax</span></span>



| <span data-ttu-id="a2a6b-107">m3x2 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="a2a6b-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="a2a6b-108">, donde</span><span class="sxs-lookup"><span data-stu-id="a2a6b-108">where</span></span>

-   <span data-ttu-id="a2a6b-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-109">dst is the destination register.</span></span> <span data-ttu-id="a2a6b-110">El resultado es un vector de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="a2a6b-111">src0 es un registro de origen que representa un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="a2a6b-112">SRC1 es un registro de origen que representa una matriz de 3x2, que corresponde al primer de 2 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a6b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2a6b-113">Remarks</span></span>



| <span data-ttu-id="a2a6b-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a2a6b-114">Vertex shader versions</span></span> | <span data-ttu-id="a2a6b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="a2a6b-115">1\_1</span></span> | <span data-ttu-id="a2a6b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2a6b-116">2\_0</span></span> | <span data-ttu-id="a2a6b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-117">2\_x</span></span> | <span data-ttu-id="a2a6b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2a6b-118">2\_sw</span></span> | <span data-ttu-id="a2a6b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2a6b-119">3\_0</span></span> | <span data-ttu-id="a2a6b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2a6b-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a2a6b-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="a2a6b-121">m3x2</span></span>                   | <span data-ttu-id="a2a6b-122">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-122">x</span></span>    | <span data-ttu-id="a2a6b-123">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-123">x</span></span>    | <span data-ttu-id="a2a6b-124">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-124">x</span></span>    | <span data-ttu-id="a2a6b-125">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-125">x</span></span>     | <span data-ttu-id="a2a6b-126">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-126">x</span></span>    | <span data-ttu-id="a2a6b-127">x</span><span class="sxs-lookup"><span data-stu-id="a2a6b-127">x</span></span>     |



 

<span data-ttu-id="a2a6b-128">La máscara XY es necesaria para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="a2a6b-129">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="a2a6b-130">Las ecuaciones siguientes muestran cómo funciona la instrucción:</span><span class="sxs-lookup"><span data-stu-id="a2a6b-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="a2a6b-131">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-131">The input vector is in register src0.</span></span> <span data-ttu-id="a2a6b-132">La matriz de 3x2 de entrada se encuentra en el registro SRC1 y en el siguiente registro superior en el mismo archivo de registro, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="a2a6b-133">Se genera un resultado 2D, lo que no afecta a los demás elementos del registro de destino (dest. z y dest. w).</span><span class="sxs-lookup"><span data-stu-id="a2a6b-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="a2a6b-134">Esta operación se utiliza normalmente para las transformaciones 2D.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="a2a6b-135">Esta instrucción se implementa como un par de productos DOT como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="a2a6b-136">Los modificadores swizzle y Negate no son válidos para el registro SRC1.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="a2a6b-137">Los registros dest y src0, o cualquiera de los registros SRC1 + i, no pueden ser iguales.</span><span class="sxs-lookup"><span data-stu-id="a2a6b-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2a6b-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2a6b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a6b-139">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a2a6b-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




