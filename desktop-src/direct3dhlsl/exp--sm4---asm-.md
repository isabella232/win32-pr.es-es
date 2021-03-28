---
title: exp (SM4-ASM)
description: 2exponent de los componentes.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077070"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="c9e03-103">exp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c9e03-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="c9e03-104">2exponent de los componentes.</span><span class="sxs-lookup"><span data-stu-id="c9e03-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="c9e03-105">EXP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c9e03-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="c9e03-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9e03-106">Item</span></span>                                                            | <span data-ttu-id="c9e03-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9e03-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c9e03-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c9e03-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c9e03-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c9e03-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="c9e03-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="c9e03-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="c9e03-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c9e03-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c9e03-112">\[en \] el exponente.</span><span class="sxs-lookup"><span data-stu-id="c9e03-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="c9e03-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9e03-113">Remarks</span></span>

<span data-ttu-id="c9e03-114">Esta instrucción sigue la teoría del límite.</span><span class="sxs-lookup"><span data-stu-id="c9e03-114">This instruction follows limit theory.</span></span> <span data-ttu-id="c9e03-115">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="c9e03-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="c9e03-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="c9e03-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="c9e03-117">En esta tabla F se indica un número finito-real.</span><span class="sxs-lookup"><span data-stu-id="c9e03-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="c9e03-118">**src**</span><span class="sxs-lookup"><span data-stu-id="c9e03-118">**src**</span></span>  | <span data-ttu-id="c9e03-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="c9e03-119">**-inf**</span></span> | <span data-ttu-id="c9e03-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="c9e03-120">**-F**</span></span> | <span data-ttu-id="c9e03-121">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="c9e03-121">**-denorm**</span></span> | <span data-ttu-id="c9e03-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="c9e03-122">**-0**</span></span> | <span data-ttu-id="c9e03-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="c9e03-123">**+0**</span></span> | <span data-ttu-id="c9e03-124">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="c9e03-124">**+denorm**</span></span> | <span data-ttu-id="c9e03-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="c9e03-125">**+F**</span></span> | <span data-ttu-id="c9e03-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="c9e03-126">**+inf**</span></span> | <span data-ttu-id="c9e03-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c9e03-127">**NaN**</span></span> |
| <span data-ttu-id="c9e03-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="c9e03-128">**dest**</span></span> | <span data-ttu-id="c9e03-129">0</span><span class="sxs-lookup"><span data-stu-id="c9e03-129">0</span></span>        | <span data-ttu-id="c9e03-130">+F</span><span class="sxs-lookup"><span data-stu-id="c9e03-130">+F</span></span>     | <span data-ttu-id="c9e03-131">1</span><span class="sxs-lookup"><span data-stu-id="c9e03-131">1</span></span>           | <span data-ttu-id="c9e03-132">1</span><span class="sxs-lookup"><span data-stu-id="c9e03-132">1</span></span>      | <span data-ttu-id="c9e03-133">1</span><span class="sxs-lookup"><span data-stu-id="c9e03-133">1</span></span>      | <span data-ttu-id="c9e03-134">1</span><span class="sxs-lookup"><span data-stu-id="c9e03-134">1</span></span>           | <span data-ttu-id="c9e03-135">+F</span><span class="sxs-lookup"><span data-stu-id="c9e03-135">+F</span></span>     | <span data-ttu-id="c9e03-136">+inf</span><span class="sxs-lookup"><span data-stu-id="c9e03-136">+inf</span></span>     | <span data-ttu-id="c9e03-137">NaN</span><span class="sxs-lookup"><span data-stu-id="c9e03-137">NaN</span></span>     |



 

<span data-ttu-id="c9e03-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c9e03-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c9e03-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c9e03-139">Vertex Shader</span></span> | <span data-ttu-id="c9e03-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="c9e03-140">Geometry Shader</span></span> | <span data-ttu-id="c9e03-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c9e03-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c9e03-142">x</span><span class="sxs-lookup"><span data-stu-id="c9e03-142">x</span></span>             | <span data-ttu-id="c9e03-143">x</span><span class="sxs-lookup"><span data-stu-id="c9e03-143">x</span></span>               | <span data-ttu-id="c9e03-144">x</span><span class="sxs-lookup"><span data-stu-id="c9e03-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9e03-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c9e03-145">Minimum Shader Model</span></span>

<span data-ttu-id="c9e03-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c9e03-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9e03-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c9e03-147">Shader Model</span></span>                                              | <span data-ttu-id="c9e03-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="c9e03-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c9e03-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c9e03-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c9e03-150">sí</span><span class="sxs-lookup"><span data-stu-id="c9e03-150">yes</span></span>       |
| [<span data-ttu-id="c9e03-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c9e03-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c9e03-152">sí</span><span class="sxs-lookup"><span data-stu-id="c9e03-152">yes</span></span>       |
| [<span data-ttu-id="c9e03-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c9e03-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c9e03-154">sí</span><span class="sxs-lookup"><span data-stu-id="c9e03-154">yes</span></span>       |
| [<span data-ttu-id="c9e03-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e03-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c9e03-156">no</span><span class="sxs-lookup"><span data-stu-id="c9e03-156">no</span></span>        |
| [<span data-ttu-id="c9e03-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e03-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c9e03-158">no</span><span class="sxs-lookup"><span data-stu-id="c9e03-158">no</span></span>        |
| [<span data-ttu-id="c9e03-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e03-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c9e03-160">no</span><span class="sxs-lookup"><span data-stu-id="c9e03-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c9e03-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9e03-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9e03-162">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9e03-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





