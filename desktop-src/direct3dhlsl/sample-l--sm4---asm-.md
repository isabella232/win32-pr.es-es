---
title: sample_l (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362271"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="8d48f-104">ejemplo \_ l (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d48f-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="8d48f-105">Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.</span><span class="sxs-lookup"><span data-stu-id="8d48f-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="8d48f-106">Sample \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLOD. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="8d48f-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="8d48f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d48f-107">Item</span></span>                                                                                                               | <span data-ttu-id="8d48f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d48f-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d48f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8d48f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="8d48f-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="8d48f-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="8d48f-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="8d48f-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="8d48f-112">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8d48f-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="8d48f-113">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="8d48f-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="8d48f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="8d48f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="8d48f-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="8d48f-115">\[in\] A texture register.</span></span> <span data-ttu-id="8d48f-116">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="8d48f-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="8d48f-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="8d48f-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="8d48f-118">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="8d48f-118">\[in\] A sampler register.</span></span> <span data-ttu-id="8d48f-119">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="8d48f-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="8d48f-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span><span class="sxs-lookup"><span data-stu-id="8d48f-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="8d48f-121">\[en \] LOD.</span><span class="sxs-lookup"><span data-stu-id="8d48f-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8d48f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d48f-122">Remarks</span></span>

<span data-ttu-id="8d48f-123">Esta instrucción es idéntica a [Sample](sample--sm4---asm-.md), salvo que la aplicación proporciona directamente el LOD como un valor escalar, que no representa ningún anisotropía.</span><span class="sxs-lookup"><span data-stu-id="8d48f-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="8d48f-124">Esta instrucción está disponible en todas las etapas del sombreador de progammable.</span><span class="sxs-lookup"><span data-stu-id="8d48f-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="8d48f-125">**ejemplos \_ l muestra** la textura mediante *srcLOD* para que sea el LOD.</span><span class="sxs-lookup"><span data-stu-id="8d48f-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="8d48f-126">Si el valor de LOD es <= 0, se elige zero'th (el mapa más grande), con el filtro de ampliación aplicado (si procede según el modo de filtro).</span><span class="sxs-lookup"><span data-stu-id="8d48f-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="8d48f-127">Dado que *srcLOD* es un valor de punto flotante, el valor fraccionario se usa para interpolar entre dos niveles de MIP, si el filtro minimizar es lineal o con filtrado anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="8d48f-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="8d48f-128">el **ejemplo \_ l** omite las derivadas de la dirección, por lo que el comportamiento del filtrado es puramente anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="8d48f-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="8d48f-129">Dado que se omiten los derivados, el filtrado anisotrópico se comporta como filtro anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="8d48f-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="8d48f-130">Se respetan los Estados de muestra MIPLODBIAS y MAX/MINMIPLEVEL.</span><span class="sxs-lookup"><span data-stu-id="8d48f-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="8d48f-131">Cuando se usa en el sombreador de píxeles, **Sample \_ l** implica que la elección de LOD es por píxel, sin ningún efecto de los píxeles adyacentes, por ejemplo en la misma marca de 2x2.</span><span class="sxs-lookup"><span data-stu-id="8d48f-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="8d48f-132">La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="8d48f-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="8d48f-133">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8d48f-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d48f-134">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8d48f-134">Vertex Shader</span></span> | <span data-ttu-id="8d48f-135">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8d48f-135">Geometry Shader</span></span> | <span data-ttu-id="8d48f-136">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8d48f-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8d48f-137">X</span><span class="sxs-lookup"><span data-stu-id="8d48f-137">X</span></span>             | <span data-ttu-id="8d48f-138">X</span><span class="sxs-lookup"><span data-stu-id="8d48f-138">X</span></span>               | <span data-ttu-id="8d48f-139">x</span><span class="sxs-lookup"><span data-stu-id="8d48f-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d48f-140">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8d48f-140">Minimum Shader Model</span></span>

<span data-ttu-id="8d48f-141">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8d48f-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d48f-142">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8d48f-142">Shader Model</span></span>                                              | <span data-ttu-id="8d48f-143">Compatible</span><span class="sxs-lookup"><span data-stu-id="8d48f-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d48f-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8d48f-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d48f-145">sí</span><span class="sxs-lookup"><span data-stu-id="8d48f-145">yes</span></span>       |
| [<span data-ttu-id="8d48f-146">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8d48f-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d48f-147">sí</span><span class="sxs-lookup"><span data-stu-id="8d48f-147">yes</span></span>       |
| [<span data-ttu-id="8d48f-148">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8d48f-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d48f-149">sí</span><span class="sxs-lookup"><span data-stu-id="8d48f-149">yes</span></span>       |
| [<span data-ttu-id="8d48f-150">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d48f-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d48f-151">no</span><span class="sxs-lookup"><span data-stu-id="8d48f-151">no</span></span>        |
| [<span data-ttu-id="8d48f-152">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d48f-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d48f-153">no</span><span class="sxs-lookup"><span data-stu-id="8d48f-153">no</span></span>        |
| [<span data-ttu-id="8d48f-154">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d48f-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d48f-155">no</span><span class="sxs-lookup"><span data-stu-id="8d48f-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d48f-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d48f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d48f-157">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d48f-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





