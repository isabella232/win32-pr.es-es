---
title: Dadd (SM5-ASM)
description: Agregación de doble precisión para componentes.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419892"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="65254-103">Dadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="65254-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="65254-104">Agregación de doble precisión para componentes.</span><span class="sxs-lookup"><span data-stu-id="65254-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="65254-105">Dadd \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="65254-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="65254-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="65254-106">Item</span></span>                                                            | <span data-ttu-id="65254-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="65254-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="65254-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="65254-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="65254-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="65254-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="65254-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="65254-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="65254-111">\[en \] los componentes que se van a agregar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="65254-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="65254-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="65254-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="65254-113">\[en \] los componentes que se van a agregar con *src0*</span><span class="sxs-lookup"><span data-stu-id="65254-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="65254-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65254-114">Remarks</span></span>

<span data-ttu-id="65254-115">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="65254-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="65254-116">Las máscaras de *destino* válidas son. XY,. ZW y. xyzw.</span><span class="sxs-lookup"><span data-stu-id="65254-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="65254-117">Las siguientes asignaciones son posteriores a swizzle:</span><span class="sxs-lookup"><span data-stu-id="65254-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="65254-118">*dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="65254-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="65254-119">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="65254-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="65254-120">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="65254-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="65254-121">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="65254-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="65254-122">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="65254-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="65254-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="65254-123"><strong>src0</strong></span></span><br /><span data-ttu-id="65254-124">
<strong>SRC1-></strong></span><span class="sxs-lookup"><span data-stu-id="65254-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="65254-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="65254-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="65254-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="65254-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="65254-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="65254-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="65254-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="65254-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="65254-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="65254-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="65254-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="65254-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="65254-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="65254-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65254-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="65254-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="65254-133">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-133">-inf</span></span></td>
<td><span data-ttu-id="65254-134">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-134">-inf</span></span></td>
<td><span data-ttu-id="65254-135">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-135">-inf</span></span></td>
<td><span data-ttu-id="65254-136">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-136">-inf</span></span></td>
<td><span data-ttu-id="65254-137">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-137">-inf</span></span></td>
<td><span data-ttu-id="65254-138">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-138">NaN</span></span></td>
<td><span data-ttu-id="65254-139">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65254-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="65254-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="65254-141">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-141">-inf</span></span></td>
<td><span data-ttu-id="65254-142">-F</span><span class="sxs-lookup"><span data-stu-id="65254-142">-F</span></span></td>
<td><span data-ttu-id="65254-143">src0</span><span class="sxs-lookup"><span data-stu-id="65254-143">src0</span></span></td>
<td><span data-ttu-id="65254-144">src0</span><span class="sxs-lookup"><span data-stu-id="65254-144">src0</span></span></td>
<td><span data-ttu-id="65254-145">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="65254-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="65254-146">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-146">+inf</span></span></td>
<td><span data-ttu-id="65254-147">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65254-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="65254-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="65254-149">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-149">-inf</span></span></td>
<td><span data-ttu-id="65254-150">src1</span><span class="sxs-lookup"><span data-stu-id="65254-150">src1</span></span></td>
<td><span data-ttu-id="65254-151">-0</span><span class="sxs-lookup"><span data-stu-id="65254-151">-0</span></span></td>
<td><span data-ttu-id="65254-152">+0</span><span class="sxs-lookup"><span data-stu-id="65254-152">+0</span></span></td>
<td><span data-ttu-id="65254-153">src1</span><span class="sxs-lookup"><span data-stu-id="65254-153">src1</span></span></td>
<td><span data-ttu-id="65254-154">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-154">+inf</span></span></td>
<td><span data-ttu-id="65254-155">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65254-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="65254-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="65254-157">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-157">-inf</span></span></td>
<td><span data-ttu-id="65254-158">src1</span><span class="sxs-lookup"><span data-stu-id="65254-158">src1</span></span></td>
<td><span data-ttu-id="65254-159">+0</span><span class="sxs-lookup"><span data-stu-id="65254-159">+0</span></span></td>
<td><span data-ttu-id="65254-160">+0</span><span class="sxs-lookup"><span data-stu-id="65254-160">+0</span></span></td>
<td><span data-ttu-id="65254-161">src1</span><span class="sxs-lookup"><span data-stu-id="65254-161">src1</span></span></td>
<td><span data-ttu-id="65254-162">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-162">+inf</span></span></td>
<td><span data-ttu-id="65254-163">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65254-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="65254-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="65254-165">-inf</span><span class="sxs-lookup"><span data-stu-id="65254-165">-inf</span></span></td>
<td><span data-ttu-id="65254-166">+-F o +-0</span><span class="sxs-lookup"><span data-stu-id="65254-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="65254-167">src0</span><span class="sxs-lookup"><span data-stu-id="65254-167">src0</span></span></td>
<td><span data-ttu-id="65254-168">src0</span><span class="sxs-lookup"><span data-stu-id="65254-168">src0</span></span></td>
<td><span data-ttu-id="65254-169">+F</span><span class="sxs-lookup"><span data-stu-id="65254-169">+F</span></span></td>
<td><span data-ttu-id="65254-170">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-170">+inf</span></span></td>
<td><span data-ttu-id="65254-171">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65254-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="65254-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="65254-173">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-173">NaN</span></span></td>
<td><span data-ttu-id="65254-174">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-174">+inf</span></span></td>
<td><span data-ttu-id="65254-175">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-175">+inf</span></span></td>
<td><span data-ttu-id="65254-176">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-176">+inf</span></span></td>
<td><span data-ttu-id="65254-177">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-177">+inf</span></span></td>
<td><span data-ttu-id="65254-178">+inf</span><span class="sxs-lookup"><span data-stu-id="65254-178">+inf</span></span></td>
<td><span data-ttu-id="65254-179">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65254-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="65254-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="65254-181">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-181">NaN</span></span></td>
<td><span data-ttu-id="65254-182">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-182">NaN</span></span></td>
<td><span data-ttu-id="65254-183">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-183">NaN</span></span></td>
<td><span data-ttu-id="65254-184">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-184">NaN</span></span></td>
<td><span data-ttu-id="65254-185">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-185">NaN</span></span></td>
<td><span data-ttu-id="65254-186">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-186">NaN</span></span></td>
<td><span data-ttu-id="65254-187">NaN</span><span class="sxs-lookup"><span data-stu-id="65254-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="65254-188">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="65254-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65254-189">Vértice</span><span class="sxs-lookup"><span data-stu-id="65254-189">Vertex</span></span> | <span data-ttu-id="65254-190">Casco</span><span class="sxs-lookup"><span data-stu-id="65254-190">Hull</span></span> | <span data-ttu-id="65254-191">Dominio</span><span class="sxs-lookup"><span data-stu-id="65254-191">Domain</span></span> | <span data-ttu-id="65254-192">Geometría</span><span class="sxs-lookup"><span data-stu-id="65254-192">Geometry</span></span> | <span data-ttu-id="65254-193">Píxel</span><span class="sxs-lookup"><span data-stu-id="65254-193">Pixel</span></span> | <span data-ttu-id="65254-194">Compute</span><span class="sxs-lookup"><span data-stu-id="65254-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="65254-195">X</span><span class="sxs-lookup"><span data-stu-id="65254-195">X</span></span>      | <span data-ttu-id="65254-196">X</span><span class="sxs-lookup"><span data-stu-id="65254-196">X</span></span>    | <span data-ttu-id="65254-197">X</span><span class="sxs-lookup"><span data-stu-id="65254-197">X</span></span>      | <span data-ttu-id="65254-198">X</span><span class="sxs-lookup"><span data-stu-id="65254-198">X</span></span>        | <span data-ttu-id="65254-199">X</span><span class="sxs-lookup"><span data-stu-id="65254-199">X</span></span>     | <span data-ttu-id="65254-200">X</span><span class="sxs-lookup"><span data-stu-id="65254-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65254-201">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="65254-201">Minimum Shader Model</span></span>

<span data-ttu-id="65254-202">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="65254-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="65254-203">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="65254-203">Shader Model</span></span>                                              | <span data-ttu-id="65254-204">Compatible</span><span class="sxs-lookup"><span data-stu-id="65254-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65254-205">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="65254-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65254-206">sí</span><span class="sxs-lookup"><span data-stu-id="65254-206">yes</span></span>       |
| [<span data-ttu-id="65254-207">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="65254-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65254-208">no</span><span class="sxs-lookup"><span data-stu-id="65254-208">no</span></span>        |
| [<span data-ttu-id="65254-209">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="65254-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65254-210">no</span><span class="sxs-lookup"><span data-stu-id="65254-210">no</span></span>        |
| [<span data-ttu-id="65254-211">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65254-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65254-212">no</span><span class="sxs-lookup"><span data-stu-id="65254-212">no</span></span>        |
| [<span data-ttu-id="65254-213">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65254-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65254-214">no</span><span class="sxs-lookup"><span data-stu-id="65254-214">no</span></span>        |
| [<span data-ttu-id="65254-215">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65254-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65254-216">no</span><span class="sxs-lookup"><span data-stu-id="65254-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65254-217">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65254-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65254-218">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65254-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





