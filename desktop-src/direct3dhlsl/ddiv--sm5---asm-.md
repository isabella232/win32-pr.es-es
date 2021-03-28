---
title: DDIV (SM5-ASM)
description: Calcula una división de doble precisión para componentes.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996876"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="62688-103">DDIV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="62688-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="62688-104">Calcula una división de doble precisión para componentes.</span><span class="sxs-lookup"><span data-stu-id="62688-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="62688-105">DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="62688-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="62688-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="62688-106">Item</span></span>                                                            | <span data-ttu-id="62688-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="62688-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62688-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="62688-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="62688-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="62688-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="62688-110">El valor del resultado debe ser preciso para 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="62688-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="62688-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="62688-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="62688-112">\[en \] el dividendo.</span><span class="sxs-lookup"><span data-stu-id="62688-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="62688-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="62688-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="62688-114">\[en \] el divisor.</span><span class="sxs-lookup"><span data-stu-id="62688-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="62688-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62688-115">Remarks</span></span>

<span data-ttu-id="62688-116">El compilador de HLSL emitirá la instrucción DDIV siempre que el operador de división se use con valores double.</span><span class="sxs-lookup"><span data-stu-id="62688-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="62688-117">Será necesario que la precisión de esta instrucción sea 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="62688-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="62688-118">Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se puedan enlazar a menos que se cumplan todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="62688-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="62688-119">El sistema admite DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="62688-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="62688-120">El sistema incluye un controlador WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="62688-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="62688-121">El controlador informa de la compatibilidad con esta instrucción a través de **\_ las opciones de D3D11 de datos de características de D3D11 \_ \_ \_ . ExtendedDoublesShaderInstructions** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="62688-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="62688-122">En la tabla siguiente se muestran los resultados btained al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="62688-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="62688-123">En esta tabla F se indica un número finito-real.</span><span class="sxs-lookup"><span data-stu-id="62688-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="62688-124">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="62688-124">**src0 src1 ->**</span></span> | <span data-ttu-id="62688-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="62688-125">**-inf**</span></span> | <span data-ttu-id="62688-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="62688-126">**-F**</span></span> | <span data-ttu-id="62688-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="62688-127">**-1.0**</span></span> | <span data-ttu-id="62688-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="62688-128">**-0**</span></span> | <span data-ttu-id="62688-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="62688-129">**+0**</span></span> | <span data-ttu-id="62688-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="62688-130">**+1.0**</span></span> | <span data-ttu-id="62688-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="62688-131">**+F**</span></span> | <span data-ttu-id="62688-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="62688-132">**+inf**</span></span> | <span data-ttu-id="62688-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="62688-133">**NaN**</span></span> |
| <span data-ttu-id="62688-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="62688-134">**-inf**</span></span>            | <span data-ttu-id="62688-135">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-135">NaN</span></span>      | <span data-ttu-id="62688-136">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-136">+inf</span></span>   | <span data-ttu-id="62688-137">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-137">+inf</span></span>     | <span data-ttu-id="62688-138">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-138">+inf</span></span>   | <span data-ttu-id="62688-139">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-139">-inf</span></span>   | <span data-ttu-id="62688-140">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-140">-inf</span></span>     | <span data-ttu-id="62688-141">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-141">-inf</span></span>   | <span data-ttu-id="62688-142">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-142">NaN</span></span>      | <span data-ttu-id="62688-143">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-143">NaN</span></span>     |
| <span data-ttu-id="62688-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="62688-144">**-F**</span></span>              | <span data-ttu-id="62688-145">+0</span><span class="sxs-lookup"><span data-stu-id="62688-145">+0</span></span>       | <span data-ttu-id="62688-146">+F</span><span class="sxs-lookup"><span data-stu-id="62688-146">+F</span></span>     | <span data-ttu-id="62688-147">-src0</span><span class="sxs-lookup"><span data-stu-id="62688-147">-src0</span></span>    | <span data-ttu-id="62688-148">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-148">+inf</span></span>   | <span data-ttu-id="62688-149">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-149">-inf</span></span>   | <span data-ttu-id="62688-150">src0</span><span class="sxs-lookup"><span data-stu-id="62688-150">src0</span></span>     | <span data-ttu-id="62688-151">-F</span><span class="sxs-lookup"><span data-stu-id="62688-151">-F</span></span>     | <span data-ttu-id="62688-152">-0</span><span class="sxs-lookup"><span data-stu-id="62688-152">-0</span></span>       | <span data-ttu-id="62688-153">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-153">NaN</span></span>     |
| <span data-ttu-id="62688-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="62688-154">**-0**</span></span>              | <span data-ttu-id="62688-155">+0</span><span class="sxs-lookup"><span data-stu-id="62688-155">+0</span></span>       | <span data-ttu-id="62688-156">+0</span><span class="sxs-lookup"><span data-stu-id="62688-156">+0</span></span>     | <span data-ttu-id="62688-157">+0</span><span class="sxs-lookup"><span data-stu-id="62688-157">+0</span></span>       | <span data-ttu-id="62688-158">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-158">NaN</span></span>    | <span data-ttu-id="62688-159">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-159">NaN</span></span>    | <span data-ttu-id="62688-160">-0</span><span class="sxs-lookup"><span data-stu-id="62688-160">-0</span></span>       | <span data-ttu-id="62688-161">-0</span><span class="sxs-lookup"><span data-stu-id="62688-161">-0</span></span>     | <span data-ttu-id="62688-162">-0</span><span class="sxs-lookup"><span data-stu-id="62688-162">-0</span></span>       | <span data-ttu-id="62688-163">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-163">NaN</span></span>     |
| <span data-ttu-id="62688-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="62688-164">**+0**</span></span>              | <span data-ttu-id="62688-165">-0</span><span class="sxs-lookup"><span data-stu-id="62688-165">-0</span></span>       | <span data-ttu-id="62688-166">-0</span><span class="sxs-lookup"><span data-stu-id="62688-166">-0</span></span>     | <span data-ttu-id="62688-167">-0</span><span class="sxs-lookup"><span data-stu-id="62688-167">-0</span></span>       | <span data-ttu-id="62688-168">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-168">NaN</span></span>    | <span data-ttu-id="62688-169">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-169">NaN</span></span>    | <span data-ttu-id="62688-170">+0</span><span class="sxs-lookup"><span data-stu-id="62688-170">+0</span></span>       | <span data-ttu-id="62688-171">+0</span><span class="sxs-lookup"><span data-stu-id="62688-171">+0</span></span>     | <span data-ttu-id="62688-172">+0</span><span class="sxs-lookup"><span data-stu-id="62688-172">+0</span></span>       | <span data-ttu-id="62688-173">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-173">NaN</span></span>     |
| <span data-ttu-id="62688-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="62688-174">**+F**</span></span>              | <span data-ttu-id="62688-175">-0</span><span class="sxs-lookup"><span data-stu-id="62688-175">-0</span></span>       | <span data-ttu-id="62688-176">-F</span><span class="sxs-lookup"><span data-stu-id="62688-176">-F</span></span>     | <span data-ttu-id="62688-177">-src0</span><span class="sxs-lookup"><span data-stu-id="62688-177">-src0</span></span>    | <span data-ttu-id="62688-178">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-178">-inf</span></span>   | <span data-ttu-id="62688-179">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-179">+inf</span></span>   | <span data-ttu-id="62688-180">src0</span><span class="sxs-lookup"><span data-stu-id="62688-180">src0</span></span>     | <span data-ttu-id="62688-181">+F</span><span class="sxs-lookup"><span data-stu-id="62688-181">+F</span></span>     | <span data-ttu-id="62688-182">+0</span><span class="sxs-lookup"><span data-stu-id="62688-182">+0</span></span>       | <span data-ttu-id="62688-183">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-183">NaN</span></span>     |
| <span data-ttu-id="62688-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="62688-184">**+inf**</span></span>            | <span data-ttu-id="62688-185">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-185">NaN</span></span>      | <span data-ttu-id="62688-186">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-186">-inf</span></span>   | <span data-ttu-id="62688-187">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-187">-inf</span></span>     | <span data-ttu-id="62688-188">-inf</span><span class="sxs-lookup"><span data-stu-id="62688-188">-inf</span></span>   | <span data-ttu-id="62688-189">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-189">+inf</span></span>   | <span data-ttu-id="62688-190">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-190">+inf</span></span>     | <span data-ttu-id="62688-191">+inf</span><span class="sxs-lookup"><span data-stu-id="62688-191">+inf</span></span>   | <span data-ttu-id="62688-192">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-192">NaN</span></span>      | <span data-ttu-id="62688-193">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-193">NaN</span></span>     |
| <span data-ttu-id="62688-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="62688-194">**NaN**</span></span>             | <span data-ttu-id="62688-195">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-195">NaN</span></span>      | <span data-ttu-id="62688-196">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-196">NaN</span></span>    | <span data-ttu-id="62688-197">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-197">NaN</span></span>      | <span data-ttu-id="62688-198">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-198">NaN</span></span>    | <span data-ttu-id="62688-199">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-199">NaN</span></span>    | <span data-ttu-id="62688-200">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-200">NaN</span></span>      | <span data-ttu-id="62688-201">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-201">NaN</span></span>    | <span data-ttu-id="62688-202">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-202">NaN</span></span>      | <span data-ttu-id="62688-203">NaN</span><span class="sxs-lookup"><span data-stu-id="62688-203">NaN</span></span>     |



 

<span data-ttu-id="62688-204">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="62688-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="62688-205">Vértice</span><span class="sxs-lookup"><span data-stu-id="62688-205">Vertex</span></span> | <span data-ttu-id="62688-206">Casco</span><span class="sxs-lookup"><span data-stu-id="62688-206">Hull</span></span> | <span data-ttu-id="62688-207">Dominio</span><span class="sxs-lookup"><span data-stu-id="62688-207">Domain</span></span> | <span data-ttu-id="62688-208">Geometría</span><span class="sxs-lookup"><span data-stu-id="62688-208">Geometry</span></span> | <span data-ttu-id="62688-209">Píxel</span><span class="sxs-lookup"><span data-stu-id="62688-209">Pixel</span></span> | <span data-ttu-id="62688-210">Compute</span><span class="sxs-lookup"><span data-stu-id="62688-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="62688-211">X</span><span class="sxs-lookup"><span data-stu-id="62688-211">X</span></span>      | <span data-ttu-id="62688-212">X</span><span class="sxs-lookup"><span data-stu-id="62688-212">X</span></span>    | <span data-ttu-id="62688-213">X</span><span class="sxs-lookup"><span data-stu-id="62688-213">X</span></span>      | <span data-ttu-id="62688-214">X</span><span class="sxs-lookup"><span data-stu-id="62688-214">X</span></span>        | <span data-ttu-id="62688-215">X</span><span class="sxs-lookup"><span data-stu-id="62688-215">X</span></span>     | <span data-ttu-id="62688-216">X</span><span class="sxs-lookup"><span data-stu-id="62688-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="62688-217">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="62688-217">Minimum Shader Model</span></span>

<span data-ttu-id="62688-218">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="62688-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="62688-219">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="62688-219">Shader Model</span></span>                                              | <span data-ttu-id="62688-220">Compatible</span><span class="sxs-lookup"><span data-stu-id="62688-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="62688-221">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="62688-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="62688-222">sí</span><span class="sxs-lookup"><span data-stu-id="62688-222">yes</span></span>       |
| [<span data-ttu-id="62688-223">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="62688-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="62688-224">no</span><span class="sxs-lookup"><span data-stu-id="62688-224">no</span></span>        |
| [<span data-ttu-id="62688-225">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="62688-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="62688-226">no</span><span class="sxs-lookup"><span data-stu-id="62688-226">no</span></span>        |
| [<span data-ttu-id="62688-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62688-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="62688-228">no</span><span class="sxs-lookup"><span data-stu-id="62688-228">no</span></span>        |
| [<span data-ttu-id="62688-229">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62688-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="62688-230">no</span><span class="sxs-lookup"><span data-stu-id="62688-230">no</span></span>        |
| [<span data-ttu-id="62688-231">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62688-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="62688-232">no</span><span class="sxs-lookup"><span data-stu-id="62688-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="62688-233">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62688-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62688-234">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62688-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





