---
title: sample_d (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998185"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="dab32-104">ejemplo \_ d (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dab32-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="dab32-105">Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.</span><span class="sxs-lookup"><span data-stu-id="dab32-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="dab32-106">SSample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcXDerivatives \[ . swizzle \] , srcYDerivatives \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dab32-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dab32-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="dab32-107">Item</span></span>                                                                                                                               | <span data-ttu-id="dab32-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab32-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab32-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dab32-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="dab32-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="dab32-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="dab32-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="dab32-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="dab32-112">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="dab32-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="dab32-113">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="dab32-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="dab32-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="dab32-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="dab32-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="dab32-115">\[in\] A texture register.</span></span> <span data-ttu-id="dab32-116">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="dab32-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="dab32-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="dab32-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="dab32-118">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="dab32-118">\[in\] A sampler register.</span></span> <span data-ttu-id="dab32-119">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="dab32-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="dab32-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span><span class="sxs-lookup"><span data-stu-id="dab32-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="dab32-121">\[en \] los derivados de la dirección de origen en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="dab32-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="dab32-122">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="dab32-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="dab32-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span><span class="sxs-lookup"><span data-stu-id="dab32-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="dab32-124">\[en \] los derivados de la dirección de origen en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="dab32-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="dab32-125">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="dab32-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dab32-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dab32-126">Remarks</span></span>

<span data-ttu-id="dab32-127">Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , con la excepción de que los derivados de la dirección de origen en la dirección x y la dirección y se proporcionan mediante parámetros adicionales, *srcXDerivatives* y *srcYDerivatives*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dab32-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="dab32-128">Estos derivados se encuentran en un espacio normalizado de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="dab32-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="dab32-129">Los componentes r, g y b de *srcXDerivatives* (pos-swizzle) proporcionan du/DX, DV/DX y DW/DX.</span><span class="sxs-lookup"><span data-stu-id="dab32-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="dab32-130">Se omite el componente ' a ' (POS-swizzle).</span><span class="sxs-lookup"><span data-stu-id="dab32-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="dab32-131">Los componentes r, g y b de *srcYDerivatives* (pos-swizzle) proporcionan du/DY, DV/DY y DW/DY.</span><span class="sxs-lookup"><span data-stu-id="dab32-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="dab32-132">Se omite el componente ' a ' (POS-swizzle).</span><span class="sxs-lookup"><span data-stu-id="dab32-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="dab32-133">A diferencia de la instrucción de **ejemplo** , que puede compartir un único cálculo de LOD en una marca de 2x2, el **ejemplo \_ d** debe calcular el LOD completamente de forma independiente y por píxel cuando se usa en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dab32-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="dab32-134">Si las entradas derivadas del **ejemplo \_ d** proceden de instrucciones de cálculo derivadas en el sombreador de píxeles y los valores incluyen INF/Nan, el comportamiento del **ejemplo \_ d** podría no coincidir con la instrucción de **ejemplo** , que calcula implícitamente el derivado.</span><span class="sxs-lookup"><span data-stu-id="dab32-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="dab32-135">Los valores INF/NaN pueden afectar al cálculo de LOD de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="dab32-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="dab32-136">La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="dab32-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="dab32-137">Restricciones</span><span class="sxs-lookup"><span data-stu-id="dab32-137">Restrictions</span></span>

-   <span data-ttu-id="dab32-138">el **ejemplo \_ d** hereda las mismas restricciones que la instrucción de **ejemplo** , además de una restricción adicional a continuación para sus parámetros adicionales.</span><span class="sxs-lookup"><span data-stu-id="dab32-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="dab32-139">*srcXDerivatives* y *srcYDerivatives* deben ser Temp (r \# /x \# ), constantBuffer (CB \# ), registros de entrada (v \# ) o valores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="dab32-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="dab32-140">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="dab32-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dab32-141">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="dab32-141">Vertex Shader</span></span> | <span data-ttu-id="dab32-142">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="dab32-142">Geometry Shader</span></span> | <span data-ttu-id="dab32-143">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dab32-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dab32-144">X</span><span class="sxs-lookup"><span data-stu-id="dab32-144">X</span></span>             | <span data-ttu-id="dab32-145">X</span><span class="sxs-lookup"><span data-stu-id="dab32-145">X</span></span>               | <span data-ttu-id="dab32-146">x</span><span class="sxs-lookup"><span data-stu-id="dab32-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dab32-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="dab32-147">Minimum Shader Model</span></span>

<span data-ttu-id="dab32-148">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dab32-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dab32-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dab32-149">Shader Model</span></span>                                              | <span data-ttu-id="dab32-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="dab32-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dab32-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dab32-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dab32-152">sí</span><span class="sxs-lookup"><span data-stu-id="dab32-152">yes</span></span>       |
| [<span data-ttu-id="dab32-153">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dab32-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dab32-154">sí</span><span class="sxs-lookup"><span data-stu-id="dab32-154">yes</span></span>       |
| [<span data-ttu-id="dab32-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dab32-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dab32-156">sí</span><span class="sxs-lookup"><span data-stu-id="dab32-156">yes</span></span>       |
| [<span data-ttu-id="dab32-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dab32-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dab32-158">no</span><span class="sxs-lookup"><span data-stu-id="dab32-158">no</span></span>        |
| [<span data-ttu-id="dab32-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dab32-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dab32-160">no</span><span class="sxs-lookup"><span data-stu-id="dab32-160">no</span></span>        |
| [<span data-ttu-id="dab32-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dab32-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dab32-162">no</span><span class="sxs-lookup"><span data-stu-id="dab32-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dab32-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dab32-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab32-164">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dab32-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





