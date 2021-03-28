---
title: RSQ (SM4-ASM)
description: Raíz cuadrada recíproca de los componentes.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc274f927151938be055150d5b17287f9be0004d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077118"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="c88d3-103">RSQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c88d3-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="c88d3-104">Raíz cuadrada recíproca de los componentes.</span><span class="sxs-lookup"><span data-stu-id="c88d3-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="c88d3-105">RSQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c88d3-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="c88d3-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c88d3-106">Item</span></span>                                                            | <span data-ttu-id="c88d3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c88d3-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c88d3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c88d3-109">\[en \] contiene los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="c88d3-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="c88d3-110">*dest* = 1.0 f/sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="c88d3-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="c88d3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c88d3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c88d3-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="c88d3-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="c88d3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c88d3-113">Remarks</span></span>

<span data-ttu-id="c88d3-114">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="c88d3-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="c88d3-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="c88d3-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="c88d3-116">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="c88d3-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="c88d3-117">**src**</span><span class="sxs-lookup"><span data-stu-id="c88d3-117">**src**</span></span>  | <span data-ttu-id="c88d3-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c88d3-118">**-inf**</span></span> | <span data-ttu-id="c88d3-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="c88d3-119">**-F**</span></span> | <span data-ttu-id="c88d3-120">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="c88d3-120">**-denorm**</span></span> | <span data-ttu-id="c88d3-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="c88d3-121">**-0**</span></span> | <span data-ttu-id="c88d3-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="c88d3-122">**+0**</span></span> | <span data-ttu-id="c88d3-123">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="c88d3-123">**+denorm**</span></span> | <span data-ttu-id="c88d3-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c88d3-124">**+F**</span></span> | <span data-ttu-id="c88d3-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c88d3-125">**+inf**</span></span> | <span data-ttu-id="c88d3-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c88d3-126">**NaN**</span></span> |
| <span data-ttu-id="c88d3-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="c88d3-127">**dest**</span></span> | <span data-ttu-id="c88d3-128">NaN</span><span class="sxs-lookup"><span data-stu-id="c88d3-128">NaN</span></span>      | <span data-ttu-id="c88d3-129">NaN</span><span class="sxs-lookup"><span data-stu-id="c88d3-129">NaN</span></span>    | <span data-ttu-id="c88d3-130">-inf</span><span class="sxs-lookup"><span data-stu-id="c88d3-130">-inf</span></span>        | <span data-ttu-id="c88d3-131">-inf</span><span class="sxs-lookup"><span data-stu-id="c88d3-131">-inf</span></span>   | <span data-ttu-id="c88d3-132">+inf</span><span class="sxs-lookup"><span data-stu-id="c88d3-132">+inf</span></span>   | <span data-ttu-id="c88d3-133">+inf</span><span class="sxs-lookup"><span data-stu-id="c88d3-133">+inf</span></span>        | <span data-ttu-id="c88d3-134">+F</span><span class="sxs-lookup"><span data-stu-id="c88d3-134">+F</span></span>     | <span data-ttu-id="c88d3-135">+0</span><span class="sxs-lookup"><span data-stu-id="c88d3-135">+0</span></span>       | <span data-ttu-id="c88d3-136">NaN</span><span class="sxs-lookup"><span data-stu-id="c88d3-136">NaN</span></span>     |



 

<span data-ttu-id="c88d3-137">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c88d3-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c88d3-138">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c88d3-138">Vertex Shader</span></span> | <span data-ttu-id="c88d3-139">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="c88d3-139">Geometry Shader</span></span> | <span data-ttu-id="c88d3-140">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c88d3-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c88d3-141">x</span><span class="sxs-lookup"><span data-stu-id="c88d3-141">x</span></span>             | <span data-ttu-id="c88d3-142">x</span><span class="sxs-lookup"><span data-stu-id="c88d3-142">x</span></span>               | <span data-ttu-id="c88d3-143">x</span><span class="sxs-lookup"><span data-stu-id="c88d3-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c88d3-144">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c88d3-144">Minimum Shader Model</span></span>

<span data-ttu-id="c88d3-145">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c88d3-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c88d3-146">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c88d3-146">Shader Model</span></span>                                              | <span data-ttu-id="c88d3-147">Compatible</span><span class="sxs-lookup"><span data-stu-id="c88d3-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c88d3-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c88d3-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c88d3-149">sí</span><span class="sxs-lookup"><span data-stu-id="c88d3-149">yes</span></span>       |
| [<span data-ttu-id="c88d3-150">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c88d3-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c88d3-151">sí</span><span class="sxs-lookup"><span data-stu-id="c88d3-151">yes</span></span>       |
| [<span data-ttu-id="c88d3-152">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c88d3-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c88d3-153">sí</span><span class="sxs-lookup"><span data-stu-id="c88d3-153">yes</span></span>       |
| [<span data-ttu-id="c88d3-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88d3-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c88d3-155">no</span><span class="sxs-lookup"><span data-stu-id="c88d3-155">no</span></span>        |
| [<span data-ttu-id="c88d3-156">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88d3-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c88d3-157">no</span><span class="sxs-lookup"><span data-stu-id="c88d3-157">no</span></span>        |
| [<span data-ttu-id="c88d3-158">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88d3-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c88d3-159">no</span><span class="sxs-lookup"><span data-stu-id="c88d3-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c88d3-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c88d3-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c88d3-161">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88d3-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





