---
title: M4x4-PS
description: Multiplica un vector de cuatro componentes por una matriz de 4x4. | M4x4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f2da73c45151f5287f3acf773efb4bd57d21e1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986423"
---
# <a name="m4x4---ps"></a><span data-ttu-id="3159c-104">M4x4-PS</span><span class="sxs-lookup"><span data-stu-id="3159c-104">m4x4 - ps</span></span>

<span data-ttu-id="3159c-105">Multiplica un vector de cuatro componentes por una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="3159c-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3159c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3159c-106">Syntax</span></span>



| <span data-ttu-id="3159c-107">M4x4 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="3159c-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="3159c-108">, donde</span><span class="sxs-lookup"><span data-stu-id="3159c-108">where</span></span>

-   <span data-ttu-id="3159c-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3159c-109">dst is the destination register.</span></span> <span data-ttu-id="3159c-110">El resultado es un vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="3159c-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="3159c-111">src0 es un registro de origen que representa un vector de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="3159c-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="3159c-112">SRC1 es un registro de origen que representa una matriz de 4x4, que corresponde al primer de 4 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="3159c-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="3159c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3159c-113">Remarks</span></span>



| <span data-ttu-id="3159c-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3159c-114">Pixel shader versions</span></span> | <span data-ttu-id="3159c-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="3159c-115">1\_1</span></span> | <span data-ttu-id="3159c-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="3159c-116">1\_2</span></span> | <span data-ttu-id="3159c-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3159c-117">1\_3</span></span> | <span data-ttu-id="3159c-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="3159c-118">1\_4</span></span> | <span data-ttu-id="3159c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3159c-119">2\_0</span></span> | <span data-ttu-id="3159c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3159c-120">2\_x</span></span> | <span data-ttu-id="3159c-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3159c-121">2\_sw</span></span> | <span data-ttu-id="3159c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3159c-122">3\_0</span></span> | <span data-ttu-id="3159c-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3159c-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3159c-124">m4x4</span><span class="sxs-lookup"><span data-stu-id="3159c-124">m4x4</span></span>                  |      |      |      |      | <span data-ttu-id="3159c-125">x</span><span class="sxs-lookup"><span data-stu-id="3159c-125">x</span></span>    | <span data-ttu-id="3159c-126">x</span><span class="sxs-lookup"><span data-stu-id="3159c-126">x</span></span>    | <span data-ttu-id="3159c-127">x</span><span class="sxs-lookup"><span data-stu-id="3159c-127">x</span></span>     | <span data-ttu-id="3159c-128">x</span><span class="sxs-lookup"><span data-stu-id="3159c-128">x</span></span>    | <span data-ttu-id="3159c-129">x</span><span class="sxs-lookup"><span data-stu-id="3159c-129">x</span></span>     |



 

<span data-ttu-id="3159c-130">Se necesita la máscara xyzw (valor predeterminado) para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3159c-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="3159c-131">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="3159c-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="3159c-132">Los modificadores swizzle y Negate no son válidos para el registro src0.</span><span class="sxs-lookup"><span data-stu-id="3159c-132">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="3159c-133">Los registros de DST y src0 no pueden ser los mismos.</span><span class="sxs-lookup"><span data-stu-id="3159c-133">The dst and src0 registers cannot be the same.</span></span>

<span data-ttu-id="3159c-134">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="3159c-134">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



<span data-ttu-id="3159c-135">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="3159c-135">The input vector is in register src0.</span></span> <span data-ttu-id="3159c-136">La matriz 4x4 de entrada está en el registro SRC1 y los tres registros superiores siguientes, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="3159c-136">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="3159c-137">Esta operación se utiliza normalmente para transformar una posición por una matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="3159c-137">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="3159c-138">Esta instrucción se implementa como un conjunto de productos de puntos, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3159c-138">This instruction is implemented as a set of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="3159c-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3159c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3159c-140">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3159c-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




