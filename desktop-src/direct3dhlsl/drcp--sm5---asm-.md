---
title: drcp (sm5 - asm)
description: Calcula un recíproco de precisión doble por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998342"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="9bb0f-103">drcp (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="9bb0f-104">Calcula un recíproco de precisión doble por componente.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="9bb0f-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="9bb0f-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="9bb0f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9bb0f-106">Item</span></span>                                                            | <span data-ttu-id="9bb0f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bb0f-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb0f-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="9bb0f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9bb0f-109">\[en \] La dirección de los resultados</span><span class="sxs-lookup"><span data-stu-id="9bb0f-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="9bb0f-110">*dest*  =  **1.0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="9bb0f-111">El valor del resultado debe ser preciso a 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="9bb0f-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="9bb0f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9bb0f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9bb0f-113">\[en \] El número del que se debe tomar el recíproco.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="9bb0f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bb0f-114">Remarks</span></span>

<span data-ttu-id="9bb0f-115">El compilador HLSL emite la instrucción DRCP solo cuando se llama explícitamente a través del intrínseco rcp(), cuando se usa double como argumento.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="9bb0f-116">La precisión de esta instrucción debe ser 1.0 ULP.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="9bb0f-117">Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se enlacen a menos que se cumplen todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="9bb0f-118">El sistema admite DirectX 11.1.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="9bb0f-119">El sistema incluye un controlador WDDM 1.2.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="9bb0f-120">El controlador informa de la compatibilidad con esta instrucción a través de **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** establecido en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="9bb0f-121">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="9bb0f-122">En esta tabla, F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="9bb0f-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="9bb0f-123">**Fuente**-></span><span class="sxs-lookup"><span data-stu-id="9bb0f-123">**src**-></span></span>  | <span data-ttu-id="9bb0f-124">**-inf**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-124">**-inf**</span></span> | <span data-ttu-id="9bb0f-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-125">**-F**</span></span> | <span data-ttu-id="9bb0f-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-126">**-0**</span></span> | <span data-ttu-id="9bb0f-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-127">**+0**</span></span> | <span data-ttu-id="9bb0f-128">**+F**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-128">**+F**</span></span> | <span data-ttu-id="9bb0f-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-129">**+inf**</span></span> | <span data-ttu-id="9bb0f-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9bb0f-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="9bb0f-131">**Dest**-></span><span class="sxs-lookup"><span data-stu-id="9bb0f-131">**dest**-></span></span> | <span data-ttu-id="9bb0f-132">-0</span><span class="sxs-lookup"><span data-stu-id="9bb0f-132">-0</span></span>       | <span data-ttu-id="9bb0f-133">-F</span><span class="sxs-lookup"><span data-stu-id="9bb0f-133">-F</span></span>     | <span data-ttu-id="9bb0f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="9bb0f-134">-inf</span></span>   | <span data-ttu-id="9bb0f-135">+inf</span><span class="sxs-lookup"><span data-stu-id="9bb0f-135">+inf</span></span>   | <span data-ttu-id="9bb0f-136">+F</span><span class="sxs-lookup"><span data-stu-id="9bb0f-136">+F</span></span>     | <span data-ttu-id="9bb0f-137">+0</span><span class="sxs-lookup"><span data-stu-id="9bb0f-137">+0</span></span>       | <span data-ttu-id="9bb0f-138">NaN</span><span class="sxs-lookup"><span data-stu-id="9bb0f-138">NaN</span></span>     |



 

<span data-ttu-id="9bb0f-139">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9bb0f-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9bb0f-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="9bb0f-140">Vertex</span></span> | <span data-ttu-id="9bb0f-141">Casco</span><span class="sxs-lookup"><span data-stu-id="9bb0f-141">Hull</span></span> | <span data-ttu-id="9bb0f-142">Domain</span><span class="sxs-lookup"><span data-stu-id="9bb0f-142">Domain</span></span> | <span data-ttu-id="9bb0f-143">Geometría</span><span class="sxs-lookup"><span data-stu-id="9bb0f-143">Geometry</span></span> | <span data-ttu-id="9bb0f-144">Píxel</span><span class="sxs-lookup"><span data-stu-id="9bb0f-144">Pixel</span></span> | <span data-ttu-id="9bb0f-145">Proceso</span><span class="sxs-lookup"><span data-stu-id="9bb0f-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9bb0f-146">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-146">X</span></span>      | <span data-ttu-id="9bb0f-147">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-147">X</span></span>    | <span data-ttu-id="9bb0f-148">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-148">X</span></span>      | <span data-ttu-id="9bb0f-149">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-149">X</span></span>        | <span data-ttu-id="9bb0f-150">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-150">X</span></span>     | <span data-ttu-id="9bb0f-151">X</span><span class="sxs-lookup"><span data-stu-id="9bb0f-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bb0f-152">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9bb0f-152">Minimum Shader Model</span></span>

<span data-ttu-id="9bb0f-153">Esta instrucción se admite en los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9bb0f-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9bb0f-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9bb0f-154">Shader Model</span></span>                                              | <span data-ttu-id="9bb0f-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="9bb0f-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9bb0f-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9bb0f-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9bb0f-157">sí</span><span class="sxs-lookup"><span data-stu-id="9bb0f-157">yes</span></span>       |
| [<span data-ttu-id="9bb0f-158">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="9bb0f-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9bb0f-159">no</span><span class="sxs-lookup"><span data-stu-id="9bb0f-159">no</span></span>        |
| [<span data-ttu-id="9bb0f-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9bb0f-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bb0f-161">no</span><span class="sxs-lookup"><span data-stu-id="9bb0f-161">no</span></span>        |
| [<span data-ttu-id="9bb0f-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bb0f-163">no</span><span class="sxs-lookup"><span data-stu-id="9bb0f-163">no</span></span>        |
| [<span data-ttu-id="9bb0f-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bb0f-165">no</span><span class="sxs-lookup"><span data-stu-id="9bb0f-165">no</span></span>        |
| [<span data-ttu-id="9bb0f-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bb0f-167">no</span><span class="sxs-lookup"><span data-stu-id="9bb0f-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9bb0f-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bb0f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bb0f-169">Ensamblado del modelo de sombreador 5 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="9bb0f-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





