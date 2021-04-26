---
title: exp (sm4 - asm)
description: 2exponent por componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999082"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="ee8e4-103">exp (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="ee8e4-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="ee8e4-104">2exponent por componente.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="ee8e4-105">exp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="ee8e4-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="ee8e4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee8e4-106">Item</span></span>                                                            | <span data-ttu-id="ee8e4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee8e4-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ee8e4-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="ee8e4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ee8e4-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="ee8e4-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="ee8e4-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="ee8e4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ee8e4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ee8e4-112">\[en \] El exponente.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ee8e4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee8e4-113">Remarks</span></span>

<span data-ttu-id="ee8e4-114">Esta instrucción sigue la teoría del límite.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-114">This instruction follows limit theory.</span></span> <span data-ttu-id="ee8e4-115">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="ee8e4-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ee8e4-117">En esta tabla, F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="ee8e4-118">**src**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-118">**src**</span></span>  | <span data-ttu-id="ee8e4-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-119">**-inf**</span></span> | <span data-ttu-id="ee8e4-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-120">**-F**</span></span> | <span data-ttu-id="ee8e4-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-121">**-denorm**</span></span> | <span data-ttu-id="ee8e4-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-122">**-0**</span></span> | <span data-ttu-id="ee8e4-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-123">**+0**</span></span> | <span data-ttu-id="ee8e4-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-124">**+denorm**</span></span> | <span data-ttu-id="ee8e4-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-125">**+F**</span></span> | <span data-ttu-id="ee8e4-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-126">**+inf**</span></span> | <span data-ttu-id="ee8e4-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ee8e4-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="ee8e4-128">**dest**</span></span> | <span data-ttu-id="ee8e4-129">0</span><span class="sxs-lookup"><span data-stu-id="ee8e4-129">0</span></span>        | <span data-ttu-id="ee8e4-130">+F</span><span class="sxs-lookup"><span data-stu-id="ee8e4-130">+F</span></span>     | <span data-ttu-id="ee8e4-131">1</span><span class="sxs-lookup"><span data-stu-id="ee8e4-131">1</span></span>           | <span data-ttu-id="ee8e4-132">1</span><span class="sxs-lookup"><span data-stu-id="ee8e4-132">1</span></span>      | <span data-ttu-id="ee8e4-133">1</span><span class="sxs-lookup"><span data-stu-id="ee8e4-133">1</span></span>      | <span data-ttu-id="ee8e4-134">1</span><span class="sxs-lookup"><span data-stu-id="ee8e4-134">1</span></span>           | <span data-ttu-id="ee8e4-135">+F</span><span class="sxs-lookup"><span data-stu-id="ee8e4-135">+F</span></span>     | <span data-ttu-id="ee8e4-136">+inf</span><span class="sxs-lookup"><span data-stu-id="ee8e4-136">+inf</span></span>     | <span data-ttu-id="ee8e4-137">NaN</span><span class="sxs-lookup"><span data-stu-id="ee8e4-137">NaN</span></span>     |



 

<span data-ttu-id="ee8e4-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ee8e4-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ee8e4-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ee8e4-139">Vertex Shader</span></span> | <span data-ttu-id="ee8e4-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ee8e4-140">Geometry Shader</span></span> | <span data-ttu-id="ee8e4-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ee8e4-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ee8e4-142">x</span><span class="sxs-lookup"><span data-stu-id="ee8e4-142">x</span></span>             | <span data-ttu-id="ee8e4-143">x</span><span class="sxs-lookup"><span data-stu-id="ee8e4-143">x</span></span>               | <span data-ttu-id="ee8e4-144">x</span><span class="sxs-lookup"><span data-stu-id="ee8e4-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee8e4-145">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ee8e4-145">Minimum Shader Model</span></span>

<span data-ttu-id="ee8e4-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ee8e4-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee8e4-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ee8e4-147">Shader Model</span></span>                                              | <span data-ttu-id="ee8e4-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="ee8e4-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ee8e4-149">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="ee8e4-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ee8e4-150">sí</span><span class="sxs-lookup"><span data-stu-id="ee8e4-150">yes</span></span>       |
| [<span data-ttu-id="ee8e4-151">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="ee8e4-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ee8e4-152">sí</span><span class="sxs-lookup"><span data-stu-id="ee8e4-152">yes</span></span>       |
| [<span data-ttu-id="ee8e4-153">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="ee8e4-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ee8e4-154">sí</span><span class="sxs-lookup"><span data-stu-id="ee8e4-154">yes</span></span>       |
| [<span data-ttu-id="ee8e4-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee8e4-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ee8e4-156">no</span><span class="sxs-lookup"><span data-stu-id="ee8e4-156">no</span></span>        |
| [<span data-ttu-id="ee8e4-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee8e4-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ee8e4-158">no</span><span class="sxs-lookup"><span data-stu-id="ee8e4-158">no</span></span>        |
| [<span data-ttu-id="ee8e4-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee8e4-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ee8e4-160">no</span><span class="sxs-lookup"><span data-stu-id="ee8e4-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ee8e4-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee8e4-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee8e4-162">Ensamblado del modelo 4 del sombreador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="ee8e4-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





