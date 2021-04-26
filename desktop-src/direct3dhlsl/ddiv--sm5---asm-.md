---
title: ddiv (sm5 - asm)
description: Calcula una división de precisión doble por componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999162"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="7dd0d-103">ddiv (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="7dd0d-104">Calcula una división de precisión doble por componente.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="7dd0d-105">ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swdivle \] \[ - \] src1 \[ \_ abs \] \[ .swdivle\]</span><span class="sxs-lookup"><span data-stu-id="7dd0d-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7dd0d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7dd0d-106">Item</span></span>                                                            | <span data-ttu-id="7dd0d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dd0d-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd0d-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="7dd0d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7dd0d-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="7dd0d-110">El valor del resultado debe ser preciso a 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="7dd0d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7dd0d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7dd0d-112">\[en \] El dividendo.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="7dd0d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7dd0d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7dd0d-114">\[en \] el divisor.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="7dd0d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dd0d-115">Remarks</span></span>

<span data-ttu-id="7dd0d-116">El compilador HLSL emitirá la instrucción DDIV cada vez que se utilice el operador de división con doubles.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="7dd0d-117">La precisión de esta instrucción será de 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="7dd0d-118">Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se enlacen a menos que se cumplen todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="7dd0d-119">El sistema admite DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="7dd0d-120">El sistema incluye un controlador WDDM 1.2.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="7dd0d-121">El controlador informa de la compatibilidad con esta instrucción a través de **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** establecido en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="7dd0d-122">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="7dd0d-123">En esta tabla, F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="7dd0d-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="7dd0d-124">**src0 src1 ->**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-124">**src0 src1 ->**</span></span> | <span data-ttu-id="7dd0d-125">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-125">**-inf**</span></span> | <span data-ttu-id="7dd0d-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-126">**-F**</span></span> | <span data-ttu-id="7dd0d-127">**-1.0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-127">**-1.0**</span></span> | <span data-ttu-id="7dd0d-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-128">**-0**</span></span> | <span data-ttu-id="7dd0d-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-129">**+0**</span></span> | <span data-ttu-id="7dd0d-130">**+1.0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-130">**+1.0**</span></span> | <span data-ttu-id="7dd0d-131">**+F**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-131">**+F**</span></span> | <span data-ttu-id="7dd0d-132">**+inf**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-132">**+inf**</span></span> | <span data-ttu-id="7dd0d-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="7dd0d-134">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-134">**-inf**</span></span>            | <span data-ttu-id="7dd0d-135">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-135">NaN</span></span>      | <span data-ttu-id="7dd0d-136">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-136">+inf</span></span>   | <span data-ttu-id="7dd0d-137">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-137">+inf</span></span>     | <span data-ttu-id="7dd0d-138">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-138">+inf</span></span>   | <span data-ttu-id="7dd0d-139">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-139">-inf</span></span>   | <span data-ttu-id="7dd0d-140">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-140">-inf</span></span>     | <span data-ttu-id="7dd0d-141">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-141">-inf</span></span>   | <span data-ttu-id="7dd0d-142">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-142">NaN</span></span>      | <span data-ttu-id="7dd0d-143">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-143">NaN</span></span>     |
| <span data-ttu-id="7dd0d-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-144">**-F**</span></span>              | <span data-ttu-id="7dd0d-145">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-145">+0</span></span>       | <span data-ttu-id="7dd0d-146">+F</span><span class="sxs-lookup"><span data-stu-id="7dd0d-146">+F</span></span>     | <span data-ttu-id="7dd0d-147">-src0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-147">-src0</span></span>    | <span data-ttu-id="7dd0d-148">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-148">+inf</span></span>   | <span data-ttu-id="7dd0d-149">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-149">-inf</span></span>   | <span data-ttu-id="7dd0d-150">src0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-150">src0</span></span>     | <span data-ttu-id="7dd0d-151">-F</span><span class="sxs-lookup"><span data-stu-id="7dd0d-151">-F</span></span>     | <span data-ttu-id="7dd0d-152">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-152">-0</span></span>       | <span data-ttu-id="7dd0d-153">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-153">NaN</span></span>     |
| <span data-ttu-id="7dd0d-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-154">**-0**</span></span>              | <span data-ttu-id="7dd0d-155">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-155">+0</span></span>       | <span data-ttu-id="7dd0d-156">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-156">+0</span></span>     | <span data-ttu-id="7dd0d-157">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-157">+0</span></span>       | <span data-ttu-id="7dd0d-158">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-158">NaN</span></span>    | <span data-ttu-id="7dd0d-159">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-159">NaN</span></span>    | <span data-ttu-id="7dd0d-160">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-160">-0</span></span>       | <span data-ttu-id="7dd0d-161">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-161">-0</span></span>     | <span data-ttu-id="7dd0d-162">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-162">-0</span></span>       | <span data-ttu-id="7dd0d-163">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-163">NaN</span></span>     |
| <span data-ttu-id="7dd0d-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-164">**+0**</span></span>              | <span data-ttu-id="7dd0d-165">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-165">-0</span></span>       | <span data-ttu-id="7dd0d-166">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-166">-0</span></span>     | <span data-ttu-id="7dd0d-167">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-167">-0</span></span>       | <span data-ttu-id="7dd0d-168">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-168">NaN</span></span>    | <span data-ttu-id="7dd0d-169">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-169">NaN</span></span>    | <span data-ttu-id="7dd0d-170">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-170">+0</span></span>       | <span data-ttu-id="7dd0d-171">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-171">+0</span></span>     | <span data-ttu-id="7dd0d-172">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-172">+0</span></span>       | <span data-ttu-id="7dd0d-173">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-173">NaN</span></span>     |
| <span data-ttu-id="7dd0d-174">**+F**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-174">**+F**</span></span>              | <span data-ttu-id="7dd0d-175">-0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-175">-0</span></span>       | <span data-ttu-id="7dd0d-176">-F</span><span class="sxs-lookup"><span data-stu-id="7dd0d-176">-F</span></span>     | <span data-ttu-id="7dd0d-177">-src0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-177">-src0</span></span>    | <span data-ttu-id="7dd0d-178">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-178">-inf</span></span>   | <span data-ttu-id="7dd0d-179">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-179">+inf</span></span>   | <span data-ttu-id="7dd0d-180">src0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-180">src0</span></span>     | <span data-ttu-id="7dd0d-181">+F</span><span class="sxs-lookup"><span data-stu-id="7dd0d-181">+F</span></span>     | <span data-ttu-id="7dd0d-182">+0</span><span class="sxs-lookup"><span data-stu-id="7dd0d-182">+0</span></span>       | <span data-ttu-id="7dd0d-183">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-183">NaN</span></span>     |
| <span data-ttu-id="7dd0d-184">**+inf**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-184">**+inf**</span></span>            | <span data-ttu-id="7dd0d-185">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-185">NaN</span></span>      | <span data-ttu-id="7dd0d-186">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-186">-inf</span></span>   | <span data-ttu-id="7dd0d-187">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-187">-inf</span></span>     | <span data-ttu-id="7dd0d-188">-inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-188">-inf</span></span>   | <span data-ttu-id="7dd0d-189">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-189">+inf</span></span>   | <span data-ttu-id="7dd0d-190">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-190">+inf</span></span>     | <span data-ttu-id="7dd0d-191">+inf</span><span class="sxs-lookup"><span data-stu-id="7dd0d-191">+inf</span></span>   | <span data-ttu-id="7dd0d-192">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-192">NaN</span></span>      | <span data-ttu-id="7dd0d-193">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-193">NaN</span></span>     |
| <span data-ttu-id="7dd0d-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7dd0d-194">**NaN**</span></span>             | <span data-ttu-id="7dd0d-195">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-195">NaN</span></span>      | <span data-ttu-id="7dd0d-196">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-196">NaN</span></span>    | <span data-ttu-id="7dd0d-197">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-197">NaN</span></span>      | <span data-ttu-id="7dd0d-198">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-198">NaN</span></span>    | <span data-ttu-id="7dd0d-199">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-199">NaN</span></span>    | <span data-ttu-id="7dd0d-200">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-200">NaN</span></span>      | <span data-ttu-id="7dd0d-201">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-201">NaN</span></span>    | <span data-ttu-id="7dd0d-202">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-202">NaN</span></span>      | <span data-ttu-id="7dd0d-203">NaN</span><span class="sxs-lookup"><span data-stu-id="7dd0d-203">NaN</span></span>     |



 

<span data-ttu-id="7dd0d-204">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7dd0d-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7dd0d-205">Vértice</span><span class="sxs-lookup"><span data-stu-id="7dd0d-205">Vertex</span></span> | <span data-ttu-id="7dd0d-206">Casco</span><span class="sxs-lookup"><span data-stu-id="7dd0d-206">Hull</span></span> | <span data-ttu-id="7dd0d-207">Domain</span><span class="sxs-lookup"><span data-stu-id="7dd0d-207">Domain</span></span> | <span data-ttu-id="7dd0d-208">Geometría</span><span class="sxs-lookup"><span data-stu-id="7dd0d-208">Geometry</span></span> | <span data-ttu-id="7dd0d-209">Píxel</span><span class="sxs-lookup"><span data-stu-id="7dd0d-209">Pixel</span></span> | <span data-ttu-id="7dd0d-210">Proceso</span><span class="sxs-lookup"><span data-stu-id="7dd0d-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7dd0d-211">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-211">X</span></span>      | <span data-ttu-id="7dd0d-212">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-212">X</span></span>    | <span data-ttu-id="7dd0d-213">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-213">X</span></span>      | <span data-ttu-id="7dd0d-214">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-214">X</span></span>        | <span data-ttu-id="7dd0d-215">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-215">X</span></span>     | <span data-ttu-id="7dd0d-216">X</span><span class="sxs-lookup"><span data-stu-id="7dd0d-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7dd0d-217">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7dd0d-217">Minimum Shader Model</span></span>

<span data-ttu-id="7dd0d-218">Esta instrucción se admite en los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7dd0d-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7dd0d-219">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7dd0d-219">Shader Model</span></span>                                              | <span data-ttu-id="7dd0d-220">Compatible</span><span class="sxs-lookup"><span data-stu-id="7dd0d-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7dd0d-221">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="7dd0d-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7dd0d-222">sí</span><span class="sxs-lookup"><span data-stu-id="7dd0d-222">yes</span></span>       |
| [<span data-ttu-id="7dd0d-223">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="7dd0d-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7dd0d-224">no</span><span class="sxs-lookup"><span data-stu-id="7dd0d-224">no</span></span>        |
| [<span data-ttu-id="7dd0d-225">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="7dd0d-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7dd0d-226">no</span><span class="sxs-lookup"><span data-stu-id="7dd0d-226">no</span></span>        |
| [<span data-ttu-id="7dd0d-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7dd0d-228">no</span><span class="sxs-lookup"><span data-stu-id="7dd0d-228">no</span></span>        |
| [<span data-ttu-id="7dd0d-229">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7dd0d-230">no</span><span class="sxs-lookup"><span data-stu-id="7dd0d-230">no</span></span>        |
| [<span data-ttu-id="7dd0d-231">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7dd0d-232">no</span><span class="sxs-lookup"><span data-stu-id="7dd0d-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7dd0d-233">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dd0d-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dd0d-234">Ensamblado del modelo de sombreador 5 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="7dd0d-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





