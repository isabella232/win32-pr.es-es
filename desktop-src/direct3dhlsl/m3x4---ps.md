---
title: M3x4-PS
description: Multiplica un vector de tres componentes por una matriz de 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986639"
---
# <a name="m3x4---ps"></a><span data-ttu-id="bf6d0-104">M3x4-PS</span><span class="sxs-lookup"><span data-stu-id="bf6d0-104">m3x4 - ps</span></span>

<span data-ttu-id="bf6d0-105">Multiplica un vector de tres componentes por una matriz de 3x4.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6d0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf6d0-106">Syntax</span></span>



| <span data-ttu-id="bf6d0-107">M3x4 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="bf6d0-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="bf6d0-108">, donde</span><span class="sxs-lookup"><span data-stu-id="bf6d0-108">where</span></span>

-   <span data-ttu-id="bf6d0-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-109">dst is the destination register.</span></span> <span data-ttu-id="bf6d0-110">El resultado es un vector de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="bf6d0-111">src0 es un registro de origen que representa un vector de tres componentes.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="bf6d0-112">SRC1 es un registro de origen que representa una matriz de 3x4, que se corresponde con el primero de 4 registros consecutivos.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf6d0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf6d0-113">Remarks</span></span>



| <span data-ttu-id="bf6d0-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="bf6d0-114">Pixel shader versions</span></span> | <span data-ttu-id="bf6d0-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="bf6d0-115">1\_1</span></span> | <span data-ttu-id="bf6d0-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="bf6d0-116">1\_2</span></span> | <span data-ttu-id="bf6d0-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bf6d0-117">1\_3</span></span> | <span data-ttu-id="bf6d0-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="bf6d0-118">1\_4</span></span> | <span data-ttu-id="bf6d0-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf6d0-119">2\_0</span></span> | <span data-ttu-id="bf6d0-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-120">2\_x</span></span> | <span data-ttu-id="bf6d0-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf6d0-121">2\_sw</span></span> | <span data-ttu-id="bf6d0-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf6d0-122">3\_0</span></span> | <span data-ttu-id="bf6d0-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf6d0-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bf6d0-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="bf6d0-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="bf6d0-125">x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-125">x</span></span>    | <span data-ttu-id="bf6d0-126">x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-126">x</span></span>    | <span data-ttu-id="bf6d0-127">x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-127">x</span></span>     | <span data-ttu-id="bf6d0-128">x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-128">x</span></span>    | <span data-ttu-id="bf6d0-129">x</span><span class="sxs-lookup"><span data-stu-id="bf6d0-129">x</span></span>     |



 

<span data-ttu-id="bf6d0-130">Se necesita la máscara xyzw (valor predeterminado) para el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="bf6d0-131">Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="bf6d0-132">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="bf6d0-133">El vector de entrada se encuentra en el registro src0.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-133">The input vector is in register src0.</span></span> <span data-ttu-id="bf6d0-134">La matriz de 3x4 de entrada se encuentra en el registro SRC1 y en los dos registros posteriores siguientes, tal como se muestra en la siguiente expansión.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="bf6d0-135">Esta operación se utiliza normalmente para transformar un vector de posición por una matriz que tiene un efecto proyectado pero no aplica ninguna traducción.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="bf6d0-136">Esta instrucción se implementa como un par de productos DOT como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="bf6d0-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="bf6d0-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf6d0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf6d0-138">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="bf6d0-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




