---
title: Agregar (SM4-ASM)
description: Agregación por componente de 2 vectores.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532890"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="fd2cc-103">Agregar (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fd2cc-103">add (sm4 - asm)</span></span>

<span data-ttu-id="fd2cc-104">Agregación por componente de 2 vectores.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="fd2cc-105">agregue \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fd2cc-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="fd2cc-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd2cc-106">Item</span></span>                                                            | <span data-ttu-id="fd2cc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd2cc-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fd2cc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fd2cc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fd2cc-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fd2cc-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fd2cc-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fd2cc-111">\[en \] el vector que se va a agregar a *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="fd2cc-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="fd2cc-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fd2cc-113">\[en \] el vector que se va a agregar a *src0*.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="fd2cc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd2cc-114">Remarks</span></span>

<span data-ttu-id="fd2cc-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="fd2cc-116">F significa un número real finito.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="fd2cc-117">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-117">**src0 src1->**</span></span> | <span data-ttu-id="fd2cc-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-118">**-inf**</span></span> | <span data-ttu-id="fd2cc-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-119">**-F**</span></span>     | <span data-ttu-id="fd2cc-120">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-120">**-denorm**</span></span> | <span data-ttu-id="fd2cc-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-121">**-0**</span></span> | <span data-ttu-id="fd2cc-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-122">**+0**</span></span> | <span data-ttu-id="fd2cc-123">**desnormativa**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-123">**denorm**</span></span> | <span data-ttu-id="fd2cc-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-124">**+F**</span></span>     | <span data-ttu-id="fd2cc-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-125">**+inf**</span></span> | <span data-ttu-id="fd2cc-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-126">**NaN**</span></span> |
| <span data-ttu-id="fd2cc-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-127">**-inf**</span></span>           | <span data-ttu-id="fd2cc-128">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-128">-inf</span></span>     | <span data-ttu-id="fd2cc-129">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-129">-inf</span></span>       | <span data-ttu-id="fd2cc-130">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-130">-inf</span></span>        | <span data-ttu-id="fd2cc-131">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-131">-inf</span></span>   | <span data-ttu-id="fd2cc-132">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-132">-inf</span></span>   | <span data-ttu-id="fd2cc-133">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-133">-inf</span></span>       | <span data-ttu-id="fd2cc-134">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-134">-inf</span></span>       | <span data-ttu-id="fd2cc-135">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-135">NaN</span></span>      | <span data-ttu-id="fd2cc-136">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-136">NaN</span></span>     |
| <span data-ttu-id="fd2cc-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-137">**-F**</span></span>             | <span data-ttu-id="fd2cc-138">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-138">-inf</span></span>     | <span data-ttu-id="fd2cc-139">-F</span><span class="sxs-lookup"><span data-stu-id="fd2cc-139">-F</span></span>         | <span data-ttu-id="fd2cc-140">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-140">src0</span></span>        | <span data-ttu-id="fd2cc-141">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-141">src0</span></span>   | <span data-ttu-id="fd2cc-142">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-142">src0</span></span>   | <span data-ttu-id="fd2cc-143">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-143">src0</span></span>       | <span data-ttu-id="fd2cc-144">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-144">+-F or +-0</span></span> | <span data-ttu-id="fd2cc-145">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-145">+inf</span></span>     | <span data-ttu-id="fd2cc-146">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-146">NaN</span></span>     |
| <span data-ttu-id="fd2cc-147">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-147">**-denorm**</span></span>        | <span data-ttu-id="fd2cc-148">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-148">-inf</span></span>     | <span data-ttu-id="fd2cc-149">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-149">src1</span></span>       | <span data-ttu-id="fd2cc-150">-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-150">-0</span></span>          | <span data-ttu-id="fd2cc-151">-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-151">-0</span></span>     | <span data-ttu-id="fd2cc-152">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-152">+0</span></span>     | <span data-ttu-id="fd2cc-153">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-153">+0</span></span>         | <span data-ttu-id="fd2cc-154">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-154">src1</span></span>       | <span data-ttu-id="fd2cc-155">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-155">+inf</span></span>     | <span data-ttu-id="fd2cc-156">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-156">NaN</span></span>     |
| <span data-ttu-id="fd2cc-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-157">**-0**</span></span>             | <span data-ttu-id="fd2cc-158">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-158">-inf</span></span>     | <span data-ttu-id="fd2cc-159">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-159">src1</span></span>       | <span data-ttu-id="fd2cc-160">-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-160">-0</span></span>          | <span data-ttu-id="fd2cc-161">-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-161">-0</span></span>     | <span data-ttu-id="fd2cc-162">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-162">+0</span></span>     | <span data-ttu-id="fd2cc-163">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-163">+0</span></span>         | <span data-ttu-id="fd2cc-164">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-164">src1</span></span>       | <span data-ttu-id="fd2cc-165">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-165">+inf</span></span>     | <span data-ttu-id="fd2cc-166">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-166">NaN</span></span>     |
| <span data-ttu-id="fd2cc-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-167">**+0**</span></span>             | <span data-ttu-id="fd2cc-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="fd2cc-168">i-inf</span></span>    | <span data-ttu-id="fd2cc-169">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-169">src1</span></span>       | <span data-ttu-id="fd2cc-170">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-170">+0</span></span>          | <span data-ttu-id="fd2cc-171">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-171">+0</span></span>     | <span data-ttu-id="fd2cc-172">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-172">+0</span></span>     | <span data-ttu-id="fd2cc-173">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-173">+0</span></span>         | <span data-ttu-id="fd2cc-174">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-174">src1</span></span>       | <span data-ttu-id="fd2cc-175">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-175">+inf</span></span>     | <span data-ttu-id="fd2cc-176">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-176">NaN</span></span>     |
| <span data-ttu-id="fd2cc-177">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-177">**+denorm**</span></span>        | <span data-ttu-id="fd2cc-178">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-178">-inf</span></span>     | <span data-ttu-id="fd2cc-179">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-179">src1</span></span>       | <span data-ttu-id="fd2cc-180">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-180">+0</span></span>          | <span data-ttu-id="fd2cc-181">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-181">+0</span></span>     | <span data-ttu-id="fd2cc-182">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-182">+0</span></span>     | <span data-ttu-id="fd2cc-183">+0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-183">+0</span></span>         | <span data-ttu-id="fd2cc-184">src1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-184">src1</span></span>       | <span data-ttu-id="fd2cc-185">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-185">+inf</span></span>     | <span data-ttu-id="fd2cc-186">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-186">NaN</span></span>     |
| <span data-ttu-id="fd2cc-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-187">**+F**</span></span>             | <span data-ttu-id="fd2cc-188">-inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-188">-inf</span></span>     | <span data-ttu-id="fd2cc-189">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-189">+-F or +-0</span></span> | <span data-ttu-id="fd2cc-190">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-190">src0</span></span>        | <span data-ttu-id="fd2cc-191">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-191">src0</span></span>   | <span data-ttu-id="fd2cc-192">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-192">src0</span></span>   | <span data-ttu-id="fd2cc-193">src0</span><span class="sxs-lookup"><span data-stu-id="fd2cc-193">src0</span></span>       | <span data-ttu-id="fd2cc-194">+F</span><span class="sxs-lookup"><span data-stu-id="fd2cc-194">+F</span></span>         | <span data-ttu-id="fd2cc-195">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-195">+inf</span></span>     | <span data-ttu-id="fd2cc-196">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-196">NaN</span></span>     |
| <span data-ttu-id="fd2cc-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-197">**+inf**</span></span>           | <span data-ttu-id="fd2cc-198">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-198">NaN</span></span>      | <span data-ttu-id="fd2cc-199">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-199">+inf</span></span>       | <span data-ttu-id="fd2cc-200">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-200">+inf</span></span>        | <span data-ttu-id="fd2cc-201">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-201">+inf</span></span>   | <span data-ttu-id="fd2cc-202">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-202">+inf</span></span>   | <span data-ttu-id="fd2cc-203">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-203">+inf</span></span>       | <span data-ttu-id="fd2cc-204">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-204">+inf</span></span>       | <span data-ttu-id="fd2cc-205">+inf</span><span class="sxs-lookup"><span data-stu-id="fd2cc-205">+inf</span></span>     | <span data-ttu-id="fd2cc-206">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-206">NaN</span></span>     |
| <span data-ttu-id="fd2cc-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="fd2cc-207">**NaN**</span></span>            | <span data-ttu-id="fd2cc-208">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-208">NaN</span></span>      | <span data-ttu-id="fd2cc-209">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-209">NaN</span></span>        | <span data-ttu-id="fd2cc-210">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-210">NaN</span></span>         | <span data-ttu-id="fd2cc-211">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-211">NaN</span></span>    | <span data-ttu-id="fd2cc-212">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-212">NaN</span></span>    | <span data-ttu-id="fd2cc-213">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-213">NaN</span></span>        | <span data-ttu-id="fd2cc-214">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-214">NaN</span></span>        | <span data-ttu-id="fd2cc-215">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-215">NaN</span></span>      | <span data-ttu-id="fd2cc-216">NaN</span><span class="sxs-lookup"><span data-stu-id="fd2cc-216">NaN</span></span>     |



 

<span data-ttu-id="fd2cc-217">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fd2cc-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fd2cc-218">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fd2cc-218">Vertex Shader</span></span> | <span data-ttu-id="fd2cc-219">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fd2cc-219">Geometry Shader</span></span> | <span data-ttu-id="fd2cc-220">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fd2cc-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fd2cc-221">x</span><span class="sxs-lookup"><span data-stu-id="fd2cc-221">x</span></span>             | <span data-ttu-id="fd2cc-222">x</span><span class="sxs-lookup"><span data-stu-id="fd2cc-222">x</span></span>               | <span data-ttu-id="fd2cc-223">x</span><span class="sxs-lookup"><span data-stu-id="fd2cc-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fd2cc-224">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fd2cc-224">Minimum Shader Model</span></span>

<span data-ttu-id="fd2cc-225">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fd2cc-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fd2cc-226">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fd2cc-226">Shader Model</span></span>                                              | <span data-ttu-id="fd2cc-227">Compatible</span><span class="sxs-lookup"><span data-stu-id="fd2cc-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fd2cc-228">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fd2cc-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fd2cc-229">sí</span><span class="sxs-lookup"><span data-stu-id="fd2cc-229">yes</span></span>       |
| [<span data-ttu-id="fd2cc-230">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fd2cc-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fd2cc-231">sí</span><span class="sxs-lookup"><span data-stu-id="fd2cc-231">yes</span></span>       |
| [<span data-ttu-id="fd2cc-232">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fd2cc-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd2cc-233">sí</span><span class="sxs-lookup"><span data-stu-id="fd2cc-233">yes</span></span>       |
| [<span data-ttu-id="fd2cc-234">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd2cc-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd2cc-235">no</span><span class="sxs-lookup"><span data-stu-id="fd2cc-235">no</span></span>        |
| [<span data-ttu-id="fd2cc-236">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd2cc-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd2cc-237">no</span><span class="sxs-lookup"><span data-stu-id="fd2cc-237">no</span></span>        |
| [<span data-ttu-id="fd2cc-238">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd2cc-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd2cc-239">no</span><span class="sxs-lookup"><span data-stu-id="fd2cc-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fd2cc-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd2cc-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd2cc-241">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd2cc-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





