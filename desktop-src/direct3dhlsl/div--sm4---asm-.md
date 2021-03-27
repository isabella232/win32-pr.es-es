---
title: div (SM4-ASM)
description: División por componentes.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077088"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="b9976-103">div (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b9976-103">div (sm4 - asm)</span></span>

<span data-ttu-id="b9976-104">División por componentes.</span><span class="sxs-lookup"><span data-stu-id="b9976-104">Component-wise divide.</span></span>



| <span data-ttu-id="b9976-105">div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b9976-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b9976-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9976-106">Item</span></span>                                                            | <span data-ttu-id="b9976-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9976-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="b9976-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b9976-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b9976-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b9976-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="b9976-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b9976-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b9976-111">\[en \] el dividendo.</span><span class="sxs-lookup"><span data-stu-id="b9976-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="b9976-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="b9976-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b9976-113">\[en \] el divisor.</span><span class="sxs-lookup"><span data-stu-id="b9976-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="b9976-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9976-114">Remarks</span></span>

<span data-ttu-id="b9976-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="b9976-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="b9976-116">Tenga en cuenta las dos implementaciones permitidas de divide: a/b y a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="b9976-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="b9976-117">Un resultado de esto es que hay excepciones a la tabla siguiente para valores de denominador grandes (mayores que 8.5070592 e + 37), donde 1/denominador es una desnormativa.</span><span class="sxs-lookup"><span data-stu-id="b9976-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="b9976-118">Dado que las implementaciones pueden realizar una división como \* (1/b), en lugar de a/b directamente, y \[ un valor de 1/grande \] es una desnormativa que se puede vaciar, algunos casos de la tabla generarán resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="b9976-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="b9976-119">Por ejemplo, el valor de (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] puede producir Nan en algunas implementaciones, pero (+/-) inf en otras implementaciones</span><span class="sxs-lookup"><span data-stu-id="b9976-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="b9976-120">En esta tabla F se indica un número finito-real.</span><span class="sxs-lookup"><span data-stu-id="b9976-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="b9976-121">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="b9976-121">**src0 src1 ->**</span></span> | <span data-ttu-id="b9976-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b9976-122">**-inf**</span></span> | <span data-ttu-id="b9976-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="b9976-123">**-F**</span></span>     | <span data-ttu-id="b9976-124">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="b9976-124">**-denorm**</span></span> | <span data-ttu-id="b9976-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="b9976-125">**-0**</span></span> | <span data-ttu-id="b9976-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="b9976-126">**+0**</span></span> | <span data-ttu-id="b9976-127">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="b9976-127">**+denorm**</span></span> | <span data-ttu-id="b9976-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b9976-128">**+F**</span></span>     | <span data-ttu-id="b9976-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b9976-129">**+inf**</span></span> | <span data-ttu-id="b9976-130">**NError**</span><span class="sxs-lookup"><span data-stu-id="b9976-130">**Nan**</span></span> |
| <span data-ttu-id="b9976-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b9976-131">**-inf**</span></span>            | <span data-ttu-id="b9976-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-132">-inf</span></span>     | <span data-ttu-id="b9976-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-133">-inf</span></span>       | <span data-ttu-id="b9976-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-134">-inf</span></span>        | <span data-ttu-id="b9976-135">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-135">-inf</span></span>   | <span data-ttu-id="b9976-136">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-136">-inf</span></span>   | <span data-ttu-id="b9976-137">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-137">-inf</span></span>        | <span data-ttu-id="b9976-138">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-138">-inf</span></span>       | <span data-ttu-id="b9976-139">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-139">NaN</span></span>      | <span data-ttu-id="b9976-140">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-140">NaN</span></span>     |
| <span data-ttu-id="b9976-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="b9976-141">**-F**</span></span>              | <span data-ttu-id="b9976-142">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-142">-inf</span></span>     | <span data-ttu-id="b9976-143">-F</span><span class="sxs-lookup"><span data-stu-id="b9976-143">-F</span></span>         | <span data-ttu-id="b9976-144">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-144">src0</span></span>        | <span data-ttu-id="b9976-145">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-145">src0</span></span>   | <span data-ttu-id="b9976-146">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-146">src0</span></span>   | <span data-ttu-id="b9976-147">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-147">src0</span></span>        | <span data-ttu-id="b9976-148">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="b9976-148">+-F or +-0</span></span> | <span data-ttu-id="b9976-149">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-149">+inf</span></span>     | <span data-ttu-id="b9976-150">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-150">NaN</span></span>     |
| <span data-ttu-id="b9976-151">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="b9976-151">**-denorm**</span></span>         | <span data-ttu-id="b9976-152">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-152">-inf</span></span>     | <span data-ttu-id="b9976-153">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-153">src1</span></span>       | <span data-ttu-id="b9976-154">-0</span><span class="sxs-lookup"><span data-stu-id="b9976-154">-0</span></span>          | <span data-ttu-id="b9976-155">-0</span><span class="sxs-lookup"><span data-stu-id="b9976-155">-0</span></span>     | <span data-ttu-id="b9976-156">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-156">+0</span></span>     | <span data-ttu-id="b9976-157">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-157">+0</span></span>          | <span data-ttu-id="b9976-158">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-158">src1</span></span>       | <span data-ttu-id="b9976-159">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-159">+inf</span></span>     | <span data-ttu-id="b9976-160">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-160">NaN</span></span>     |
| <span data-ttu-id="b9976-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="b9976-161">**-0**</span></span>              | <span data-ttu-id="b9976-162">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-162">-inf</span></span>     | <span data-ttu-id="b9976-163">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-163">src1</span></span>       | <span data-ttu-id="b9976-164">-0</span><span class="sxs-lookup"><span data-stu-id="b9976-164">-0</span></span>          | <span data-ttu-id="b9976-165">-0</span><span class="sxs-lookup"><span data-stu-id="b9976-165">-0</span></span>     | <span data-ttu-id="b9976-166">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-166">+0</span></span>     | <span data-ttu-id="b9976-167">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-167">+0</span></span>          | <span data-ttu-id="b9976-168">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-168">src1</span></span>       | <span data-ttu-id="b9976-169">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-169">+inf</span></span>     | <span data-ttu-id="b9976-170">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-170">NaN</span></span>     |
| <span data-ttu-id="b9976-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="b9976-171">**+0**</span></span>              | <span data-ttu-id="b9976-172">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-172">-inf</span></span>     | <span data-ttu-id="b9976-173">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-173">src1</span></span>       | <span data-ttu-id="b9976-174">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-174">+0</span></span>          | <span data-ttu-id="b9976-175">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-175">+0</span></span>     | <span data-ttu-id="b9976-176">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-176">+0</span></span>     | <span data-ttu-id="b9976-177">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-177">+0</span></span>          | <span data-ttu-id="b9976-178">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-178">src1</span></span>       | <span data-ttu-id="b9976-179">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-179">+inf</span></span>     | <span data-ttu-id="b9976-180">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-180">NaN</span></span>     |
| <span data-ttu-id="b9976-181">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="b9976-181">**+denorm**</span></span>         | <span data-ttu-id="b9976-182">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-182">-inf</span></span>     | <span data-ttu-id="b9976-183">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-183">src1</span></span>       | <span data-ttu-id="b9976-184">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-184">+0</span></span>          | <span data-ttu-id="b9976-185">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-185">+0</span></span>     | <span data-ttu-id="b9976-186">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-186">+0</span></span>     | <span data-ttu-id="b9976-187">+0</span><span class="sxs-lookup"><span data-stu-id="b9976-187">+0</span></span>          | <span data-ttu-id="b9976-188">src1</span><span class="sxs-lookup"><span data-stu-id="b9976-188">src1</span></span>       | <span data-ttu-id="b9976-189">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-189">+inf</span></span>     | <span data-ttu-id="b9976-190">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-190">NaN</span></span>     |
| <span data-ttu-id="b9976-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b9976-191">**+F**</span></span>              | <span data-ttu-id="b9976-192">-inf</span><span class="sxs-lookup"><span data-stu-id="b9976-192">-inf</span></span>     | <span data-ttu-id="b9976-193">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="b9976-193">+-F or +-0</span></span> | <span data-ttu-id="b9976-194">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-194">src0</span></span>        | <span data-ttu-id="b9976-195">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-195">src0</span></span>   | <span data-ttu-id="b9976-196">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-196">src0</span></span>   | <span data-ttu-id="b9976-197">src0</span><span class="sxs-lookup"><span data-stu-id="b9976-197">src0</span></span>        | <span data-ttu-id="b9976-198">+F</span><span class="sxs-lookup"><span data-stu-id="b9976-198">+F</span></span>         | <span data-ttu-id="b9976-199">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-199">+inf</span></span>     | <span data-ttu-id="b9976-200">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-200">NaN</span></span>     |
| <span data-ttu-id="b9976-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b9976-201">**+inf**</span></span>            | <span data-ttu-id="b9976-202">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-202">NaN</span></span>      | <span data-ttu-id="b9976-203">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-203">+inf</span></span>       | <span data-ttu-id="b9976-204">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-204">+inf</span></span>        | <span data-ttu-id="b9976-205">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-205">+inf</span></span>   | <span data-ttu-id="b9976-206">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-206">+inf</span></span>   | <span data-ttu-id="b9976-207">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-207">+inf</span></span>        | <span data-ttu-id="b9976-208">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-208">+inf</span></span>       | <span data-ttu-id="b9976-209">+inf</span><span class="sxs-lookup"><span data-stu-id="b9976-209">+inf</span></span>     | <span data-ttu-id="b9976-210">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-210">NaN</span></span>     |
| <span data-ttu-id="b9976-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b9976-211">**NaN**</span></span>             | <span data-ttu-id="b9976-212">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-212">NaN</span></span>      | <span data-ttu-id="b9976-213">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-213">NaN</span></span>        | <span data-ttu-id="b9976-214">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-214">NaN</span></span>         | <span data-ttu-id="b9976-215">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-215">NaN</span></span>    | <span data-ttu-id="b9976-216">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-216">NaN</span></span>    | <span data-ttu-id="b9976-217">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-217">NaN</span></span>         | <span data-ttu-id="b9976-218">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-218">NaN</span></span>        | <span data-ttu-id="b9976-219">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-219">NaN</span></span>      | <span data-ttu-id="b9976-220">NaN</span><span class="sxs-lookup"><span data-stu-id="b9976-220">NaN</span></span>     |



 

<span data-ttu-id="b9976-221">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="b9976-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b9976-222">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b9976-222">Vertex Shader</span></span> | <span data-ttu-id="b9976-223">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="b9976-223">Geometry Shader</span></span> | <span data-ttu-id="b9976-224">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b9976-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b9976-225">x</span><span class="sxs-lookup"><span data-stu-id="b9976-225">x</span></span>             | <span data-ttu-id="b9976-226">x</span><span class="sxs-lookup"><span data-stu-id="b9976-226">x</span></span>               | <span data-ttu-id="b9976-227">x</span><span class="sxs-lookup"><span data-stu-id="b9976-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b9976-228">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b9976-228">Minimum Shader Model</span></span>

<span data-ttu-id="b9976-229">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b9976-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b9976-230">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b9976-230">Shader Model</span></span>                                              | <span data-ttu-id="b9976-231">Compatible</span><span class="sxs-lookup"><span data-stu-id="b9976-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b9976-232">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b9976-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b9976-233">sí</span><span class="sxs-lookup"><span data-stu-id="b9976-233">yes</span></span>       |
| [<span data-ttu-id="b9976-234">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b9976-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b9976-235">sí</span><span class="sxs-lookup"><span data-stu-id="b9976-235">yes</span></span>       |
| [<span data-ttu-id="b9976-236">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b9976-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b9976-237">sí</span><span class="sxs-lookup"><span data-stu-id="b9976-237">yes</span></span>       |
| [<span data-ttu-id="b9976-238">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9976-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b9976-239">no</span><span class="sxs-lookup"><span data-stu-id="b9976-239">no</span></span>        |
| [<span data-ttu-id="b9976-240">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9976-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b9976-241">no</span><span class="sxs-lookup"><span data-stu-id="b9976-241">no</span></span>        |
| [<span data-ttu-id="b9976-242">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9976-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b9976-243">no</span><span class="sxs-lookup"><span data-stu-id="b9976-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b9976-244">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9976-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9976-245">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9976-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





