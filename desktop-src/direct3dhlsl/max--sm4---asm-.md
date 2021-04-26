---
title: max (sm4 - asm)
description: Máximo flotante por componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994732"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="e582c-103">max (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="e582c-103">max (sm4 - asm)</span></span>

<span data-ttu-id="e582c-104">Máximo flotante por componente.</span><span class="sxs-lookup"><span data-stu-id="e582c-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="e582c-105">max \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swle \] ,</span><span class="sxs-lookup"><span data-stu-id="e582c-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e582c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e582c-106">Item</span></span>                                                            | <span data-ttu-id="e582c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e582c-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e582c-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="e582c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e582c-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e582c-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="e582c-110">*dest*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="e582c-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="e582c-111">*src0:* *src1*</span><span class="sxs-lookup"><span data-stu-id="e582c-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="e582c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e582c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e582c-113">\[en \] Los componentes que se comparan con *src1*.</span><span class="sxs-lookup"><span data-stu-id="e582c-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="e582c-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e582c-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e582c-115">\[en \] Los componentes que se comparan con *src0*.</span><span class="sxs-lookup"><span data-stu-id="e582c-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e582c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e582c-116">Remarks</span></span>

><span data-ttu-id="e582c-117">= se usa en lugar > para que si min(x,y) = x, max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="e582c-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="e582c-118">NaN tiene un control especial.</span><span class="sxs-lookup"><span data-stu-id="e582c-118">NaN has special handling.</span></span> <span data-ttu-id="e582c-119">Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="e582c-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="e582c-120">Si ambos son NaN, se devuelve cualquier representación de NaN.</span><span class="sxs-lookup"><span data-stu-id="e582c-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="e582c-121">Los desnormas se vacían con el signo conservado antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="e582c-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="e582c-122">Sin embargo, el resultado escrito *en dest* puede o no vaciarse desnormado.</span><span class="sxs-lookup"><span data-stu-id="e582c-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="e582c-123">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.</span><span class="sxs-lookup"><span data-stu-id="e582c-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="e582c-124">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="e582c-124">F means finite real number.</span></span>



| <span data-ttu-id="e582c-125">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="e582c-125">**src0 src1->**</span></span> | <span data-ttu-id="e582c-126">**-inf**</span><span class="sxs-lookup"><span data-stu-id="e582c-126">**-inf**</span></span> | <span data-ttu-id="e582c-127">**F**</span><span class="sxs-lookup"><span data-stu-id="e582c-127">**F**</span></span>        | <span data-ttu-id="e582c-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="e582c-128">**+inf**</span></span> | <span data-ttu-id="e582c-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e582c-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="e582c-130">**-inf**</span><span class="sxs-lookup"><span data-stu-id="e582c-130">**-inf**</span></span>           | <span data-ttu-id="e582c-131">-inf</span><span class="sxs-lookup"><span data-stu-id="e582c-131">-inf</span></span>     | <span data-ttu-id="e582c-132">src1</span><span class="sxs-lookup"><span data-stu-id="e582c-132">src1</span></span>         | <span data-ttu-id="e582c-133">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-133">+inf</span></span>     | <span data-ttu-id="e582c-134">-inf</span><span class="sxs-lookup"><span data-stu-id="e582c-134">-inf</span></span>    |
| <span data-ttu-id="e582c-135">**F**</span><span class="sxs-lookup"><span data-stu-id="e582c-135">**F**</span></span>              | <span data-ttu-id="e582c-136">src0</span><span class="sxs-lookup"><span data-stu-id="e582c-136">src0</span></span>     | <span data-ttu-id="e582c-137">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="e582c-137">src0 or src1</span></span> | <span data-ttu-id="e582c-138">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-138">+inf</span></span>     | <span data-ttu-id="e582c-139">src0</span><span class="sxs-lookup"><span data-stu-id="e582c-139">src0</span></span>    |
| <span data-ttu-id="e582c-140">**+inf**</span><span class="sxs-lookup"><span data-stu-id="e582c-140">**+inf**</span></span>           | <span data-ttu-id="e582c-141">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-141">+inf</span></span>     | <span data-ttu-id="e582c-142">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-142">+inf</span></span>         | <span data-ttu-id="e582c-143">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-143">+inf</span></span>     | <span data-ttu-id="e582c-144">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-144">+inf</span></span>    |
| <span data-ttu-id="e582c-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="e582c-145">**NaN**</span></span>            | <span data-ttu-id="e582c-146">-inf</span><span class="sxs-lookup"><span data-stu-id="e582c-146">-inf</span></span>     | <span data-ttu-id="e582c-147">src1</span><span class="sxs-lookup"><span data-stu-id="e582c-147">src1</span></span>         | <span data-ttu-id="e582c-148">+inf</span><span class="sxs-lookup"><span data-stu-id="e582c-148">+inf</span></span>     | <span data-ttu-id="e582c-149">NaN</span><span class="sxs-lookup"><span data-stu-id="e582c-149">NaN</span></span>     |



 

<span data-ttu-id="e582c-150">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e582c-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e582c-151">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="e582c-151">Vertex Shader</span></span> | <span data-ttu-id="e582c-152">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="e582c-152">Geometry Shader</span></span> | <span data-ttu-id="e582c-153">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e582c-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e582c-154">x</span><span class="sxs-lookup"><span data-stu-id="e582c-154">x</span></span>             | <span data-ttu-id="e582c-155">x</span><span class="sxs-lookup"><span data-stu-id="e582c-155">x</span></span>               | <span data-ttu-id="e582c-156">x</span><span class="sxs-lookup"><span data-stu-id="e582c-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e582c-157">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e582c-157">Minimum Shader Model</span></span>

<span data-ttu-id="e582c-158">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e582c-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e582c-159">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e582c-159">Shader Model</span></span>                                              | <span data-ttu-id="e582c-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="e582c-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e582c-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e582c-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e582c-162">sí</span><span class="sxs-lookup"><span data-stu-id="e582c-162">yes</span></span>       |
| [<span data-ttu-id="e582c-163">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="e582c-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e582c-164">sí</span><span class="sxs-lookup"><span data-stu-id="e582c-164">yes</span></span>       |
| [<span data-ttu-id="e582c-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e582c-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e582c-166">sí</span><span class="sxs-lookup"><span data-stu-id="e582c-166">yes</span></span>       |
| [<span data-ttu-id="e582c-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e582c-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e582c-168">no</span><span class="sxs-lookup"><span data-stu-id="e582c-168">no</span></span>        |
| [<span data-ttu-id="e582c-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e582c-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e582c-170">no</span><span class="sxs-lookup"><span data-stu-id="e582c-170">no</span></span>        |
| [<span data-ttu-id="e582c-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e582c-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e582c-172">no</span><span class="sxs-lookup"><span data-stu-id="e582c-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e582c-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e582c-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e582c-174">Ensamblado del modelo de sombreador 4 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="e582c-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





