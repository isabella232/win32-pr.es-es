---
title: Registro de origen permutación (referencia de PS de HLSL)
description: Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen. Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358524"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="5882e-105">Registro de origen permutación (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="5882e-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="5882e-106">Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal.</span><span class="sxs-lookup"><span data-stu-id="5882e-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="5882e-107">Permutación no afecta a los datos de registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5882e-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="5882e-108">Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="5882e-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="5882e-109">Permutación de origen</span><span class="sxs-lookup"><span data-stu-id="5882e-109">Source Swizzling</span></span>

<span data-ttu-id="5882e-110">El swizzle de origen permite que un componente individual de un registro de origen asuma el valor de cualquiera de los cuatro componentes del mismo registro de origen antes de que se lea el registro para el cálculo.</span><span class="sxs-lookup"><span data-stu-id="5882e-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="5882e-111">Por ejemplo,. zxxy swizzle significa:</span><span class="sxs-lookup"><span data-stu-id="5882e-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="5882e-112">el componente. x tomará el valor del componente. z</span><span class="sxs-lookup"><span data-stu-id="5882e-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="5882e-113">el componente. y tomará el valor del componente. x</span><span class="sxs-lookup"><span data-stu-id="5882e-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="5882e-114">el componente. z tomará el valor del componente. x</span><span class="sxs-lookup"><span data-stu-id="5882e-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="5882e-115">el componente. w tomará el valor del componente. y</span><span class="sxs-lookup"><span data-stu-id="5882e-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="5882e-116">Los componentes pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="5882e-116">The components can appear in any order.</span></span> <span data-ttu-id="5882e-117">Si se especifican menos de cuatro componentes, se repite el último componente.</span><span class="sxs-lookup"><span data-stu-id="5882e-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="5882e-118">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5882e-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="5882e-119">Si no se especifica ningún componente, no se aplica ningún permutación.</span><span class="sxs-lookup"><span data-stu-id="5882e-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="5882e-120">Algunas instrucciones tienen restricciones de swizzle de código fuente.</span><span class="sxs-lookup"><span data-stu-id="5882e-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="5882e-121">Aparecen en las páginas de referencia de instrucciones respetadas.</span><span class="sxs-lookup"><span data-stu-id="5882e-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="5882e-122">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5882e-122">Pixel shader versions</span></span> | <span data-ttu-id="5882e-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="5882e-123">1\_1</span></span> | <span data-ttu-id="5882e-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="5882e-124">1\_2</span></span> | <span data-ttu-id="5882e-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5882e-125">1\_3</span></span> | <span data-ttu-id="5882e-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="5882e-126">1\_4</span></span> | <span data-ttu-id="5882e-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5882e-127">2\_0</span></span> | <span data-ttu-id="5882e-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5882e-128">2\_x</span></span> | <span data-ttu-id="5882e-129">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5882e-129">2\_sw</span></span> | <span data-ttu-id="5882e-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5882e-130">3\_0</span></span> | <span data-ttu-id="5882e-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5882e-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5882e-132">.x</span><span class="sxs-lookup"><span data-stu-id="5882e-132">.x</span></span>                    |      |      |      | <span data-ttu-id="5882e-133">x</span><span class="sxs-lookup"><span data-stu-id="5882e-133">x</span></span>    | <span data-ttu-id="5882e-134">x</span><span class="sxs-lookup"><span data-stu-id="5882e-134">x</span></span>    | <span data-ttu-id="5882e-135">x</span><span class="sxs-lookup"><span data-stu-id="5882e-135">x</span></span>    | <span data-ttu-id="5882e-136">x</span><span class="sxs-lookup"><span data-stu-id="5882e-136">x</span></span>     | <span data-ttu-id="5882e-137">x</span><span class="sxs-lookup"><span data-stu-id="5882e-137">x</span></span>    | <span data-ttu-id="5882e-138">x</span><span class="sxs-lookup"><span data-stu-id="5882e-138">x</span></span>     |
| <span data-ttu-id="5882e-139">. y</span><span class="sxs-lookup"><span data-stu-id="5882e-139">.y</span></span>                    |      |      |      | <span data-ttu-id="5882e-140">x</span><span class="sxs-lookup"><span data-stu-id="5882e-140">x</span></span>    | <span data-ttu-id="5882e-141">x</span><span class="sxs-lookup"><span data-stu-id="5882e-141">x</span></span>    | <span data-ttu-id="5882e-142">x</span><span class="sxs-lookup"><span data-stu-id="5882e-142">x</span></span>    | <span data-ttu-id="5882e-143">x</span><span class="sxs-lookup"><span data-stu-id="5882e-143">x</span></span>     | <span data-ttu-id="5882e-144">x</span><span class="sxs-lookup"><span data-stu-id="5882e-144">x</span></span>    | <span data-ttu-id="5882e-145">x</span><span class="sxs-lookup"><span data-stu-id="5882e-145">x</span></span>     |
| <span data-ttu-id="5882e-146">. z</span><span class="sxs-lookup"><span data-stu-id="5882e-146">.z</span></span>                    | <span data-ttu-id="5882e-147">x1\*</span><span class="sxs-lookup"><span data-stu-id="5882e-147">x\*</span></span>  | <span data-ttu-id="5882e-148">x1\*</span><span class="sxs-lookup"><span data-stu-id="5882e-148">x\*</span></span>  | <span data-ttu-id="5882e-149">x1\*</span><span class="sxs-lookup"><span data-stu-id="5882e-149">x\*</span></span>  | <span data-ttu-id="5882e-150">x</span><span class="sxs-lookup"><span data-stu-id="5882e-150">x</span></span>    | <span data-ttu-id="5882e-151">x</span><span class="sxs-lookup"><span data-stu-id="5882e-151">x</span></span>    | <span data-ttu-id="5882e-152">x</span><span class="sxs-lookup"><span data-stu-id="5882e-152">x</span></span>    | <span data-ttu-id="5882e-153">x</span><span class="sxs-lookup"><span data-stu-id="5882e-153">x</span></span>     | <span data-ttu-id="5882e-154">x</span><span class="sxs-lookup"><span data-stu-id="5882e-154">x</span></span>    | <span data-ttu-id="5882e-155">x</span><span class="sxs-lookup"><span data-stu-id="5882e-155">x</span></span>     |
| <span data-ttu-id="5882e-156">. w</span><span class="sxs-lookup"><span data-stu-id="5882e-156">.w</span></span>                    | <span data-ttu-id="5882e-157">x</span><span class="sxs-lookup"><span data-stu-id="5882e-157">x</span></span>    | <span data-ttu-id="5882e-158">x</span><span class="sxs-lookup"><span data-stu-id="5882e-158">x</span></span>    | <span data-ttu-id="5882e-159">x</span><span class="sxs-lookup"><span data-stu-id="5882e-159">x</span></span>    | <span data-ttu-id="5882e-160">x</span><span class="sxs-lookup"><span data-stu-id="5882e-160">x</span></span>    | <span data-ttu-id="5882e-161">x</span><span class="sxs-lookup"><span data-stu-id="5882e-161">x</span></span>    | <span data-ttu-id="5882e-162">x</span><span class="sxs-lookup"><span data-stu-id="5882e-162">x</span></span>    | <span data-ttu-id="5882e-163">x</span><span class="sxs-lookup"><span data-stu-id="5882e-163">x</span></span>     | <span data-ttu-id="5882e-164">x</span><span class="sxs-lookup"><span data-stu-id="5882e-164">x</span></span>    | <span data-ttu-id="5882e-165">x</span><span class="sxs-lookup"><span data-stu-id="5882e-165">x</span></span>     |
| <span data-ttu-id="5882e-166">. xyzw (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="5882e-166">.xyzw (default)</span></span>       | <span data-ttu-id="5882e-167">x</span><span class="sxs-lookup"><span data-stu-id="5882e-167">x</span></span>    | <span data-ttu-id="5882e-168">x</span><span class="sxs-lookup"><span data-stu-id="5882e-168">x</span></span>    | <span data-ttu-id="5882e-169">x</span><span class="sxs-lookup"><span data-stu-id="5882e-169">x</span></span>    | <span data-ttu-id="5882e-170">x</span><span class="sxs-lookup"><span data-stu-id="5882e-170">x</span></span>    | <span data-ttu-id="5882e-171">x</span><span class="sxs-lookup"><span data-stu-id="5882e-171">x</span></span>    | <span data-ttu-id="5882e-172">x</span><span class="sxs-lookup"><span data-stu-id="5882e-172">x</span></span>    | <span data-ttu-id="5882e-173">x</span><span class="sxs-lookup"><span data-stu-id="5882e-173">x</span></span>     | <span data-ttu-id="5882e-174">x</span><span class="sxs-lookup"><span data-stu-id="5882e-174">x</span></span>    | <span data-ttu-id="5882e-175">x</span><span class="sxs-lookup"><span data-stu-id="5882e-175">x</span></span>     |
| <span data-ttu-id="5882e-176">. yzxw</span><span class="sxs-lookup"><span data-stu-id="5882e-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="5882e-177">x</span><span class="sxs-lookup"><span data-stu-id="5882e-177">x</span></span>    | <span data-ttu-id="5882e-178">x</span><span class="sxs-lookup"><span data-stu-id="5882e-178">x</span></span>    | <span data-ttu-id="5882e-179">x</span><span class="sxs-lookup"><span data-stu-id="5882e-179">x</span></span>     | <span data-ttu-id="5882e-180">x</span><span class="sxs-lookup"><span data-stu-id="5882e-180">x</span></span>    | <span data-ttu-id="5882e-181">x</span><span class="sxs-lookup"><span data-stu-id="5882e-181">x</span></span>     |
| <span data-ttu-id="5882e-182">. zxyw</span><span class="sxs-lookup"><span data-stu-id="5882e-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="5882e-183">x</span><span class="sxs-lookup"><span data-stu-id="5882e-183">x</span></span>    | <span data-ttu-id="5882e-184">x</span><span class="sxs-lookup"><span data-stu-id="5882e-184">x</span></span>    | <span data-ttu-id="5882e-185">x</span><span class="sxs-lookup"><span data-stu-id="5882e-185">x</span></span>     | <span data-ttu-id="5882e-186">x</span><span class="sxs-lookup"><span data-stu-id="5882e-186">x</span></span>    | <span data-ttu-id="5882e-187">x</span><span class="sxs-lookup"><span data-stu-id="5882e-187">x</span></span>     |
| <span data-ttu-id="5882e-188">. wzyx</span><span class="sxs-lookup"><span data-stu-id="5882e-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="5882e-189">x</span><span class="sxs-lookup"><span data-stu-id="5882e-189">x</span></span>    | <span data-ttu-id="5882e-190">x</span><span class="sxs-lookup"><span data-stu-id="5882e-190">x</span></span>    | <span data-ttu-id="5882e-191">x</span><span class="sxs-lookup"><span data-stu-id="5882e-191">x</span></span>     | <span data-ttu-id="5882e-192">x</span><span class="sxs-lookup"><span data-stu-id="5882e-192">x</span></span>    | <span data-ttu-id="5882e-193">x</span><span class="sxs-lookup"><span data-stu-id="5882e-193">x</span></span>     |
| <span data-ttu-id="5882e-194">swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="5882e-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="5882e-195">x</span><span class="sxs-lookup"><span data-stu-id="5882e-195">x</span></span>    | <span data-ttu-id="5882e-196">x</span><span class="sxs-lookup"><span data-stu-id="5882e-196">x</span></span>     | <span data-ttu-id="5882e-197">x</span><span class="sxs-lookup"><span data-stu-id="5882e-197">x</span></span>    | <span data-ttu-id="5882e-198">x</span><span class="sxs-lookup"><span data-stu-id="5882e-198">x</span></span>     |



 

<span data-ttu-id="5882e-199">\* Solo disponible si la máscara de escritura de destino es. w (. a).</span><span class="sxs-lookup"><span data-stu-id="5882e-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="5882e-200">Swizzle arbitrario</span><span class="sxs-lookup"><span data-stu-id="5882e-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="5882e-201">Swizzles se puede aplicar a los registros de origen en un orden arbitrario. es decir, cualquier registro de origen puede tomar cualquier máscara de componente, en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="5882e-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="5882e-202">Replicar swizzle</span><span class="sxs-lookup"><span data-stu-id="5882e-202">Replicate Swizzle</span></span>

<span data-ttu-id="5882e-203">Replicar swizzle copia un componente en otro.</span><span class="sxs-lookup"><span data-stu-id="5882e-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="5882e-204">Es, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).</span><span class="sxs-lookup"><span data-stu-id="5882e-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5882e-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5882e-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5882e-206">Modificadores de registro de origen del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5882e-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="5882e-207">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros</span><span class="sxs-lookup"><span data-stu-id="5882e-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="5882e-208">Registros de PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5882e-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="5882e-209">Registros de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5882e-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="5882e-210">Registros de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5882e-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




