---
title: rcp (sm5 - asm)
description: Recíproco por componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998252"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="40697-103">rcp (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="40697-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="40697-104">Recíproco por componente.</span><span class="sxs-lookup"><span data-stu-id="40697-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="40697-105">rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="40697-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="40697-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="40697-106">Item</span></span>                                                            | <span data-ttu-id="40697-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="40697-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40697-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="40697-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="40697-109">\[en \] La dirección de los resultados</span><span class="sxs-lookup"><span data-stu-id="40697-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="40697-110">*dest*  =  **1.0f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="40697-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="40697-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="40697-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="40697-112">\[en \] El número del que se debe tomar el recíproco.</span><span class="sxs-lookup"><span data-stu-id="40697-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="40697-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40697-113">Remarks</span></span>

<span data-ttu-id="40697-114">Use esta instrucción para reducir la precisión mutua, independientemente de los requisitos estrictos para la división.</span><span class="sxs-lookup"><span data-stu-id="40697-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="40697-115">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="40697-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="40697-116">(La tolerancia a errores solo coincide con rsq)</span><span class="sxs-lookup"><span data-stu-id="40697-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="40697-117">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="40697-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="40697-118">*src*</span><span class="sxs-lookup"><span data-stu-id="40697-118">*src*</span></span>  | <span data-ttu-id="40697-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="40697-119">**-inf**</span></span> | <span data-ttu-id="40697-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="40697-120">**-F**</span></span> | <span data-ttu-id="40697-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="40697-121">**-denorm**</span></span> | <span data-ttu-id="40697-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="40697-122">**-0**</span></span> | <span data-ttu-id="40697-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="40697-123">**+0**</span></span> | <span data-ttu-id="40697-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="40697-124">**+denorm**</span></span> | <span data-ttu-id="40697-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="40697-125">**+F**</span></span> | <span data-ttu-id="40697-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="40697-126">**+inf**</span></span> | <span data-ttu-id="40697-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="40697-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="40697-128">*Dest*</span><span class="sxs-lookup"><span data-stu-id="40697-128">*dest*</span></span> | <span data-ttu-id="40697-129">-0</span><span class="sxs-lookup"><span data-stu-id="40697-129">-0</span></span>       | <span data-ttu-id="40697-130">-F</span><span class="sxs-lookup"><span data-stu-id="40697-130">-F</span></span>     | <span data-ttu-id="40697-131">-inf</span><span class="sxs-lookup"><span data-stu-id="40697-131">-inf</span></span>        | <span data-ttu-id="40697-132">-inf</span><span class="sxs-lookup"><span data-stu-id="40697-132">-inf</span></span>   | <span data-ttu-id="40697-133">+inf</span><span class="sxs-lookup"><span data-stu-id="40697-133">+inf</span></span>   | <span data-ttu-id="40697-134">+inf</span><span class="sxs-lookup"><span data-stu-id="40697-134">+inf</span></span>        | <span data-ttu-id="40697-135">+F</span><span class="sxs-lookup"><span data-stu-id="40697-135">+F</span></span>     | <span data-ttu-id="40697-136">+0</span><span class="sxs-lookup"><span data-stu-id="40697-136">+0</span></span>       | <span data-ttu-id="40697-137">NaN</span><span class="sxs-lookup"><span data-stu-id="40697-137">NaN</span></span>     |



 

<span data-ttu-id="40697-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="40697-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="40697-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="40697-139">Vertex</span></span> | <span data-ttu-id="40697-140">Casco</span><span class="sxs-lookup"><span data-stu-id="40697-140">Hull</span></span> | <span data-ttu-id="40697-141">Domain</span><span class="sxs-lookup"><span data-stu-id="40697-141">Domain</span></span> | <span data-ttu-id="40697-142">Geometría</span><span class="sxs-lookup"><span data-stu-id="40697-142">Geometry</span></span> | <span data-ttu-id="40697-143">Píxel</span><span class="sxs-lookup"><span data-stu-id="40697-143">Pixel</span></span> | <span data-ttu-id="40697-144">Proceso</span><span class="sxs-lookup"><span data-stu-id="40697-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="40697-145">X</span><span class="sxs-lookup"><span data-stu-id="40697-145">X</span></span>      | <span data-ttu-id="40697-146">X</span><span class="sxs-lookup"><span data-stu-id="40697-146">X</span></span>    | <span data-ttu-id="40697-147">X</span><span class="sxs-lookup"><span data-stu-id="40697-147">X</span></span>      | <span data-ttu-id="40697-148">X</span><span class="sxs-lookup"><span data-stu-id="40697-148">X</span></span>        | <span data-ttu-id="40697-149">X</span><span class="sxs-lookup"><span data-stu-id="40697-149">X</span></span>     | <span data-ttu-id="40697-150">X</span><span class="sxs-lookup"><span data-stu-id="40697-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="40697-151">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="40697-151">Minimum Shader Model</span></span>

<span data-ttu-id="40697-152">Esta instrucción se admite en los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="40697-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="40697-153">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="40697-153">Shader Model</span></span>                                              | <span data-ttu-id="40697-154">Compatible</span><span class="sxs-lookup"><span data-stu-id="40697-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="40697-155">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="40697-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="40697-156">sí</span><span class="sxs-lookup"><span data-stu-id="40697-156">yes</span></span>       |
| [<span data-ttu-id="40697-157">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="40697-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="40697-158">no</span><span class="sxs-lookup"><span data-stu-id="40697-158">no</span></span>        |
| [<span data-ttu-id="40697-159">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="40697-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="40697-160">no</span><span class="sxs-lookup"><span data-stu-id="40697-160">no</span></span>        |
| [<span data-ttu-id="40697-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40697-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="40697-162">no</span><span class="sxs-lookup"><span data-stu-id="40697-162">no</span></span>        |
| [<span data-ttu-id="40697-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40697-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="40697-164">no</span><span class="sxs-lookup"><span data-stu-id="40697-164">no</span></span>        |
| [<span data-ttu-id="40697-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40697-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="40697-166">no</span><span class="sxs-lookup"><span data-stu-id="40697-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="40697-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40697-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40697-168">Ensamblado del modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="40697-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





