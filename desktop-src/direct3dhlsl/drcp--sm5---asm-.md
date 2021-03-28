---
title: DRCP (SM5-ASM)
description: Calcula un recíproco de doble precisión de tipo componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358491"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="2795f-103">DRCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2795f-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="2795f-104">Calcula un recíproco de doble precisión de tipo componente.</span><span class="sxs-lookup"><span data-stu-id="2795f-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="2795f-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2795f-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="2795f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2795f-106">Item</span></span>                                                            | <span data-ttu-id="2795f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2795f-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2795f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2795f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2795f-109">\[en \] la dirección de los resultados</span><span class="sxs-lookup"><span data-stu-id="2795f-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="2795f-110">*dest*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="2795f-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="2795f-111">El valor del resultado debe ser preciso para 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="2795f-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="2795f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2795f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2795f-113">\[en \] el número del que se va a tomar el recíproco.</span><span class="sxs-lookup"><span data-stu-id="2795f-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="2795f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2795f-114">Remarks</span></span>

<span data-ttu-id="2795f-115">El compilador de HLSL emite la instrucción DRCP solo cuando se llama explícitamente a través de la función de RCP (), cuando se usa un valor Double como argumento.</span><span class="sxs-lookup"><span data-stu-id="2795f-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="2795f-116">La precisión de esta instrucción es obligatoria para ser 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="2795f-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="2795f-117">Los sombreadores que usan esta instrucción se marcarán con una marca de sombreador que hará que no se puedan enlazar a menos que se cumplan todas las condiciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="2795f-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="2795f-118">El sistema admite DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="2795f-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="2795f-119">El sistema incluye un controlador WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="2795f-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="2795f-120">El controlador informa de la compatibilidad con esta instrucción a través de **\_ las opciones de D3D11 de datos de características de D3D11 \_ \_ \_ . ExtendedDoublesShaderInstructions** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="2795f-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="2795f-121">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="2795f-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="2795f-122">En esta tabla F se indica un número finito-real.</span><span class="sxs-lookup"><span data-stu-id="2795f-122">In this table F means finite-real number.</span></span>



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="2795f-123">**diez**-></span><span class="sxs-lookup"><span data-stu-id="2795f-123">**src**-></span></span>  | <span data-ttu-id="2795f-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2795f-124">**-inf**</span></span> | <span data-ttu-id="2795f-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="2795f-125">**-F**</span></span> | <span data-ttu-id="2795f-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="2795f-126">**-0**</span></span> | <span data-ttu-id="2795f-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="2795f-127">**+0**</span></span> | <span data-ttu-id="2795f-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2795f-128">**+F**</span></span> | <span data-ttu-id="2795f-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2795f-129">**+inf**</span></span> | <span data-ttu-id="2795f-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="2795f-130">**NaN**</span></span> |
| <span data-ttu-id="2795f-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="2795f-131">**dest**-></span></span> | <span data-ttu-id="2795f-132">-0</span><span class="sxs-lookup"><span data-stu-id="2795f-132">-0</span></span>       | <span data-ttu-id="2795f-133">-F</span><span class="sxs-lookup"><span data-stu-id="2795f-133">-F</span></span>     | <span data-ttu-id="2795f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="2795f-134">-inf</span></span>   | <span data-ttu-id="2795f-135">+inf</span><span class="sxs-lookup"><span data-stu-id="2795f-135">+inf</span></span>   | <span data-ttu-id="2795f-136">+F</span><span class="sxs-lookup"><span data-stu-id="2795f-136">+F</span></span>     | <span data-ttu-id="2795f-137">+0</span><span class="sxs-lookup"><span data-stu-id="2795f-137">+0</span></span>       | <span data-ttu-id="2795f-138">NaN</span><span class="sxs-lookup"><span data-stu-id="2795f-138">NaN</span></span>     |



 

<span data-ttu-id="2795f-139">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2795f-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2795f-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="2795f-140">Vertex</span></span> | <span data-ttu-id="2795f-141">Casco</span><span class="sxs-lookup"><span data-stu-id="2795f-141">Hull</span></span> | <span data-ttu-id="2795f-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="2795f-142">Domain</span></span> | <span data-ttu-id="2795f-143">Geometría</span><span class="sxs-lookup"><span data-stu-id="2795f-143">Geometry</span></span> | <span data-ttu-id="2795f-144">Píxel</span><span class="sxs-lookup"><span data-stu-id="2795f-144">Pixel</span></span> | <span data-ttu-id="2795f-145">Compute</span><span class="sxs-lookup"><span data-stu-id="2795f-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2795f-146">X</span><span class="sxs-lookup"><span data-stu-id="2795f-146">X</span></span>      | <span data-ttu-id="2795f-147">X</span><span class="sxs-lookup"><span data-stu-id="2795f-147">X</span></span>    | <span data-ttu-id="2795f-148">X</span><span class="sxs-lookup"><span data-stu-id="2795f-148">X</span></span>      | <span data-ttu-id="2795f-149">X</span><span class="sxs-lookup"><span data-stu-id="2795f-149">X</span></span>        | <span data-ttu-id="2795f-150">X</span><span class="sxs-lookup"><span data-stu-id="2795f-150">X</span></span>     | <span data-ttu-id="2795f-151">X</span><span class="sxs-lookup"><span data-stu-id="2795f-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2795f-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2795f-152">Minimum Shader Model</span></span>

<span data-ttu-id="2795f-153">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2795f-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2795f-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2795f-154">Shader Model</span></span>                                              | <span data-ttu-id="2795f-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="2795f-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2795f-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2795f-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2795f-157">sí</span><span class="sxs-lookup"><span data-stu-id="2795f-157">yes</span></span>       |
| [<span data-ttu-id="2795f-158">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2795f-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2795f-159">no</span><span class="sxs-lookup"><span data-stu-id="2795f-159">no</span></span>        |
| [<span data-ttu-id="2795f-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2795f-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2795f-161">no</span><span class="sxs-lookup"><span data-stu-id="2795f-161">no</span></span>        |
| [<span data-ttu-id="2795f-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2795f-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2795f-163">no</span><span class="sxs-lookup"><span data-stu-id="2795f-163">no</span></span>        |
| [<span data-ttu-id="2795f-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2795f-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2795f-165">no</span><span class="sxs-lookup"><span data-stu-id="2795f-165">no</span></span>        |
| [<span data-ttu-id="2795f-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2795f-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2795f-167">no</span><span class="sxs-lookup"><span data-stu-id="2795f-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2795f-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2795f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2795f-169">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2795f-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





