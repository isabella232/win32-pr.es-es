---
title: M4x4-vs
description: Multiplica un vector de cuatro componentes por una matriz de 4x4. | M4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279996"
---
# <a name="m4x4---vs"></a><span data-ttu-id="8aa0d-104">M4x4-vs</span><span class="sxs-lookup"><span data-stu-id="8aa0d-104">m4x4 - vs</span></span>

<span data-ttu-id="8aa0d-105">Multiplica un vector de cuatro componentes por una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aa0d-106">Syntax</span></span>



| <span data-ttu-id="8aa0d-107">M4x4 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="8aa0d-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="8aa0d-108">, donde</span><span class="sxs-lookup"><span data-stu-id="8aa0d-108">where</span></span>

-   <span data-ttu-id="8aa0d-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-109">dst is the destination register.</span></span> <span data-ttu-id="8aa0d-110">El resultado es un vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="8aa0d-111">src0 es un registro de origen que representa un vector de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="8aa0d-112">SRC1 es un registro de origen que representa una matriz de 4x4, que corresponde al primer de 4 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa0d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aa0d-113">Remarks</span></span>



| <span data-ttu-id="8aa0d-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8aa0d-114">Vertex shader versions</span></span> | <span data-ttu-id="8aa0d-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="8aa0d-115">1\_1</span></span> | <span data-ttu-id="8aa0d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aa0d-116">2\_0</span></span> | <span data-ttu-id="8aa0d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-117">2\_x</span></span> | <span data-ttu-id="8aa0d-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8aa0d-118">2\_sw</span></span> | <span data-ttu-id="8aa0d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8aa0d-119">3\_0</span></span> | <span data-ttu-id="8aa0d-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8aa0d-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8aa0d-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="8aa0d-121">m4x4</span></span>                   | <span data-ttu-id="8aa0d-122">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-122">x</span></span>    | <span data-ttu-id="8aa0d-123">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-123">x</span></span>    | <span data-ttu-id="8aa0d-124">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-124">x</span></span>    | <span data-ttu-id="8aa0d-125">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-125">x</span></span>     | <span data-ttu-id="8aa0d-126">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-126">x</span></span>    | <span data-ttu-id="8aa0d-127">x</span><span class="sxs-lookup"><span data-stu-id="8aa0d-127">x</span></span>     |



 

<span data-ttu-id="8aa0d-128">Se necesita la máscara xyzw (valor predeterminado) para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="8aa0d-129">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="8aa0d-130">Los modificadores swizzle y Negate no son válidos para el registro src0.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="8aa0d-131">Los registros dest y src0 no pueden ser iguales.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="8aa0d-132">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="8aa0d-133">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-133">The input vector is in register src0.</span></span> <span data-ttu-id="8aa0d-134">La matriz 4x4 de entrada está en el registro SRC1 y los tres registros superiores siguientes, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="8aa0d-135">Esta operación se utiliza normalmente para transformar una posición por una matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="8aa0d-136">Esta instrucción se implementa como una serie de productos de puntos, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="8aa0d-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="8aa0d-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8aa0d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa0d-138">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8aa0d-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




