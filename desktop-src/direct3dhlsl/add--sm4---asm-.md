---
title: add (sm4 - asm)
description: Adición por componente de 2 vectores.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994982"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="d757c-103">add (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="d757c-103">add (sm4 - asm)</span></span>

<span data-ttu-id="d757c-104">Adición por componente de 2 vectores.</span><span class="sxs-lookup"><span data-stu-id="d757c-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="d757c-105">add \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw sw swzzle\]</span><span class="sxs-lookup"><span data-stu-id="d757c-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d757c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d757c-106">Item</span></span>                                                            | <span data-ttu-id="d757c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d757c-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d757c-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="d757c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d757c-109">\[en \] La dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d757c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="d757c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d757c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d757c-111">\[en \] El vector que se va a agregar a *src1.*</span><span class="sxs-lookup"><span data-stu-id="d757c-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="d757c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d757c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d757c-113">\[en \] Vector que se va a agregar a *src0.*</span><span class="sxs-lookup"><span data-stu-id="d757c-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="d757c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d757c-114">Remarks</span></span>

<span data-ttu-id="d757c-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.</span><span class="sxs-lookup"><span data-stu-id="d757c-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="d757c-116">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="d757c-116">F means finite real number.</span></span>



| <span data-ttu-id="d757c-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="d757c-117">**src0 src1->**</span></span> | <span data-ttu-id="d757c-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="d757c-118">**-inf**</span></span> | <span data-ttu-id="d757c-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="d757c-119">**-F**</span></span>     | <span data-ttu-id="d757c-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d757c-120">**-denorm**</span></span> | <span data-ttu-id="d757c-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="d757c-121">**-0**</span></span> | <span data-ttu-id="d757c-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="d757c-122">**+0**</span></span> | <span data-ttu-id="d757c-123">**denorm**</span><span class="sxs-lookup"><span data-stu-id="d757c-123">**denorm**</span></span> | <span data-ttu-id="d757c-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="d757c-124">**+F**</span></span>     | <span data-ttu-id="d757c-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="d757c-125">**+inf**</span></span> | <span data-ttu-id="d757c-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d757c-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="d757c-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="d757c-127">**-inf**</span></span>           | <span data-ttu-id="d757c-128">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-128">-inf</span></span>     | <span data-ttu-id="d757c-129">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-129">-inf</span></span>       | <span data-ttu-id="d757c-130">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-130">-inf</span></span>        | <span data-ttu-id="d757c-131">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-131">-inf</span></span>   | <span data-ttu-id="d757c-132">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-132">-inf</span></span>   | <span data-ttu-id="d757c-133">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-133">-inf</span></span>       | <span data-ttu-id="d757c-134">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-134">-inf</span></span>       | <span data-ttu-id="d757c-135">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-135">NaN</span></span>      | <span data-ttu-id="d757c-136">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-136">NaN</span></span>     |
| <span data-ttu-id="d757c-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="d757c-137">**-F**</span></span>             | <span data-ttu-id="d757c-138">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-138">-inf</span></span>     | <span data-ttu-id="d757c-139">-F</span><span class="sxs-lookup"><span data-stu-id="d757c-139">-F</span></span>         | <span data-ttu-id="d757c-140">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-140">src0</span></span>        | <span data-ttu-id="d757c-141">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-141">src0</span></span>   | <span data-ttu-id="d757c-142">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-142">src0</span></span>   | <span data-ttu-id="d757c-143">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-143">src0</span></span>       | <span data-ttu-id="d757c-144">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="d757c-144">+-F or +-0</span></span> | <span data-ttu-id="d757c-145">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-145">+inf</span></span>     | <span data-ttu-id="d757c-146">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-146">NaN</span></span>     |
| <span data-ttu-id="d757c-147">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="d757c-147">**-denorm**</span></span>        | <span data-ttu-id="d757c-148">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-148">-inf</span></span>     | <span data-ttu-id="d757c-149">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-149">src1</span></span>       | <span data-ttu-id="d757c-150">-0</span><span class="sxs-lookup"><span data-stu-id="d757c-150">-0</span></span>          | <span data-ttu-id="d757c-151">-0</span><span class="sxs-lookup"><span data-stu-id="d757c-151">-0</span></span>     | <span data-ttu-id="d757c-152">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-152">+0</span></span>     | <span data-ttu-id="d757c-153">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-153">+0</span></span>         | <span data-ttu-id="d757c-154">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-154">src1</span></span>       | <span data-ttu-id="d757c-155">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-155">+inf</span></span>     | <span data-ttu-id="d757c-156">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-156">NaN</span></span>     |
| <span data-ttu-id="d757c-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="d757c-157">**-0**</span></span>             | <span data-ttu-id="d757c-158">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-158">-inf</span></span>     | <span data-ttu-id="d757c-159">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-159">src1</span></span>       | <span data-ttu-id="d757c-160">-0</span><span class="sxs-lookup"><span data-stu-id="d757c-160">-0</span></span>          | <span data-ttu-id="d757c-161">-0</span><span class="sxs-lookup"><span data-stu-id="d757c-161">-0</span></span>     | <span data-ttu-id="d757c-162">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-162">+0</span></span>     | <span data-ttu-id="d757c-163">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-163">+0</span></span>         | <span data-ttu-id="d757c-164">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-164">src1</span></span>       | <span data-ttu-id="d757c-165">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-165">+inf</span></span>     | <span data-ttu-id="d757c-166">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-166">NaN</span></span>     |
| <span data-ttu-id="d757c-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="d757c-167">**+0**</span></span>             | <span data-ttu-id="d757c-168">i-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-168">i-inf</span></span>    | <span data-ttu-id="d757c-169">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-169">src1</span></span>       | <span data-ttu-id="d757c-170">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-170">+0</span></span>          | <span data-ttu-id="d757c-171">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-171">+0</span></span>     | <span data-ttu-id="d757c-172">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-172">+0</span></span>     | <span data-ttu-id="d757c-173">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-173">+0</span></span>         | <span data-ttu-id="d757c-174">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-174">src1</span></span>       | <span data-ttu-id="d757c-175">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-175">+inf</span></span>     | <span data-ttu-id="d757c-176">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-176">NaN</span></span>     |
| <span data-ttu-id="d757c-177">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="d757c-177">**+denorm**</span></span>        | <span data-ttu-id="d757c-178">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-178">-inf</span></span>     | <span data-ttu-id="d757c-179">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-179">src1</span></span>       | <span data-ttu-id="d757c-180">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-180">+0</span></span>          | <span data-ttu-id="d757c-181">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-181">+0</span></span>     | <span data-ttu-id="d757c-182">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-182">+0</span></span>     | <span data-ttu-id="d757c-183">+0</span><span class="sxs-lookup"><span data-stu-id="d757c-183">+0</span></span>         | <span data-ttu-id="d757c-184">src1</span><span class="sxs-lookup"><span data-stu-id="d757c-184">src1</span></span>       | <span data-ttu-id="d757c-185">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-185">+inf</span></span>     | <span data-ttu-id="d757c-186">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-186">NaN</span></span>     |
| <span data-ttu-id="d757c-187">**+F**</span><span class="sxs-lookup"><span data-stu-id="d757c-187">**+F**</span></span>             | <span data-ttu-id="d757c-188">-inf</span><span class="sxs-lookup"><span data-stu-id="d757c-188">-inf</span></span>     | <span data-ttu-id="d757c-189">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="d757c-189">+-F or +-0</span></span> | <span data-ttu-id="d757c-190">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-190">src0</span></span>        | <span data-ttu-id="d757c-191">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-191">src0</span></span>   | <span data-ttu-id="d757c-192">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-192">src0</span></span>   | <span data-ttu-id="d757c-193">src0</span><span class="sxs-lookup"><span data-stu-id="d757c-193">src0</span></span>       | <span data-ttu-id="d757c-194">+F</span><span class="sxs-lookup"><span data-stu-id="d757c-194">+F</span></span>         | <span data-ttu-id="d757c-195">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-195">+inf</span></span>     | <span data-ttu-id="d757c-196">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-196">NaN</span></span>     |
| <span data-ttu-id="d757c-197">**+inf**</span><span class="sxs-lookup"><span data-stu-id="d757c-197">**+inf**</span></span>           | <span data-ttu-id="d757c-198">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-198">NaN</span></span>      | <span data-ttu-id="d757c-199">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-199">+inf</span></span>       | <span data-ttu-id="d757c-200">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-200">+inf</span></span>        | <span data-ttu-id="d757c-201">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-201">+inf</span></span>   | <span data-ttu-id="d757c-202">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-202">+inf</span></span>   | <span data-ttu-id="d757c-203">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-203">+inf</span></span>       | <span data-ttu-id="d757c-204">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-204">+inf</span></span>       | <span data-ttu-id="d757c-205">+inf</span><span class="sxs-lookup"><span data-stu-id="d757c-205">+inf</span></span>     | <span data-ttu-id="d757c-206">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-206">NaN</span></span>     |
| <span data-ttu-id="d757c-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d757c-207">**NaN**</span></span>            | <span data-ttu-id="d757c-208">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-208">NaN</span></span>      | <span data-ttu-id="d757c-209">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-209">NaN</span></span>        | <span data-ttu-id="d757c-210">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-210">NaN</span></span>         | <span data-ttu-id="d757c-211">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-211">NaN</span></span>    | <span data-ttu-id="d757c-212">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-212">NaN</span></span>    | <span data-ttu-id="d757c-213">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-213">NaN</span></span>        | <span data-ttu-id="d757c-214">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-214">NaN</span></span>        | <span data-ttu-id="d757c-215">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-215">NaN</span></span>      | <span data-ttu-id="d757c-216">NaN</span><span class="sxs-lookup"><span data-stu-id="d757c-216">NaN</span></span>     |



 

<span data-ttu-id="d757c-217">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d757c-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d757c-218">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d757c-218">Vertex Shader</span></span> | <span data-ttu-id="d757c-219">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d757c-219">Geometry Shader</span></span> | <span data-ttu-id="d757c-220">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d757c-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d757c-221">x</span><span class="sxs-lookup"><span data-stu-id="d757c-221">x</span></span>             | <span data-ttu-id="d757c-222">x</span><span class="sxs-lookup"><span data-stu-id="d757c-222">x</span></span>               | <span data-ttu-id="d757c-223">x</span><span class="sxs-lookup"><span data-stu-id="d757c-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d757c-224">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d757c-224">Minimum Shader Model</span></span>

<span data-ttu-id="d757c-225">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d757c-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d757c-226">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d757c-226">Shader Model</span></span>                                              | <span data-ttu-id="d757c-227">Compatible</span><span class="sxs-lookup"><span data-stu-id="d757c-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d757c-228">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d757c-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d757c-229">sí</span><span class="sxs-lookup"><span data-stu-id="d757c-229">yes</span></span>       |
| [<span data-ttu-id="d757c-230">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="d757c-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d757c-231">sí</span><span class="sxs-lookup"><span data-stu-id="d757c-231">yes</span></span>       |
| [<span data-ttu-id="d757c-232">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="d757c-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d757c-233">sí</span><span class="sxs-lookup"><span data-stu-id="d757c-233">yes</span></span>       |
| [<span data-ttu-id="d757c-234">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d757c-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d757c-235">no</span><span class="sxs-lookup"><span data-stu-id="d757c-235">no</span></span>        |
| [<span data-ttu-id="d757c-236">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d757c-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d757c-237">no</span><span class="sxs-lookup"><span data-stu-id="d757c-237">no</span></span>        |
| [<span data-ttu-id="d757c-238">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d757c-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d757c-239">no</span><span class="sxs-lookup"><span data-stu-id="d757c-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d757c-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d757c-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d757c-241">Ensamblado del modelo 4 del sombreador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="d757c-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





