---
title: log (sm4 - asm)
description: Base de registro 2 por componentes.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998322"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="a556e-103">log (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="a556e-103">log (sm4 - asm)</span></span>

<span data-ttu-id="a556e-104">Base de registro 2 por componentes.</span><span class="sxs-lookup"><span data-stu-id="a556e-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="a556e-105">log \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle</span><span class="sxs-lookup"><span data-stu-id="a556e-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="a556e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a556e-106">Item</span></span>                                                            | <span data-ttu-id="a556e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a556e-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a556e-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="a556e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a556e-109">\[en \] La dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a556e-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="a556e-110">dest = log2(src0)</span><span class="sxs-lookup"><span data-stu-id="a556e-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="a556e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a556e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a556e-112">\[en \] El valor de la operación.</span><span class="sxs-lookup"><span data-stu-id="a556e-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="a556e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a556e-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="a556e-114">Restricciones</span><span class="sxs-lookup"><span data-stu-id="a556e-114">Restrictions</span></span>

-   <span data-ttu-id="a556e-115">Sigue la teoría del límite.</span><span class="sxs-lookup"><span data-stu-id="a556e-115">Follows limit theory.</span></span>
-   <span data-ttu-id="a556e-116">Tolerancia a errores: si *src0* es \[ 0.5..2, el error absolue no debe ser superior a \] 2-21.</span><span class="sxs-lookup"><span data-stu-id="a556e-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="a556e-117">Si *src0* es (0..0.5) o (2..+INF), el error relativo no debe ser superior a \] 2-21.</span><span class="sxs-lookup"><span data-stu-id="a556e-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="a556e-118">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="a556e-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="a556e-119">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="a556e-119">F means finite-real number.</span></span>



| <span data-ttu-id="a556e-120">**src**</span><span class="sxs-lookup"><span data-stu-id="a556e-120">**src**</span></span>  | <span data-ttu-id="a556e-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="a556e-121">**-inf**</span></span> | <span data-ttu-id="a556e-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="a556e-122">**-F**</span></span> | <span data-ttu-id="a556e-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="a556e-123">**-denorm**</span></span> | <span data-ttu-id="a556e-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="a556e-124">**-0**</span></span> | <span data-ttu-id="a556e-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="a556e-125">**+0**</span></span> | <span data-ttu-id="a556e-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="a556e-126">**+denorm**</span></span> | <span data-ttu-id="a556e-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="a556e-127">**+F**</span></span> | <span data-ttu-id="a556e-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="a556e-128">**+inf**</span></span> | <span data-ttu-id="a556e-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a556e-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="a556e-130">**Dest**</span><span class="sxs-lookup"><span data-stu-id="a556e-130">**dest**</span></span> | <span data-ttu-id="a556e-131">NaN</span><span class="sxs-lookup"><span data-stu-id="a556e-131">NaN</span></span>      | <span data-ttu-id="a556e-132">NaN</span><span class="sxs-lookup"><span data-stu-id="a556e-132">NaN</span></span>    | <span data-ttu-id="a556e-133">-inf</span><span class="sxs-lookup"><span data-stu-id="a556e-133">-inf</span></span>        | <span data-ttu-id="a556e-134">-inf</span><span class="sxs-lookup"><span data-stu-id="a556e-134">-inf</span></span>   | <span data-ttu-id="a556e-135">-inf</span><span class="sxs-lookup"><span data-stu-id="a556e-135">-inf</span></span>   | <span data-ttu-id="a556e-136">-inf</span><span class="sxs-lookup"><span data-stu-id="a556e-136">-inf</span></span>        | <span data-ttu-id="a556e-137">F</span><span class="sxs-lookup"><span data-stu-id="a556e-137">F</span></span>      | <span data-ttu-id="a556e-138">+inf</span><span class="sxs-lookup"><span data-stu-id="a556e-138">+inf</span></span>     | <span data-ttu-id="a556e-139">NaN</span><span class="sxs-lookup"><span data-stu-id="a556e-139">NaN</span></span>     |



 

<span data-ttu-id="a556e-140">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a556e-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a556e-141">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a556e-141">Vertex Shader</span></span> | <span data-ttu-id="a556e-142">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="a556e-142">Geometry Shader</span></span> | <span data-ttu-id="a556e-143">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a556e-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a556e-144">x</span><span class="sxs-lookup"><span data-stu-id="a556e-144">x</span></span>             | <span data-ttu-id="a556e-145">x</span><span class="sxs-lookup"><span data-stu-id="a556e-145">x</span></span>               | <span data-ttu-id="a556e-146">x</span><span class="sxs-lookup"><span data-stu-id="a556e-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="a556e-147">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a556e-147">Minimum Shader Model</span></span>

<span data-ttu-id="a556e-148">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a556e-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a556e-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a556e-149">Shader Model</span></span>                                              | <span data-ttu-id="a556e-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="a556e-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a556e-151">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a556e-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a556e-152">sí</span><span class="sxs-lookup"><span data-stu-id="a556e-152">yes</span></span>       |
| [<span data-ttu-id="a556e-153">Shader Model 4.1</span><span class="sxs-lookup"><span data-stu-id="a556e-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a556e-154">sí</span><span class="sxs-lookup"><span data-stu-id="a556e-154">yes</span></span>       |
| [<span data-ttu-id="a556e-155">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="a556e-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a556e-156">sí</span><span class="sxs-lookup"><span data-stu-id="a556e-156">yes</span></span>       |
| [<span data-ttu-id="a556e-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a556e-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a556e-158">no</span><span class="sxs-lookup"><span data-stu-id="a556e-158">no</span></span>        |
| [<span data-ttu-id="a556e-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a556e-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a556e-160">no</span><span class="sxs-lookup"><span data-stu-id="a556e-160">no</span></span>        |
| [<span data-ttu-id="a556e-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a556e-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a556e-162">no</span><span class="sxs-lookup"><span data-stu-id="a556e-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a556e-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a556e-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a556e-164">Ensamblado del modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a556e-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





