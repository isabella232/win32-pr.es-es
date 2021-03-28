---
title: RCP (SM5-ASM)
description: Recíproco de componentes.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532896"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="b708a-103">RCP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b708a-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="b708a-104">Recíproco de componentes.</span><span class="sxs-lookup"><span data-stu-id="b708a-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="b708a-105">RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b708a-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="b708a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b708a-106">Item</span></span>                                                            | <span data-ttu-id="b708a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b708a-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b708a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b708a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b708a-109">\[en \] la dirección de los resultados</span><span class="sxs-lookup"><span data-stu-id="b708a-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="b708a-110">*dest*  =  **1,0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="b708a-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="b708a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b708a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b708a-112">\[en \] el número del que se va a tomar el recíproco.</span><span class="sxs-lookup"><span data-stu-id="b708a-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="b708a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b708a-113">Remarks</span></span>

<span data-ttu-id="b708a-114">Use esta instrucción para el uso de la precisión reducida, independientemente de los estrictos requisitos de la división.</span><span class="sxs-lookup"><span data-stu-id="b708a-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="b708a-115">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="b708a-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="b708a-116">(La tolerancia de errores solo coincide con RSQ)</span><span class="sxs-lookup"><span data-stu-id="b708a-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="b708a-117">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="b708a-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="b708a-118">*src*</span><span class="sxs-lookup"><span data-stu-id="b708a-118">*src*</span></span>  | <span data-ttu-id="b708a-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b708a-119">**-inf**</span></span> | <span data-ttu-id="b708a-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="b708a-120">**-F**</span></span> | <span data-ttu-id="b708a-121">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="b708a-121">**-denorm**</span></span> | <span data-ttu-id="b708a-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="b708a-122">**-0**</span></span> | <span data-ttu-id="b708a-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="b708a-123">**+0**</span></span> | <span data-ttu-id="b708a-124">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="b708a-124">**+denorm**</span></span> | <span data-ttu-id="b708a-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b708a-125">**+F**</span></span> | <span data-ttu-id="b708a-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b708a-126">**+inf**</span></span> | <span data-ttu-id="b708a-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="b708a-127">**NaN**</span></span> |
| <span data-ttu-id="b708a-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="b708a-128">*dest*</span></span> | <span data-ttu-id="b708a-129">-0</span><span class="sxs-lookup"><span data-stu-id="b708a-129">-0</span></span>       | <span data-ttu-id="b708a-130">-F</span><span class="sxs-lookup"><span data-stu-id="b708a-130">-F</span></span>     | <span data-ttu-id="b708a-131">-inf</span><span class="sxs-lookup"><span data-stu-id="b708a-131">-inf</span></span>        | <span data-ttu-id="b708a-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b708a-132">-inf</span></span>   | <span data-ttu-id="b708a-133">+inf</span><span class="sxs-lookup"><span data-stu-id="b708a-133">+inf</span></span>   | <span data-ttu-id="b708a-134">+inf</span><span class="sxs-lookup"><span data-stu-id="b708a-134">+inf</span></span>        | <span data-ttu-id="b708a-135">+F</span><span class="sxs-lookup"><span data-stu-id="b708a-135">+F</span></span>     | <span data-ttu-id="b708a-136">+0</span><span class="sxs-lookup"><span data-stu-id="b708a-136">+0</span></span>       | <span data-ttu-id="b708a-137">NaN</span><span class="sxs-lookup"><span data-stu-id="b708a-137">NaN</span></span>     |



 

<span data-ttu-id="b708a-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="b708a-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b708a-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="b708a-139">Vertex</span></span> | <span data-ttu-id="b708a-140">Casco</span><span class="sxs-lookup"><span data-stu-id="b708a-140">Hull</span></span> | <span data-ttu-id="b708a-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="b708a-141">Domain</span></span> | <span data-ttu-id="b708a-142">Geometría</span><span class="sxs-lookup"><span data-stu-id="b708a-142">Geometry</span></span> | <span data-ttu-id="b708a-143">Píxel</span><span class="sxs-lookup"><span data-stu-id="b708a-143">Pixel</span></span> | <span data-ttu-id="b708a-144">Compute</span><span class="sxs-lookup"><span data-stu-id="b708a-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b708a-145">X</span><span class="sxs-lookup"><span data-stu-id="b708a-145">X</span></span>      | <span data-ttu-id="b708a-146">X</span><span class="sxs-lookup"><span data-stu-id="b708a-146">X</span></span>    | <span data-ttu-id="b708a-147">X</span><span class="sxs-lookup"><span data-stu-id="b708a-147">X</span></span>      | <span data-ttu-id="b708a-148">X</span><span class="sxs-lookup"><span data-stu-id="b708a-148">X</span></span>        | <span data-ttu-id="b708a-149">X</span><span class="sxs-lookup"><span data-stu-id="b708a-149">X</span></span>     | <span data-ttu-id="b708a-150">X</span><span class="sxs-lookup"><span data-stu-id="b708a-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b708a-151">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b708a-151">Minimum Shader Model</span></span>

<span data-ttu-id="b708a-152">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b708a-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b708a-153">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b708a-153">Shader Model</span></span>                                              | <span data-ttu-id="b708a-154">Compatible</span><span class="sxs-lookup"><span data-stu-id="b708a-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b708a-155">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b708a-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b708a-156">sí</span><span class="sxs-lookup"><span data-stu-id="b708a-156">yes</span></span>       |
| [<span data-ttu-id="b708a-157">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b708a-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b708a-158">no</span><span class="sxs-lookup"><span data-stu-id="b708a-158">no</span></span>        |
| [<span data-ttu-id="b708a-159">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b708a-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b708a-160">no</span><span class="sxs-lookup"><span data-stu-id="b708a-160">no</span></span>        |
| [<span data-ttu-id="b708a-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b708a-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b708a-162">no</span><span class="sxs-lookup"><span data-stu-id="b708a-162">no</span></span>        |
| [<span data-ttu-id="b708a-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b708a-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b708a-164">no</span><span class="sxs-lookup"><span data-stu-id="b708a-164">no</span></span>        |
| [<span data-ttu-id="b708a-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b708a-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b708a-166">no</span><span class="sxs-lookup"><span data-stu-id="b708a-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b708a-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b708a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b708a-168">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b708a-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





