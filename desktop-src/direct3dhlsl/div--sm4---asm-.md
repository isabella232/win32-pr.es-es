---
title: div (sm4 - asm)
description: División por componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999102"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="494cb-103">div (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="494cb-103">div (sm4 - asm)</span></span>

<span data-ttu-id="494cb-104">División por componente.</span><span class="sxs-lookup"><span data-stu-id="494cb-104">Component-wise divide.</span></span>



| <span data-ttu-id="494cb-105">div \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] \[ - \] src1 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="494cb-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="494cb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="494cb-106">Item</span></span>                                                            | <span data-ttu-id="494cb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="494cb-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="494cb-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="494cb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="494cb-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="494cb-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="494cb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="494cb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="494cb-111">\[en \] El dividendo.</span><span class="sxs-lookup"><span data-stu-id="494cb-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="494cb-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="494cb-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="494cb-113">\[en \] el divisor.</span><span class="sxs-lookup"><span data-stu-id="494cb-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="494cb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="494cb-114">Remarks</span></span>

<span data-ttu-id="494cb-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="494cb-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="494cb-116">Debe tener en cuenta las dos implementaciones permitidas de divide: a/b y a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="494cb-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="494cb-117">Un resultado de esto es que hay excepciones en la tabla siguiente para valores denominadores grandes (mayor que 8,5070592e+37), donde 1/denominador es un desnormado.</span><span class="sxs-lookup"><span data-stu-id="494cb-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="494cb-118">Dado que las implementaciones pueden realizar la división como (1/b), en lugar de a/b directamente, y un valor grande de 1/ es un \* \[ desnorma que podría vaciarse, algunos casos de la tabla producirían resultados \] diferentes.</span><span class="sxs-lookup"><span data-stu-id="494cb-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="494cb-119">Por ejemplo, el valor (+/-)INF / (+/-) \[ > 8.5070592e+37 puede generar NaN en algunas implementaciones, pero \] (+/-)INF en otras implementaciones</span><span class="sxs-lookup"><span data-stu-id="494cb-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="494cb-120">En esta tabla, F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="494cb-120">In this table F means finite-real number.</span></span>



| <span data-ttu-id="494cb-121">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="494cb-121">**src0 src1 ->**</span></span> | <span data-ttu-id="494cb-122">**-inf**</span><span class="sxs-lookup"><span data-stu-id="494cb-122">**-inf**</span></span> | <span data-ttu-id="494cb-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="494cb-123">**-F**</span></span>     | <span data-ttu-id="494cb-124">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="494cb-124">**-denorm**</span></span> | <span data-ttu-id="494cb-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="494cb-125">**-0**</span></span> | <span data-ttu-id="494cb-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="494cb-126">**+0**</span></span> | <span data-ttu-id="494cb-127">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="494cb-127">**+denorm**</span></span> | <span data-ttu-id="494cb-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="494cb-128">**+F**</span></span>     | <span data-ttu-id="494cb-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="494cb-129">**+inf**</span></span> | <span data-ttu-id="494cb-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="494cb-130">**Nan**</span></span> |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="494cb-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="494cb-131">**-inf**</span></span>            | <span data-ttu-id="494cb-132">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-132">-inf</span></span>     | <span data-ttu-id="494cb-133">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-133">-inf</span></span>       | <span data-ttu-id="494cb-134">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-134">-inf</span></span>        | <span data-ttu-id="494cb-135">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-135">-inf</span></span>   | <span data-ttu-id="494cb-136">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-136">-inf</span></span>   | <span data-ttu-id="494cb-137">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-137">-inf</span></span>        | <span data-ttu-id="494cb-138">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-138">-inf</span></span>       | <span data-ttu-id="494cb-139">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-139">NaN</span></span>      | <span data-ttu-id="494cb-140">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-140">NaN</span></span>     |
| <span data-ttu-id="494cb-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="494cb-141">**-F**</span></span>              | <span data-ttu-id="494cb-142">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-142">-inf</span></span>     | <span data-ttu-id="494cb-143">-F</span><span class="sxs-lookup"><span data-stu-id="494cb-143">-F</span></span>         | <span data-ttu-id="494cb-144">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-144">src0</span></span>        | <span data-ttu-id="494cb-145">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-145">src0</span></span>   | <span data-ttu-id="494cb-146">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-146">src0</span></span>   | <span data-ttu-id="494cb-147">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-147">src0</span></span>        | <span data-ttu-id="494cb-148">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="494cb-148">+-F or +-0</span></span> | <span data-ttu-id="494cb-149">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-149">+inf</span></span>     | <span data-ttu-id="494cb-150">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-150">NaN</span></span>     |
| <span data-ttu-id="494cb-151">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="494cb-151">**-denorm**</span></span>         | <span data-ttu-id="494cb-152">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-152">-inf</span></span>     | <span data-ttu-id="494cb-153">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-153">src1</span></span>       | <span data-ttu-id="494cb-154">-0</span><span class="sxs-lookup"><span data-stu-id="494cb-154">-0</span></span>          | <span data-ttu-id="494cb-155">-0</span><span class="sxs-lookup"><span data-stu-id="494cb-155">-0</span></span>     | <span data-ttu-id="494cb-156">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-156">+0</span></span>     | <span data-ttu-id="494cb-157">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-157">+0</span></span>          | <span data-ttu-id="494cb-158">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-158">src1</span></span>       | <span data-ttu-id="494cb-159">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-159">+inf</span></span>     | <span data-ttu-id="494cb-160">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-160">NaN</span></span>     |
| <span data-ttu-id="494cb-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="494cb-161">**-0**</span></span>              | <span data-ttu-id="494cb-162">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-162">-inf</span></span>     | <span data-ttu-id="494cb-163">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-163">src1</span></span>       | <span data-ttu-id="494cb-164">-0</span><span class="sxs-lookup"><span data-stu-id="494cb-164">-0</span></span>          | <span data-ttu-id="494cb-165">-0</span><span class="sxs-lookup"><span data-stu-id="494cb-165">-0</span></span>     | <span data-ttu-id="494cb-166">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-166">+0</span></span>     | <span data-ttu-id="494cb-167">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-167">+0</span></span>          | <span data-ttu-id="494cb-168">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-168">src1</span></span>       | <span data-ttu-id="494cb-169">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-169">+inf</span></span>     | <span data-ttu-id="494cb-170">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-170">NaN</span></span>     |
| <span data-ttu-id="494cb-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="494cb-171">**+0**</span></span>              | <span data-ttu-id="494cb-172">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-172">-inf</span></span>     | <span data-ttu-id="494cb-173">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-173">src1</span></span>       | <span data-ttu-id="494cb-174">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-174">+0</span></span>          | <span data-ttu-id="494cb-175">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-175">+0</span></span>     | <span data-ttu-id="494cb-176">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-176">+0</span></span>     | <span data-ttu-id="494cb-177">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-177">+0</span></span>          | <span data-ttu-id="494cb-178">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-178">src1</span></span>       | <span data-ttu-id="494cb-179">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-179">+inf</span></span>     | <span data-ttu-id="494cb-180">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-180">NaN</span></span>     |
| <span data-ttu-id="494cb-181">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="494cb-181">**+denorm**</span></span>         | <span data-ttu-id="494cb-182">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-182">-inf</span></span>     | <span data-ttu-id="494cb-183">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-183">src1</span></span>       | <span data-ttu-id="494cb-184">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-184">+0</span></span>          | <span data-ttu-id="494cb-185">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-185">+0</span></span>     | <span data-ttu-id="494cb-186">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-186">+0</span></span>     | <span data-ttu-id="494cb-187">+0</span><span class="sxs-lookup"><span data-stu-id="494cb-187">+0</span></span>          | <span data-ttu-id="494cb-188">src1</span><span class="sxs-lookup"><span data-stu-id="494cb-188">src1</span></span>       | <span data-ttu-id="494cb-189">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-189">+inf</span></span>     | <span data-ttu-id="494cb-190">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-190">NaN</span></span>     |
| <span data-ttu-id="494cb-191">**+F**</span><span class="sxs-lookup"><span data-stu-id="494cb-191">**+F**</span></span>              | <span data-ttu-id="494cb-192">-inf</span><span class="sxs-lookup"><span data-stu-id="494cb-192">-inf</span></span>     | <span data-ttu-id="494cb-193">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="494cb-193">+-F or +-0</span></span> | <span data-ttu-id="494cb-194">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-194">src0</span></span>        | <span data-ttu-id="494cb-195">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-195">src0</span></span>   | <span data-ttu-id="494cb-196">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-196">src0</span></span>   | <span data-ttu-id="494cb-197">src0</span><span class="sxs-lookup"><span data-stu-id="494cb-197">src0</span></span>        | <span data-ttu-id="494cb-198">+F</span><span class="sxs-lookup"><span data-stu-id="494cb-198">+F</span></span>         | <span data-ttu-id="494cb-199">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-199">+inf</span></span>     | <span data-ttu-id="494cb-200">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-200">NaN</span></span>     |
| <span data-ttu-id="494cb-201">**+inf**</span><span class="sxs-lookup"><span data-stu-id="494cb-201">**+inf**</span></span>            | <span data-ttu-id="494cb-202">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-202">NaN</span></span>      | <span data-ttu-id="494cb-203">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-203">+inf</span></span>       | <span data-ttu-id="494cb-204">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-204">+inf</span></span>        | <span data-ttu-id="494cb-205">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-205">+inf</span></span>   | <span data-ttu-id="494cb-206">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-206">+inf</span></span>   | <span data-ttu-id="494cb-207">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-207">+inf</span></span>        | <span data-ttu-id="494cb-208">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-208">+inf</span></span>       | <span data-ttu-id="494cb-209">+inf</span><span class="sxs-lookup"><span data-stu-id="494cb-209">+inf</span></span>     | <span data-ttu-id="494cb-210">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-210">NaN</span></span>     |
| <span data-ttu-id="494cb-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="494cb-211">**NaN**</span></span>             | <span data-ttu-id="494cb-212">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-212">NaN</span></span>      | <span data-ttu-id="494cb-213">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-213">NaN</span></span>        | <span data-ttu-id="494cb-214">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-214">NaN</span></span>         | <span data-ttu-id="494cb-215">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-215">NaN</span></span>    | <span data-ttu-id="494cb-216">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-216">NaN</span></span>    | <span data-ttu-id="494cb-217">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-217">NaN</span></span>         | <span data-ttu-id="494cb-218">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-218">NaN</span></span>        | <span data-ttu-id="494cb-219">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-219">NaN</span></span>      | <span data-ttu-id="494cb-220">NaN</span><span class="sxs-lookup"><span data-stu-id="494cb-220">NaN</span></span>     |



 

<span data-ttu-id="494cb-221">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="494cb-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="494cb-222">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="494cb-222">Vertex Shader</span></span> | <span data-ttu-id="494cb-223">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="494cb-223">Geometry Shader</span></span> | <span data-ttu-id="494cb-224">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="494cb-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="494cb-225">x</span><span class="sxs-lookup"><span data-stu-id="494cb-225">x</span></span>             | <span data-ttu-id="494cb-226">x</span><span class="sxs-lookup"><span data-stu-id="494cb-226">x</span></span>               | <span data-ttu-id="494cb-227">x</span><span class="sxs-lookup"><span data-stu-id="494cb-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="494cb-228">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="494cb-228">Minimum Shader Model</span></span>

<span data-ttu-id="494cb-229">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="494cb-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="494cb-230">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="494cb-230">Shader Model</span></span>                                              | <span data-ttu-id="494cb-231">Compatible</span><span class="sxs-lookup"><span data-stu-id="494cb-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="494cb-232">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="494cb-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="494cb-233">sí</span><span class="sxs-lookup"><span data-stu-id="494cb-233">yes</span></span>       |
| [<span data-ttu-id="494cb-234">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="494cb-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="494cb-235">sí</span><span class="sxs-lookup"><span data-stu-id="494cb-235">yes</span></span>       |
| [<span data-ttu-id="494cb-236">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="494cb-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="494cb-237">sí</span><span class="sxs-lookup"><span data-stu-id="494cb-237">yes</span></span>       |
| [<span data-ttu-id="494cb-238">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="494cb-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="494cb-239">no</span><span class="sxs-lookup"><span data-stu-id="494cb-239">no</span></span>        |
| [<span data-ttu-id="494cb-240">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="494cb-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="494cb-241">no</span><span class="sxs-lookup"><span data-stu-id="494cb-241">no</span></span>        |
| [<span data-ttu-id="494cb-242">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="494cb-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="494cb-243">no</span><span class="sxs-lookup"><span data-stu-id="494cb-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="494cb-244">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="494cb-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="494cb-245">Ensamblado del modelo de sombreador 4 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="494cb-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





