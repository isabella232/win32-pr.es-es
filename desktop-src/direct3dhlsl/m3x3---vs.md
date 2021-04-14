---
title: M3x3-vs
description: Multiplica un vector de tres componentes por una matriz de 3x3. | M3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424268"
---
# <a name="m3x3---vs"></a><span data-ttu-id="53c80-104">M3x3-vs</span><span class="sxs-lookup"><span data-stu-id="53c80-104">m3x3 - vs</span></span>

<span data-ttu-id="53c80-105">Multiplica un vector de tres componentes por una matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="53c80-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c80-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53c80-106">Syntax</span></span>



| <span data-ttu-id="53c80-107">M3x3 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="53c80-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="53c80-108">, donde</span><span class="sxs-lookup"><span data-stu-id="53c80-108">where</span></span>

-   <span data-ttu-id="53c80-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="53c80-109">dst is the destination register.</span></span> <span data-ttu-id="53c80-110">El resultado es un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="53c80-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="53c80-111">src0 es un registro de origen que representa un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="53c80-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="53c80-112">SRC1 es un registro de origen que representa una matriz de 3x3, que corresponde al primer de 3 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="53c80-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c80-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53c80-113">Remarks</span></span>



| <span data-ttu-id="53c80-114">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="53c80-114">Vertex shader versions</span></span> | <span data-ttu-id="53c80-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="53c80-115">1\_1</span></span> | <span data-ttu-id="53c80-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53c80-116">2\_0</span></span> | <span data-ttu-id="53c80-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53c80-117">2\_x</span></span> | <span data-ttu-id="53c80-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53c80-118">2\_sw</span></span> | <span data-ttu-id="53c80-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53c80-119">3\_0</span></span> | <span data-ttu-id="53c80-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53c80-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="53c80-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="53c80-121">m3x3</span></span>                   | <span data-ttu-id="53c80-122">x</span><span class="sxs-lookup"><span data-stu-id="53c80-122">x</span></span>    | <span data-ttu-id="53c80-123">x</span><span class="sxs-lookup"><span data-stu-id="53c80-123">x</span></span>    | <span data-ttu-id="53c80-124">x</span><span class="sxs-lookup"><span data-stu-id="53c80-124">x</span></span>    | <span data-ttu-id="53c80-125">x</span><span class="sxs-lookup"><span data-stu-id="53c80-125">x</span></span>     | <span data-ttu-id="53c80-126">x</span><span class="sxs-lookup"><span data-stu-id="53c80-126">x</span></span>    | <span data-ttu-id="53c80-127">x</span><span class="sxs-lookup"><span data-stu-id="53c80-127">x</span></span>     |



 

<span data-ttu-id="53c80-128">La máscara XYZ es necesaria para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="53c80-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="53c80-129">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="53c80-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="53c80-130">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="53c80-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="53c80-131">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="53c80-131">The input vector is in register src0.</span></span> <span data-ttu-id="53c80-132">La matriz de 3x3 de entrada está en el registro SRC1 y los dos registros más altos siguientes, como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="53c80-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="53c80-133">Se genera un resultado 3D, lo que no afecta al otro elemento del registro de destino (dest. w).</span><span class="sxs-lookup"><span data-stu-id="53c80-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="53c80-134">Esta operación se utiliza normalmente para transformar vectores normales durante los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="53c80-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="53c80-135">Esta instrucción se implementa como un par de productos DOT como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="53c80-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="53c80-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53c80-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c80-137">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="53c80-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




