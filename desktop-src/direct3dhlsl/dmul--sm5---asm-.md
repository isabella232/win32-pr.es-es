---
title: dmul (sm5 - asm)
description: Multiplicación de precisión doble por componentes.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999092"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="41ed4-103">dmul (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="41ed4-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="41ed4-104">Multiplicación de precisión doble por componentes.</span><span class="sxs-lookup"><span data-stu-id="41ed4-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="41ed4-105">dmul \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swzzle\]</span><span class="sxs-lookup"><span data-stu-id="41ed4-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="41ed4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="41ed4-106">Item</span></span>                                                            | <span data-ttu-id="41ed4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="41ed4-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ed4-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="41ed4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="41ed4-109">\[en \] La dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="41ed4-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="41ed4-110">*dest*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="41ed4-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="41ed4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="41ed4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="41ed4-112">\[en \] Componentes que se va a multiplicar por *src1*.</span><span class="sxs-lookup"><span data-stu-id="41ed4-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="41ed4-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="41ed4-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="41ed4-114">\[en \] Componentes que se va a multiplicar por *src0.*</span><span class="sxs-lookup"><span data-stu-id="41ed4-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="41ed4-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41ed4-115">Remarks</span></span>

<span data-ttu-id="41ed4-116">Los swzzles válidos para los parámetros de origen son .xyzw, .xyxy, .zwxy, .zwzw.</span><span class="sxs-lookup"><span data-stu-id="41ed4-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="41ed4-117">Las máscaras *dest* válidas son .xy, .zw y .xyzw.</span><span class="sxs-lookup"><span data-stu-id="41ed4-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="41ed4-118">Las siguientes *asignaciones de src* son posteriores a swzzle:</span><span class="sxs-lookup"><span data-stu-id="41ed4-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="41ed4-119">*dest* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="41ed4-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="41ed4-120">*src0* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="41ed4-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="41ed4-121">*src1* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="41ed4-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="41ed4-122">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="41ed4-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="41ed4-123">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="41ed4-123">F means finite-real number.</span></span>



| <span data-ttu-id="41ed4-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="41ed4-124">**src0 src1->**</span></span> | <span data-ttu-id="41ed4-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="41ed4-125">**-inf**</span></span> | <span data-ttu-id="41ed4-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="41ed4-126">**-F**</span></span> | <span data-ttu-id="41ed4-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-127">**-1.0**</span></span> | <span data-ttu-id="41ed4-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-128">**-0**</span></span> | <span data-ttu-id="41ed4-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-129">**+0**</span></span> | <span data-ttu-id="41ed4-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-130">**+1.0**</span></span> | <span data-ttu-id="41ed4-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="41ed4-131">**+F**</span></span> | <span data-ttu-id="41ed4-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="41ed4-132">**+inf**</span></span> | <span data-ttu-id="41ed4-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="41ed4-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="41ed4-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="41ed4-134">**-inf**</span></span>           | <span data-ttu-id="41ed4-135">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-135">+inf</span></span>     | <span data-ttu-id="41ed4-136">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-136">+inf</span></span>   | <span data-ttu-id="41ed4-137">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-137">+inf</span></span>     | <span data-ttu-id="41ed4-138">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-138">NaN</span></span>    | <span data-ttu-id="41ed4-139">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-139">NaN</span></span>    | <span data-ttu-id="41ed4-140">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-140">-inf</span></span>     | <span data-ttu-id="41ed4-141">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-141">-inf</span></span>   | <span data-ttu-id="41ed4-142">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-142">-inf</span></span>     | <span data-ttu-id="41ed4-143">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-143">NaN</span></span>     |
| <span data-ttu-id="41ed4-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="41ed4-144">**-F**</span></span>             | <span data-ttu-id="41ed4-145">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-145">+inf</span></span>     | <span data-ttu-id="41ed4-146">+F</span><span class="sxs-lookup"><span data-stu-id="41ed4-146">+F</span></span>     | <span data-ttu-id="41ed4-147">-src0</span><span class="sxs-lookup"><span data-stu-id="41ed4-147">-src0</span></span>    | <span data-ttu-id="41ed4-148">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-148">+0</span></span>     | <span data-ttu-id="41ed4-149">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-149">-0</span></span>     | <span data-ttu-id="41ed4-150">src0</span><span class="sxs-lookup"><span data-stu-id="41ed4-150">src0</span></span>     | <span data-ttu-id="41ed4-151">-F</span><span class="sxs-lookup"><span data-stu-id="41ed4-151">-F</span></span>     | <span data-ttu-id="41ed4-152">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-152">-inf</span></span>     | <span data-ttu-id="41ed4-153">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-153">NaN</span></span>     |
| <span data-ttu-id="41ed4-154">**-1.0F**</span><span class="sxs-lookup"><span data-stu-id="41ed4-154">**-1.0F**</span></span>          | <span data-ttu-id="41ed4-155">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-155">+inf</span></span>     | <span data-ttu-id="41ed4-156">-src1</span><span class="sxs-lookup"><span data-stu-id="41ed4-156">-src1</span></span>  | <span data-ttu-id="41ed4-157">+1.0</span><span class="sxs-lookup"><span data-stu-id="41ed4-157">+1.0</span></span>     | <span data-ttu-id="41ed4-158">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-158">+0</span></span>     | <span data-ttu-id="41ed4-159">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-159">-0</span></span>     | <span data-ttu-id="41ed4-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="41ed4-160">-1.0</span></span>     | <span data-ttu-id="41ed4-161">-src1</span><span class="sxs-lookup"><span data-stu-id="41ed4-161">-src1</span></span>  | <span data-ttu-id="41ed4-162">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-162">-inf</span></span>     | <span data-ttu-id="41ed4-163">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-163">NaN</span></span>     |
| <span data-ttu-id="41ed4-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-164">**-0**</span></span>             | <span data-ttu-id="41ed4-165">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-165">NaN</span></span>      | <span data-ttu-id="41ed4-166">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-166">+0</span></span>     | <span data-ttu-id="41ed4-167">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-167">+0</span></span>       | <span data-ttu-id="41ed4-168">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-168">+0</span></span>     | <span data-ttu-id="41ed4-169">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-169">-0</span></span>     | <span data-ttu-id="41ed4-170">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-170">-0</span></span>       | <span data-ttu-id="41ed4-171">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-171">-0</span></span>     | <span data-ttu-id="41ed4-172">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-172">NaN</span></span>      | <span data-ttu-id="41ed4-173">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-173">NaN</span></span>     |
| <span data-ttu-id="41ed4-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-174">**+0**</span></span>             | <span data-ttu-id="41ed4-175">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-175">NaN</span></span>      | <span data-ttu-id="41ed4-176">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-176">-0</span></span>     | <span data-ttu-id="41ed4-177">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-177">-0</span></span>       | <span data-ttu-id="41ed4-178">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-178">-0</span></span>     | <span data-ttu-id="41ed4-179">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-179">+0</span></span>     | <span data-ttu-id="41ed4-180">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-180">+0</span></span>       | <span data-ttu-id="41ed4-181">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-181">+0</span></span>     | <span data-ttu-id="41ed4-182">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-182">NaN</span></span>      | <span data-ttu-id="41ed4-183">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-183">NaN</span></span>     |
| <span data-ttu-id="41ed4-184">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="41ed4-184">**+1.0**</span></span>           | <span data-ttu-id="41ed4-185">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-185">-inf</span></span>     | <span data-ttu-id="41ed4-186">src1</span><span class="sxs-lookup"><span data-stu-id="41ed4-186">src1</span></span>   | <span data-ttu-id="41ed4-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="41ed4-187">-1.0</span></span>     | <span data-ttu-id="41ed4-188">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-188">-0</span></span>     | <span data-ttu-id="41ed4-189">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-189">+0</span></span>     | <span data-ttu-id="41ed4-190">+1</span><span class="sxs-lookup"><span data-stu-id="41ed4-190">+1</span></span>       | <span data-ttu-id="41ed4-191">src1</span><span class="sxs-lookup"><span data-stu-id="41ed4-191">src1</span></span>   | <span data-ttu-id="41ed4-192">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-192">+inf</span></span>     | <span data-ttu-id="41ed4-193">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-193">NaN</span></span>     |
| <span data-ttu-id="41ed4-194">**+F**</span><span class="sxs-lookup"><span data-stu-id="41ed4-194">**+F**</span></span>             | <span data-ttu-id="41ed4-195">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-195">-inf</span></span>     | <span data-ttu-id="41ed4-196">-F</span><span class="sxs-lookup"><span data-stu-id="41ed4-196">-F</span></span>     | <span data-ttu-id="41ed4-197">-src0</span><span class="sxs-lookup"><span data-stu-id="41ed4-197">-src0</span></span>    | <span data-ttu-id="41ed4-198">-0</span><span class="sxs-lookup"><span data-stu-id="41ed4-198">-0</span></span>     | <span data-ttu-id="41ed4-199">+0</span><span class="sxs-lookup"><span data-stu-id="41ed4-199">+0</span></span>     | <span data-ttu-id="41ed4-200">src0</span><span class="sxs-lookup"><span data-stu-id="41ed4-200">src0</span></span>     | <span data-ttu-id="41ed4-201">+F</span><span class="sxs-lookup"><span data-stu-id="41ed4-201">+F</span></span>     | <span data-ttu-id="41ed4-202">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-202">+inf</span></span>     | <span data-ttu-id="41ed4-203">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-203">NaN</span></span>     |
| <span data-ttu-id="41ed4-204">**+inf**</span><span class="sxs-lookup"><span data-stu-id="41ed4-204">**+inf**</span></span>           | <span data-ttu-id="41ed4-205">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-205">-inf</span></span>     | <span data-ttu-id="41ed4-206">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-206">-inf</span></span>   | <span data-ttu-id="41ed4-207">-inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-207">-inf</span></span>     | <span data-ttu-id="41ed4-208">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-208">NaN</span></span>    | <span data-ttu-id="41ed4-209">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-209">NaN</span></span>    | <span data-ttu-id="41ed4-210">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-210">+inf</span></span>     | <span data-ttu-id="41ed4-211">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-211">+inf</span></span>   | <span data-ttu-id="41ed4-212">+inf</span><span class="sxs-lookup"><span data-stu-id="41ed4-212">+inf</span></span>     | <span data-ttu-id="41ed4-213">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-213">NaN</span></span>     |
| <span data-ttu-id="41ed4-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="41ed4-214">**NaN**</span></span>            | <span data-ttu-id="41ed4-215">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-215">NaN</span></span>      | <span data-ttu-id="41ed4-216">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-216">NaN</span></span>    | <span data-ttu-id="41ed4-217">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-217">NaN</span></span>      | <span data-ttu-id="41ed4-218">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-218">NaN</span></span>    | <span data-ttu-id="41ed4-219">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-219">NaN</span></span>    | <span data-ttu-id="41ed4-220">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-220">NaN</span></span>      | <span data-ttu-id="41ed4-221">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-221">NaN</span></span>    | <span data-ttu-id="41ed4-222">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-222">NaN</span></span>      | <span data-ttu-id="41ed4-223">NaN</span><span class="sxs-lookup"><span data-stu-id="41ed4-223">NaN</span></span>     |



 

<span data-ttu-id="41ed4-224">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="41ed4-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="41ed4-225">Vértice</span><span class="sxs-lookup"><span data-stu-id="41ed4-225">Vertex</span></span> | <span data-ttu-id="41ed4-226">Casco</span><span class="sxs-lookup"><span data-stu-id="41ed4-226">Hull</span></span> | <span data-ttu-id="41ed4-227">Domain</span><span class="sxs-lookup"><span data-stu-id="41ed4-227">Domain</span></span> | <span data-ttu-id="41ed4-228">Geometría</span><span class="sxs-lookup"><span data-stu-id="41ed4-228">Geometry</span></span> | <span data-ttu-id="41ed4-229">Píxel</span><span class="sxs-lookup"><span data-stu-id="41ed4-229">Pixel</span></span> | <span data-ttu-id="41ed4-230">Proceso</span><span class="sxs-lookup"><span data-stu-id="41ed4-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="41ed4-231">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-231">X</span></span>      | <span data-ttu-id="41ed4-232">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-232">X</span></span>    | <span data-ttu-id="41ed4-233">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-233">X</span></span>      | <span data-ttu-id="41ed4-234">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-234">X</span></span>        | <span data-ttu-id="41ed4-235">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-235">X</span></span>     | <span data-ttu-id="41ed4-236">X</span><span class="sxs-lookup"><span data-stu-id="41ed4-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="41ed4-237">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="41ed4-237">Minimum Shader Model</span></span>

<span data-ttu-id="41ed4-238">Esta instrucción se admite en los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="41ed4-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="41ed4-239">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="41ed4-239">Shader Model</span></span>                                              | <span data-ttu-id="41ed4-240">Compatible</span><span class="sxs-lookup"><span data-stu-id="41ed4-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="41ed4-241">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="41ed4-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="41ed4-242">sí</span><span class="sxs-lookup"><span data-stu-id="41ed4-242">yes</span></span>       |
| [<span data-ttu-id="41ed4-243">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="41ed4-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="41ed4-244">no</span><span class="sxs-lookup"><span data-stu-id="41ed4-244">no</span></span>        |
| [<span data-ttu-id="41ed4-245">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="41ed4-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="41ed4-246">no</span><span class="sxs-lookup"><span data-stu-id="41ed4-246">no</span></span>        |
| [<span data-ttu-id="41ed4-247">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41ed4-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="41ed4-248">no</span><span class="sxs-lookup"><span data-stu-id="41ed4-248">no</span></span>        |
| [<span data-ttu-id="41ed4-249">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41ed4-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="41ed4-250">no</span><span class="sxs-lookup"><span data-stu-id="41ed4-250">no</span></span>        |
| [<span data-ttu-id="41ed4-251">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="41ed4-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="41ed4-252">no</span><span class="sxs-lookup"><span data-stu-id="41ed4-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="41ed4-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41ed4-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ed4-254">Ensamblado del modelo de sombreador 5 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="41ed4-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





