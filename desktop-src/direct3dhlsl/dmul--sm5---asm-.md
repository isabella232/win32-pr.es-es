---
title: dmul (SM5-ASM)
description: Multiplicación de doble precisión para componentes.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996893"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="a8f78-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a8f78-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="a8f78-104">Multiplicación de doble precisión para componentes.</span><span class="sxs-lookup"><span data-stu-id="a8f78-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="a8f78-105">dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a8f78-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a8f78-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8f78-106">Item</span></span>                                                            | <span data-ttu-id="a8f78-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8f78-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f78-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a8f78-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a8f78-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a8f78-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="a8f78-110">*dest*  =  *src0* \* *SRC1*</span><span class="sxs-lookup"><span data-stu-id="a8f78-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="a8f78-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a8f78-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a8f78-112">\[en \] los componentes que se van a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="a8f78-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="a8f78-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="a8f78-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a8f78-114">\[en \] los componentes que se van a multiplicar por *src0*.</span><span class="sxs-lookup"><span data-stu-id="a8f78-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="a8f78-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8f78-115">Remarks</span></span>

<span data-ttu-id="a8f78-116">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="a8f78-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="a8f78-117">Las máscaras de *destino* válidas son. XY,. ZW y. xyzw.</span><span class="sxs-lookup"><span data-stu-id="a8f78-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="a8f78-118">Las siguientes asignaciones *src* son post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="a8f78-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="a8f78-119">*dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8f78-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a8f78-120">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8f78-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a8f78-121">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8f78-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="a8f78-122">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="a8f78-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="a8f78-123">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="a8f78-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="a8f78-124">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="a8f78-124">**src0 src1->**</span></span> | <span data-ttu-id="a8f78-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a8f78-125">**-inf**</span></span> | <span data-ttu-id="a8f78-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8f78-126">**-F**</span></span> | <span data-ttu-id="a8f78-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-127">**-1.0**</span></span> | <span data-ttu-id="a8f78-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-128">**-0**</span></span> | <span data-ttu-id="a8f78-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-129">**+0**</span></span> | <span data-ttu-id="a8f78-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-130">**+1.0**</span></span> | <span data-ttu-id="a8f78-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a8f78-131">**+F**</span></span> | <span data-ttu-id="a8f78-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a8f78-132">**+inf**</span></span> | <span data-ttu-id="a8f78-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8f78-133">**NaN**</span></span> |
| <span data-ttu-id="a8f78-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a8f78-134">**-inf**</span></span>           | <span data-ttu-id="a8f78-135">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-135">+inf</span></span>     | <span data-ttu-id="a8f78-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-136">+inf</span></span>   | <span data-ttu-id="a8f78-137">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-137">+inf</span></span>     | <span data-ttu-id="a8f78-138">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-138">NaN</span></span>    | <span data-ttu-id="a8f78-139">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-139">NaN</span></span>    | <span data-ttu-id="a8f78-140">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-140">-inf</span></span>     | <span data-ttu-id="a8f78-141">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-141">-inf</span></span>   | <span data-ttu-id="a8f78-142">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-142">-inf</span></span>     | <span data-ttu-id="a8f78-143">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-143">NaN</span></span>     |
| <span data-ttu-id="a8f78-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8f78-144">**-F**</span></span>             | <span data-ttu-id="a8f78-145">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-145">+inf</span></span>     | <span data-ttu-id="a8f78-146">+F</span><span class="sxs-lookup"><span data-stu-id="a8f78-146">+F</span></span>     | <span data-ttu-id="a8f78-147">-src0</span><span class="sxs-lookup"><span data-stu-id="a8f78-147">-src0</span></span>    | <span data-ttu-id="a8f78-148">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-148">+0</span></span>     | <span data-ttu-id="a8f78-149">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-149">-0</span></span>     | <span data-ttu-id="a8f78-150">src0</span><span class="sxs-lookup"><span data-stu-id="a8f78-150">src0</span></span>     | <span data-ttu-id="a8f78-151">-F</span><span class="sxs-lookup"><span data-stu-id="a8f78-151">-F</span></span>     | <span data-ttu-id="a8f78-152">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-152">-inf</span></span>     | <span data-ttu-id="a8f78-153">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-153">NaN</span></span>     |
| <span data-ttu-id="a8f78-154">**-1,0 f**</span><span class="sxs-lookup"><span data-stu-id="a8f78-154">**-1.0F**</span></span>          | <span data-ttu-id="a8f78-155">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-155">+inf</span></span>     | <span data-ttu-id="a8f78-156">-SRC1</span><span class="sxs-lookup"><span data-stu-id="a8f78-156">-src1</span></span>  | <span data-ttu-id="a8f78-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="a8f78-157">+1.0</span></span>     | <span data-ttu-id="a8f78-158">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-158">+0</span></span>     | <span data-ttu-id="a8f78-159">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-159">-0</span></span>     | <span data-ttu-id="a8f78-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="a8f78-160">-1.0</span></span>     | <span data-ttu-id="a8f78-161">-SRC1</span><span class="sxs-lookup"><span data-stu-id="a8f78-161">-src1</span></span>  | <span data-ttu-id="a8f78-162">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-162">-inf</span></span>     | <span data-ttu-id="a8f78-163">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-163">NaN</span></span>     |
| <span data-ttu-id="a8f78-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-164">**-0**</span></span>             | <span data-ttu-id="a8f78-165">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-165">NaN</span></span>      | <span data-ttu-id="a8f78-166">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-166">+0</span></span>     | <span data-ttu-id="a8f78-167">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-167">+0</span></span>       | <span data-ttu-id="a8f78-168">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-168">+0</span></span>     | <span data-ttu-id="a8f78-169">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-169">-0</span></span>     | <span data-ttu-id="a8f78-170">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-170">-0</span></span>       | <span data-ttu-id="a8f78-171">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-171">-0</span></span>     | <span data-ttu-id="a8f78-172">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-172">NaN</span></span>      | <span data-ttu-id="a8f78-173">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-173">NaN</span></span>     |
| <span data-ttu-id="a8f78-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-174">**+0**</span></span>             | <span data-ttu-id="a8f78-175">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-175">NaN</span></span>      | <span data-ttu-id="a8f78-176">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-176">-0</span></span>     | <span data-ttu-id="a8f78-177">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-177">-0</span></span>       | <span data-ttu-id="a8f78-178">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-178">-0</span></span>     | <span data-ttu-id="a8f78-179">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-179">+0</span></span>     | <span data-ttu-id="a8f78-180">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-180">+0</span></span>       | <span data-ttu-id="a8f78-181">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-181">+0</span></span>     | <span data-ttu-id="a8f78-182">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-182">NaN</span></span>      | <span data-ttu-id="a8f78-183">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-183">NaN</span></span>     |
| <span data-ttu-id="a8f78-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="a8f78-184">**+1.0**</span></span>           | <span data-ttu-id="a8f78-185">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-185">-inf</span></span>     | <span data-ttu-id="a8f78-186">src1</span><span class="sxs-lookup"><span data-stu-id="a8f78-186">src1</span></span>   | <span data-ttu-id="a8f78-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="a8f78-187">-1.0</span></span>     | <span data-ttu-id="a8f78-188">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-188">-0</span></span>     | <span data-ttu-id="a8f78-189">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-189">+0</span></span>     | <span data-ttu-id="a8f78-190">+1</span><span class="sxs-lookup"><span data-stu-id="a8f78-190">+1</span></span>       | <span data-ttu-id="a8f78-191">src1</span><span class="sxs-lookup"><span data-stu-id="a8f78-191">src1</span></span>   | <span data-ttu-id="a8f78-192">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-192">+inf</span></span>     | <span data-ttu-id="a8f78-193">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-193">NaN</span></span>     |
| <span data-ttu-id="a8f78-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a8f78-194">**+F**</span></span>             | <span data-ttu-id="a8f78-195">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-195">-inf</span></span>     | <span data-ttu-id="a8f78-196">-F</span><span class="sxs-lookup"><span data-stu-id="a8f78-196">-F</span></span>     | <span data-ttu-id="a8f78-197">-src0</span><span class="sxs-lookup"><span data-stu-id="a8f78-197">-src0</span></span>    | <span data-ttu-id="a8f78-198">-0</span><span class="sxs-lookup"><span data-stu-id="a8f78-198">-0</span></span>     | <span data-ttu-id="a8f78-199">+0</span><span class="sxs-lookup"><span data-stu-id="a8f78-199">+0</span></span>     | <span data-ttu-id="a8f78-200">src0</span><span class="sxs-lookup"><span data-stu-id="a8f78-200">src0</span></span>     | <span data-ttu-id="a8f78-201">+F</span><span class="sxs-lookup"><span data-stu-id="a8f78-201">+F</span></span>     | <span data-ttu-id="a8f78-202">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-202">+inf</span></span>     | <span data-ttu-id="a8f78-203">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-203">NaN</span></span>     |
| <span data-ttu-id="a8f78-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a8f78-204">**+inf**</span></span>           | <span data-ttu-id="a8f78-205">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-205">-inf</span></span>     | <span data-ttu-id="a8f78-206">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-206">-inf</span></span>   | <span data-ttu-id="a8f78-207">-inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-207">-inf</span></span>     | <span data-ttu-id="a8f78-208">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-208">NaN</span></span>    | <span data-ttu-id="a8f78-209">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-209">NaN</span></span>    | <span data-ttu-id="a8f78-210">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-210">+inf</span></span>     | <span data-ttu-id="a8f78-211">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-211">+inf</span></span>   | <span data-ttu-id="a8f78-212">+inf</span><span class="sxs-lookup"><span data-stu-id="a8f78-212">+inf</span></span>     | <span data-ttu-id="a8f78-213">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-213">NaN</span></span>     |
| <span data-ttu-id="a8f78-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8f78-214">**NaN**</span></span>            | <span data-ttu-id="a8f78-215">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-215">NaN</span></span>      | <span data-ttu-id="a8f78-216">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-216">NaN</span></span>    | <span data-ttu-id="a8f78-217">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-217">NaN</span></span>      | <span data-ttu-id="a8f78-218">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-218">NaN</span></span>    | <span data-ttu-id="a8f78-219">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-219">NaN</span></span>    | <span data-ttu-id="a8f78-220">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-220">NaN</span></span>      | <span data-ttu-id="a8f78-221">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-221">NaN</span></span>    | <span data-ttu-id="a8f78-222">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-222">NaN</span></span>      | <span data-ttu-id="a8f78-223">NaN</span><span class="sxs-lookup"><span data-stu-id="a8f78-223">NaN</span></span>     |



 

<span data-ttu-id="a8f78-224">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a8f78-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8f78-225">Vértice</span><span class="sxs-lookup"><span data-stu-id="a8f78-225">Vertex</span></span> | <span data-ttu-id="a8f78-226">Casco</span><span class="sxs-lookup"><span data-stu-id="a8f78-226">Hull</span></span> | <span data-ttu-id="a8f78-227">Dominio</span><span class="sxs-lookup"><span data-stu-id="a8f78-227">Domain</span></span> | <span data-ttu-id="a8f78-228">Geometría</span><span class="sxs-lookup"><span data-stu-id="a8f78-228">Geometry</span></span> | <span data-ttu-id="a8f78-229">Píxel</span><span class="sxs-lookup"><span data-stu-id="a8f78-229">Pixel</span></span> | <span data-ttu-id="a8f78-230">Compute</span><span class="sxs-lookup"><span data-stu-id="a8f78-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8f78-231">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-231">X</span></span>      | <span data-ttu-id="a8f78-232">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-232">X</span></span>    | <span data-ttu-id="a8f78-233">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-233">X</span></span>      | <span data-ttu-id="a8f78-234">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-234">X</span></span>        | <span data-ttu-id="a8f78-235">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-235">X</span></span>     | <span data-ttu-id="a8f78-236">X</span><span class="sxs-lookup"><span data-stu-id="a8f78-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8f78-237">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a8f78-237">Minimum Shader Model</span></span>

<span data-ttu-id="a8f78-238">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a8f78-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8f78-239">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8f78-239">Shader Model</span></span>                                              | <span data-ttu-id="a8f78-240">Compatible</span><span class="sxs-lookup"><span data-stu-id="a8f78-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8f78-241">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a8f78-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8f78-242">sí</span><span class="sxs-lookup"><span data-stu-id="a8f78-242">yes</span></span>       |
| [<span data-ttu-id="a8f78-243">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a8f78-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8f78-244">no</span><span class="sxs-lookup"><span data-stu-id="a8f78-244">no</span></span>        |
| [<span data-ttu-id="a8f78-245">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a8f78-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8f78-246">no</span><span class="sxs-lookup"><span data-stu-id="a8f78-246">no</span></span>        |
| [<span data-ttu-id="a8f78-247">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8f78-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8f78-248">no</span><span class="sxs-lookup"><span data-stu-id="a8f78-248">no</span></span>        |
| [<span data-ttu-id="a8f78-249">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8f78-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8f78-250">no</span><span class="sxs-lookup"><span data-stu-id="a8f78-250">no</span></span>        |
| [<span data-ttu-id="a8f78-251">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8f78-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8f78-252">no</span><span class="sxs-lookup"><span data-stu-id="a8f78-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8f78-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8f78-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8f78-254">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8f78-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





