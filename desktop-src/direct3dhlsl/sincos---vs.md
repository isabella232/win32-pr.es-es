---
title: sincos (-vs
description: Calcula el seno y el coseno, en radianes. | sincos (-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003698"
---
# <a name="sincos---vs"></a><span data-ttu-id="3fef6-104">sincos (-vs</span><span class="sxs-lookup"><span data-stu-id="3fef6-104">sincos - vs</span></span>

<span data-ttu-id="3fef6-105">Calcula el seno y el coseno, en radianes.</span><span class="sxs-lookup"><span data-stu-id="3fef6-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fef6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fef6-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="3fef6-107">vs \_ 2 \_ 0 y vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3fef6-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="3fef6-108">sincos (DST. x1</span><span class="sxs-lookup"><span data-stu-id="3fef6-108">sincos dst.{x\</span></span>|<span data-ttu-id="3fef6-109">sí</span><span class="sxs-lookup"><span data-stu-id="3fef6-109">y\</span></span>|<span data-ttu-id="3fef6-110">XY}, src0. x1</span><span class="sxs-lookup"><span data-stu-id="3fef6-110">xy}, src0.{x\</span></span>|<span data-ttu-id="3fef6-111">sí</span><span class="sxs-lookup"><span data-stu-id="3fef6-111">y\</span></span>|<span data-ttu-id="3fef6-112">z</span><span class="sxs-lookup"><span data-stu-id="3fef6-112">z\</span></span>|<span data-ttu-id="3fef6-113">w}, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="3fef6-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="3fef6-114">Donde:</span><span class="sxs-lookup"><span data-stu-id="3fef6-114">Where:</span></span>

-   <span data-ttu-id="3fef6-115">DST es el registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="3fef6-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="3fef6-116">El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="3fef6-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="3fef6-117">src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="3fef6-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="3fef6-118">{x \| y \| z \| w} es el swizzle de replicación necesario.</span><span class="sxs-lookup"><span data-stu-id="3fef6-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="3fef6-119">SRC1 y src2 son registros de origen y deben ser dos [registros Float constantes](dx9-graphics-reference-asm-vs-registers-constant-float.md) diferentes (c \# ).</span><span class="sxs-lookup"><span data-stu-id="3fef6-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="3fef6-120">Los valores de SRC1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3fef6-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="3fef6-121">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3fef6-121">vs\_3\_0</span></span>



| <span data-ttu-id="3fef6-122">sincos (DST. x1</span><span class="sxs-lookup"><span data-stu-id="3fef6-122">sincos dst.{x\</span></span>|<span data-ttu-id="3fef6-123">sí</span><span class="sxs-lookup"><span data-stu-id="3fef6-123">y\</span></span>|<span data-ttu-id="3fef6-124">XY}, src0. x1</span><span class="sxs-lookup"><span data-stu-id="3fef6-124">xy}, src0.{x\</span></span>|<span data-ttu-id="3fef6-125">sí</span><span class="sxs-lookup"><span data-stu-id="3fef6-125">y\</span></span>|<span data-ttu-id="3fef6-126">z</span><span class="sxs-lookup"><span data-stu-id="3fef6-126">z\</span></span>|<span data-ttu-id="3fef6-127">con</span><span class="sxs-lookup"><span data-stu-id="3fef6-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="3fef6-128">Donde:</span><span class="sxs-lookup"><span data-stu-id="3fef6-128">Where:</span></span>

-   <span data-ttu-id="3fef6-129">DST es un registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="3fef6-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="3fef6-130">El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="3fef6-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="3fef6-131">src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="3fef6-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="3fef6-132">{x \| y \| z \| w} es el swizzle de replicación necesario.</span><span class="sxs-lookup"><span data-stu-id="3fef6-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fef6-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fef6-133">Remarks</span></span>



| <span data-ttu-id="3fef6-134">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3fef6-134">Vertex shader versions</span></span> | <span data-ttu-id="3fef6-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="3fef6-135">1\_1</span></span> | <span data-ttu-id="3fef6-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3fef6-136">2\_0</span></span> | <span data-ttu-id="3fef6-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3fef6-137">2\_x</span></span> | <span data-ttu-id="3fef6-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3fef6-138">2\_sw</span></span> | <span data-ttu-id="3fef6-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3fef6-139">3\_0</span></span> | <span data-ttu-id="3fef6-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3fef6-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3fef6-141">sincos (</span><span class="sxs-lookup"><span data-stu-id="3fef6-141">sincos</span></span>                 |      | <span data-ttu-id="3fef6-142">x</span><span class="sxs-lookup"><span data-stu-id="3fef6-142">x</span></span>    | <span data-ttu-id="3fef6-143">x</span><span class="sxs-lookup"><span data-stu-id="3fef6-143">x</span></span>    | <span data-ttu-id="3fef6-144">x</span><span class="sxs-lookup"><span data-stu-id="3fef6-144">x</span></span>     | <span data-ttu-id="3fef6-145">x</span><span class="sxs-lookup"><span data-stu-id="3fef6-145">x</span></span>    | <span data-ttu-id="3fef6-146">x</span><span class="sxs-lookup"><span data-stu-id="3fef6-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="3fef6-147">vs \_ 2 \_ 0 y vs \_ 2 \_ x comentarios</span><span class="sxs-lookup"><span data-stu-id="3fef6-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="3fef6-148">Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, sincos (se puede usar con predication, pero con una restricción a swizzle del registro de [predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0): solo se permite replicar swizzle (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="3fef6-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="3fef6-149">Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, la instrucción funciona de la siguiente manera: (V = el valor escalar de src0 con un swizzle de replicación):</span><span class="sxs-lookup"><span data-stu-id="3fef6-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="3fef6-150">Si la máscara de escritura es. x:</span><span class="sxs-lookup"><span data-stu-id="3fef6-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="3fef6-151">Si la máscara de escritura es. y:</span><span class="sxs-lookup"><span data-stu-id="3fef6-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="3fef6-152">Si la máscara de escritura es. XY:</span><span class="sxs-lookup"><span data-stu-id="3fef6-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="3fef6-153">vs \_ 3 \_ 0 comentarios</span><span class="sxs-lookup"><span data-stu-id="3fef6-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="3fef6-154">Para vs \_ 3 \_ 0, sincos (se puede usar con predication sin ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="3fef6-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="3fef6-155">Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="3fef6-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="3fef6-156">En el caso de vs \_ 3 \_ 0, la instrucción funciona de la siguiente manera: (V = el valor escalar de src0 con un swizzle de replicación)</span><span class="sxs-lookup"><span data-stu-id="3fef6-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="3fef6-157">Si la máscara de escritura es. x:</span><span class="sxs-lookup"><span data-stu-id="3fef6-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="3fef6-158">Si la máscara de escritura es. y:</span><span class="sxs-lookup"><span data-stu-id="3fef6-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="3fef6-159">Si la máscara de escritura es. XY:</span><span class="sxs-lookup"><span data-stu-id="3fef6-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="3fef6-160">La aplicación puede asignar un ángulo arbitrario (en radianes) al intervalo \[ -PI, + PI \] con el siguiente pseudocódigo del sombreador:</span><span class="sxs-lookup"><span data-stu-id="3fef6-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="3fef6-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fef6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fef6-162">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3fef6-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
