---
title: sincos (-PS
description: Calcula el seno y el coseno, en radianes. | sincos (-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998137"
---
# <a name="sincos---ps"></a><span data-ttu-id="058e0-104">sincos (-PS</span><span class="sxs-lookup"><span data-stu-id="058e0-104">sincos - ps</span></span>

<span data-ttu-id="058e0-105">Calcula el seno y el coseno, en radianes.</span><span class="sxs-lookup"><span data-stu-id="058e0-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="058e0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="058e0-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="058e0-107">PS \_ 2 \_ 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="058e0-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="058e0-108">sincos (DST. x1</span><span class="sxs-lookup"><span data-stu-id="058e0-108">sincos dst.{x\</span></span>|<span data-ttu-id="058e0-109">sí</span><span class="sxs-lookup"><span data-stu-id="058e0-109">y\</span></span>|<span data-ttu-id="058e0-110">XY}, src0. x1</span><span class="sxs-lookup"><span data-stu-id="058e0-110">xy}, src0.{x\</span></span>|<span data-ttu-id="058e0-111">sí</span><span class="sxs-lookup"><span data-stu-id="058e0-111">y\</span></span>|<span data-ttu-id="058e0-112">z</span><span class="sxs-lookup"><span data-stu-id="058e0-112">z\</span></span>|<span data-ttu-id="058e0-113">w}, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="058e0-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="058e0-114">Donde:</span><span class="sxs-lookup"><span data-stu-id="058e0-114">Where:</span></span>

-   <span data-ttu-id="058e0-115">DST es el registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="058e0-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="058e0-116">El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="058e0-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="058e0-117">src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="058e0-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="058e0-118">{x \| y \| z \| w} es el swizzle de replicación necesario.</span><span class="sxs-lookup"><span data-stu-id="058e0-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="058e0-119">SRC1 y src2 son registros de origen y deben ser dos [registros Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)diferentes (c \# ).</span><span class="sxs-lookup"><span data-stu-id="058e0-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="058e0-120">Los valores de SRC1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="058e0-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="058e0-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="058e0-121">ps\_3\_0</span></span>



| <span data-ttu-id="058e0-122">sincos (DST. x1</span><span class="sxs-lookup"><span data-stu-id="058e0-122">sincos dst.{x\</span></span>|<span data-ttu-id="058e0-123">sí</span><span class="sxs-lookup"><span data-stu-id="058e0-123">y\</span></span>|<span data-ttu-id="058e0-124">XY}, src0. x1</span><span class="sxs-lookup"><span data-stu-id="058e0-124">xy}, src0.{x\</span></span>|<span data-ttu-id="058e0-125">sí</span><span class="sxs-lookup"><span data-stu-id="058e0-125">y\</span></span>|<span data-ttu-id="058e0-126">z</span><span class="sxs-lookup"><span data-stu-id="058e0-126">z\</span></span>|<span data-ttu-id="058e0-127">con</span><span class="sxs-lookup"><span data-stu-id="058e0-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="058e0-128">Donde:</span><span class="sxs-lookup"><span data-stu-id="058e0-128">Where:</span></span>

-   <span data-ttu-id="058e0-129">DST es un registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="058e0-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="058e0-130">El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="058e0-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="058e0-131">src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="058e0-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="058e0-132">{x \| y \| z \| w} es el swizzle de replicación necesario.</span><span class="sxs-lookup"><span data-stu-id="058e0-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="058e0-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="058e0-133">Remarks</span></span>



| <span data-ttu-id="058e0-134">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="058e0-134">Pixel shader versions</span></span> | <span data-ttu-id="058e0-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="058e0-135">1\_1</span></span> | <span data-ttu-id="058e0-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="058e0-136">1\_2</span></span> | <span data-ttu-id="058e0-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="058e0-137">1\_3</span></span> | <span data-ttu-id="058e0-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="058e0-138">1\_4</span></span> | <span data-ttu-id="058e0-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="058e0-139">2\_0</span></span> | <span data-ttu-id="058e0-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="058e0-140">2\_x</span></span> | <span data-ttu-id="058e0-141">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="058e0-141">2\_sw</span></span> | <span data-ttu-id="058e0-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="058e0-142">3\_0</span></span> | <span data-ttu-id="058e0-143">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="058e0-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="058e0-144">sincos (</span><span class="sxs-lookup"><span data-stu-id="058e0-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="058e0-145">x</span><span class="sxs-lookup"><span data-stu-id="058e0-145">x</span></span>    | <span data-ttu-id="058e0-146">x</span><span class="sxs-lookup"><span data-stu-id="058e0-146">x</span></span>    | <span data-ttu-id="058e0-147">x</span><span class="sxs-lookup"><span data-stu-id="058e0-147">x</span></span>     | <span data-ttu-id="058e0-148">x</span><span class="sxs-lookup"><span data-stu-id="058e0-148">x</span></span>    | <span data-ttu-id="058e0-149">x</span><span class="sxs-lookup"><span data-stu-id="058e0-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="058e0-150">PS \_ 2 \_ 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="058e0-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="058e0-151">Para PS \_ 2 \_ 0 y PS \_ 2 \_ x, sincos (se puede usar con predication, pero con una restricción a swizzle del registro de [predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0): solo se permite replicar swizzle (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="058e0-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="058e0-152">Para PS \_ 2 \_ 0 y PS \_ 2 \_ x, la instrucción funciona de la siguiente manera (V = el valor escalar de src0 con un swizzle de replicación):</span><span class="sxs-lookup"><span data-stu-id="058e0-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="058e0-153">Si la máscara de escritura es. x:</span><span class="sxs-lookup"><span data-stu-id="058e0-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="058e0-154">Si la máscara de escritura es. y:</span><span class="sxs-lookup"><span data-stu-id="058e0-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="058e0-155">Si la máscara de escritura es. XY:</span><span class="sxs-lookup"><span data-stu-id="058e0-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="058e0-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="058e0-156">ps\_3\_0</span></span>

<span data-ttu-id="058e0-157">Para PS \_ 3 \_ 0, sincos (se puede usar con predication sin ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="058e0-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="058e0-158">Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="058e0-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="058e0-159">Para PS \_ 3 \_ 0, la instrucción funciona de la siguiente manera (V = el valor escalar de src0 con un swizzle de replicación):</span><span class="sxs-lookup"><span data-stu-id="058e0-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="058e0-160">Si la máscara de escritura es. x:</span><span class="sxs-lookup"><span data-stu-id="058e0-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="058e0-161">Si la máscara de escritura es. y:</span><span class="sxs-lookup"><span data-stu-id="058e0-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="058e0-162">Si la máscara de escritura es. XY:</span><span class="sxs-lookup"><span data-stu-id="058e0-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="058e0-163">La aplicación puede asignar un ángulo arbitrario (en radianes) al intervalo \[ -PI, + PI \] con el siguiente pseudocódigo del sombreador:</span><span class="sxs-lookup"><span data-stu-id="058e0-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="058e0-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="058e0-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="058e0-165">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="058e0-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
