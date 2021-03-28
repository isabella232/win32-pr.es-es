---
title: sample_c_lz (SM4-ASM)
description: Realiza un filtro de comparación. Esta instrucción se comporta como ejemplo \_ c, excepto el valor de LOD es 0 y se omiten los derivados.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419923"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="b9021-104">ejemplo \_ \_ de c LZ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b9021-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="b9021-105">Realiza un filtro de comparación.</span><span class="sxs-lookup"><span data-stu-id="b9021-105">Performs a comparison filter.</span></span> <span data-ttu-id="b9021-106">Esta instrucción se comporta como [ejemplo \_ c](sample-c--sm4---asm-.md), excepto el valor de LOD es 0 y se omiten los derivados.</span><span class="sxs-lookup"><span data-stu-id="b9021-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="b9021-107">Sample \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//debe ser. r swizzle srcSampler, srcReferenceValue//Single Component seleccionado</span><span class="sxs-lookup"><span data-stu-id="b9021-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b9021-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9021-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="b9021-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9021-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9021-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b9021-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="b9021-111">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="b9021-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="b9021-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="b9021-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="b9021-113">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b9021-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="b9021-114">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b9021-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="b9021-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="b9021-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="b9021-116">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="b9021-116">\[in\] A texture register.</span></span> <span data-ttu-id="b9021-117">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="b9021-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b9021-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="b9021-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="b9021-119">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="b9021-119">\[in\] A sampler register.</span></span> <span data-ttu-id="b9021-120">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="b9021-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b9021-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="b9021-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="b9021-122">\[en \] un registro con un componente único seleccionado, que se usa en la comparación.</span><span class="sxs-lookup"><span data-stu-id="b9021-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b9021-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9021-123">Remarks</span></span>

<span data-ttu-id="b9021-124">"LZ" representa el nivel cero.</span><span class="sxs-lookup"><span data-stu-id="b9021-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="b9021-125">Dado que se omiten los derivados, esta instrucción está disponible en los sombreadores distintos del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b9021-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="b9021-126">Si esta instrucción se usa con una textura de mipmapped, se muestra el valor de LOD 0, a menos que la muestra tenga una abrazadera LOD que coloque el LOD en alguna otra parte, o bien, si hay una diferencia de LOD, que simplemente afectaría a partir de 0.</span><span class="sxs-lookup"><span data-stu-id="b9021-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="b9021-127">Dado que se omiten los derivados, el filtrado anisotrópico se comporta como filtro anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="b9021-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="b9021-128">En los sombreadores de píxeles, esta instrucción se puede usar dentro del control de flujo variable cuando las coordenadas de textura se derivan en el sombreador, a diferencia del **ejemplo \_ c**.</span><span class="sxs-lookup"><span data-stu-id="b9021-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="b9021-129">La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="b9021-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="b9021-130">Esta instrucción está disponible en todos los sombreadores, no solo en el sombreador de píxeles, por coherencia.</span><span class="sxs-lookup"><span data-stu-id="b9021-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="b9021-131">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b9021-131">Vertex Shader</span></span> | <span data-ttu-id="b9021-132">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="b9021-132">Geometry Shader</span></span> | <span data-ttu-id="b9021-133">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b9021-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b9021-134">X</span><span class="sxs-lookup"><span data-stu-id="b9021-134">X</span></span>             | <span data-ttu-id="b9021-135">X</span><span class="sxs-lookup"><span data-stu-id="b9021-135">X</span></span>               | <span data-ttu-id="b9021-136">x</span><span class="sxs-lookup"><span data-stu-id="b9021-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b9021-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b9021-137">Minimum Shader Model</span></span>

<span data-ttu-id="b9021-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b9021-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b9021-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b9021-139">Shader Model</span></span>                                              | <span data-ttu-id="b9021-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="b9021-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b9021-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b9021-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b9021-142">sí</span><span class="sxs-lookup"><span data-stu-id="b9021-142">yes</span></span>       |
| [<span data-ttu-id="b9021-143">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b9021-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b9021-144">sí</span><span class="sxs-lookup"><span data-stu-id="b9021-144">yes</span></span>       |
| [<span data-ttu-id="b9021-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b9021-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b9021-146">sí</span><span class="sxs-lookup"><span data-stu-id="b9021-146">yes</span></span>       |
| [<span data-ttu-id="b9021-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9021-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b9021-148">no</span><span class="sxs-lookup"><span data-stu-id="b9021-148">no</span></span>        |
| [<span data-ttu-id="b9021-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9021-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b9021-150">no</span><span class="sxs-lookup"><span data-stu-id="b9021-150">no</span></span>        |
| [<span data-ttu-id="b9021-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9021-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b9021-152">no</span><span class="sxs-lookup"><span data-stu-id="b9021-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b9021-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9021-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9021-154">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9021-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





