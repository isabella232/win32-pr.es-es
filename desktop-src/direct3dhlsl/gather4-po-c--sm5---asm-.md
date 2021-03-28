---
title: gather4_po_c (SM5-ASM)
description: Se comporta igual que gather4 \_ Po, excepto que realiza una comparación en textura, de forma similar al ejemplo \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419964"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="2fd7e-103">\_po gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2fd7e-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="2fd7e-104">Se comporta igual que [**gather4 \_ po**](gather4-po--sm5---asm-.md), excepto que realiza una comparación en textura, de forma similar al [**ejemplo \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="2fd7e-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="2fd7e-105">gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="2fd7e-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2fd7e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2fd7e-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="2fd7e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd7e-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2fd7e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="2fd7e-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="2fd7e-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="2fd7e-111">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="2fd7e-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="2fd7e-113">\[en \] el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="2fd7e-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="2fd7e-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="2fd7e-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="2fd7e-117">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="2fd7e-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="2fd7e-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="2fd7e-119">\[en \] componente único seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2fd7e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fd7e-120">Remarks</span></span>

<span data-ttu-id="2fd7e-121">Vea el [**ejemplo \_ c**](sample-c--sm4---asm-.md) para obtener información sobre cómo se compara *srcReferenceValue* con cada textura capturado.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="2fd7e-122">A diferencia del **ejemplo \_ c**, *gather4 \_ po \_ c* devuelve cada resultado de comparación, en lugar de filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="2fd7e-123">Esta instrucción, como **gather4 \_ po**, solo funciona con texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="2fd7e-124">Esto no es lo mismo que [**gather4 \_ c**](gather4-c--sm5---asm-.md), que también funciona con TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="2fd7e-125">En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado o +-INF, se usa en la operación de comparación sin tocar.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="2fd7e-126">NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="2fd7e-127">Las desnormaciones se vacían en cero entrando en la comparación.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="2fd7e-128">En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="2fd7e-129">Los formatos admitidos para **\_ po gather4 \_ c** son los mismos que los que se admiten para el **ejemplo \_ c**.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="2fd7e-130">Son formatos de un solo componente, por lo tanto,. R en srcSampler, en lugar de un swizzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="2fd7e-131">**gather4 \_ po \_ c** en un recurso sin enlazar devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="2fd7e-132">Use este método para el filtrado de mapas de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2fd7e-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="2fd7e-133">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2fd7e-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2fd7e-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="2fd7e-134">Vertex</span></span> | <span data-ttu-id="2fd7e-135">Casco</span><span class="sxs-lookup"><span data-stu-id="2fd7e-135">Hull</span></span> | <span data-ttu-id="2fd7e-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="2fd7e-136">Domain</span></span> | <span data-ttu-id="2fd7e-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="2fd7e-137">Geometry</span></span> | <span data-ttu-id="2fd7e-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="2fd7e-138">Pixel</span></span> | <span data-ttu-id="2fd7e-139">Compute</span><span class="sxs-lookup"><span data-stu-id="2fd7e-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2fd7e-140">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-140">X</span></span>      | <span data-ttu-id="2fd7e-141">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-141">X</span></span>    | <span data-ttu-id="2fd7e-142">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-142">X</span></span>      | <span data-ttu-id="2fd7e-143">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-143">X</span></span>        | <span data-ttu-id="2fd7e-144">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-144">X</span></span>     | <span data-ttu-id="2fd7e-145">X</span><span class="sxs-lookup"><span data-stu-id="2fd7e-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2fd7e-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2fd7e-146">Minimum Shader Model</span></span>

<span data-ttu-id="2fd7e-147">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2fd7e-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2fd7e-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2fd7e-148">Shader Model</span></span>                                              | <span data-ttu-id="2fd7e-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="2fd7e-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2fd7e-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2fd7e-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2fd7e-151">sí</span><span class="sxs-lookup"><span data-stu-id="2fd7e-151">yes</span></span>       |
| [<span data-ttu-id="2fd7e-152">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2fd7e-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2fd7e-153">no</span><span class="sxs-lookup"><span data-stu-id="2fd7e-153">no</span></span>        |
| [<span data-ttu-id="2fd7e-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2fd7e-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2fd7e-155">no</span><span class="sxs-lookup"><span data-stu-id="2fd7e-155">no</span></span>        |
| [<span data-ttu-id="2fd7e-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd7e-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fd7e-157">no</span><span class="sxs-lookup"><span data-stu-id="2fd7e-157">no</span></span>        |
| [<span data-ttu-id="2fd7e-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd7e-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2fd7e-159">no</span><span class="sxs-lookup"><span data-stu-id="2fd7e-159">no</span></span>        |
| [<span data-ttu-id="2fd7e-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd7e-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2fd7e-161">no</span><span class="sxs-lookup"><span data-stu-id="2fd7e-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2fd7e-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fd7e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd7e-163">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fd7e-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





