---
title: m4x3-vs
description: Multiplica un vector de cuatro componentes por una matriz de 4x3. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986311"
---
# <a name="m4x3---vs"></a><span data-ttu-id="91dca-104">m4x3-vs</span><span class="sxs-lookup"><span data-stu-id="91dca-104">m4x3 - vs</span></span>

<span data-ttu-id="91dca-105">Multiplica un vector de cuatro componentes por una matriz de 4x3.</span><span class="sxs-lookup"><span data-stu-id="91dca-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="91dca-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91dca-106">Syntax</span></span>



| <span data-ttu-id="91dca-107">m4x3 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="91dca-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="91dca-108">, donde</span><span class="sxs-lookup"><span data-stu-id="91dca-108">where</span></span>

-   <span data-ttu-id="91dca-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="91dca-109">dst is the destination register.</span></span> <span data-ttu-id="91dca-110">El resultado es un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="91dca-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="91dca-111">src0 es un registro de origen que representa un vector de 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="91dca-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="91dca-112">SRC1 es un registro de origen que representa una matriz de 4x3, que corresponde al primer de 3 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="91dca-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="91dca-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91dca-113">Remarks</span></span>



| <span data-ttu-id="91dca-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="91dca-114">Vertex shader versions</span></span> | <span data-ttu-id="91dca-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="91dca-115">1\_1</span></span> | <span data-ttu-id="91dca-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91dca-116">2\_0</span></span> | <span data-ttu-id="91dca-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91dca-117">2\_x</span></span> | <span data-ttu-id="91dca-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91dca-118">2\_sw</span></span> | <span data-ttu-id="91dca-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91dca-119">3\_0</span></span> | <span data-ttu-id="91dca-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91dca-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="91dca-121">m4x3</span><span class="sxs-lookup"><span data-stu-id="91dca-121">m4x3</span></span>                   | <span data-ttu-id="91dca-122">x</span><span class="sxs-lookup"><span data-stu-id="91dca-122">x</span></span>    | <span data-ttu-id="91dca-123">x</span><span class="sxs-lookup"><span data-stu-id="91dca-123">x</span></span>    | <span data-ttu-id="91dca-124">x</span><span class="sxs-lookup"><span data-stu-id="91dca-124">x</span></span>    | <span data-ttu-id="91dca-125">x</span><span class="sxs-lookup"><span data-stu-id="91dca-125">x</span></span>     | <span data-ttu-id="91dca-126">x</span><span class="sxs-lookup"><span data-stu-id="91dca-126">x</span></span>    | <span data-ttu-id="91dca-127">x</span><span class="sxs-lookup"><span data-stu-id="91dca-127">x</span></span>     |



 

<span data-ttu-id="91dca-128">La máscara XYZ es necesaria para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="91dca-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="91dca-129">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="91dca-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="91dca-130">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="91dca-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



<span data-ttu-id="91dca-131">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="91dca-131">The input vector is in register src0.</span></span> <span data-ttu-id="91dca-132">La matriz de 4x3 de entrada se encuentra en el registro SRC1 y en los dos registros posteriores siguientes, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="91dca-132">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="91dca-133">Se genera un resultado 3D, lo que no afecta al otro elemento del registro de destino (dest. w).</span><span class="sxs-lookup"><span data-stu-id="91dca-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="91dca-134">Esta operación se utiliza normalmente para transformar un vector de posición por una matriz que no tiene ningún efecto proyectado, como ocurre en las transformaciones de espacio de modelo.</span><span class="sxs-lookup"><span data-stu-id="91dca-134">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="91dca-135">Esta instrucción se implementa como un par de productos DOT como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="91dca-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="91dca-136">Los modificadores swizzle y Negate no son válidos para el registro SRC1.</span><span class="sxs-lookup"><span data-stu-id="91dca-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="91dca-137">El registro de DST y src0 no puede ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="91dca-137">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91dca-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91dca-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91dca-139">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="91dca-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




