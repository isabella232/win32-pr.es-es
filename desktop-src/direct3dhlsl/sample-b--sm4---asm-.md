---
title: sample_b (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280129"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="eefa0-104">ejemplo \_ b (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eefa0-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="eefa0-105">Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.</span><span class="sxs-lookup"><span data-stu-id="eefa0-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="eefa0-106">ejemplo \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLODBias. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="eefa0-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="eefa0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="eefa0-107">Item</span></span>                                                                                                               | <span data-ttu-id="eefa0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="eefa0-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefa0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eefa0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="eefa0-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eefa0-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="eefa0-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="eefa0-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="eefa0-112">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="eefa0-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="eefa0-113">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="eefa0-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="eefa0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="eefa0-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="eefa0-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="eefa0-115">\[in\] A texture register.</span></span> <span data-ttu-id="eefa0-116">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="eefa0-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="eefa0-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="eefa0-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="eefa0-118">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="eefa0-118">\[in\] A sampler register.</span></span> <span data-ttu-id="eefa0-119">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="eefa0-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="eefa0-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span><span class="sxs-lookup"><span data-stu-id="eefa0-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="eefa0-121">\[en, \] vea la sección **comentarios** para obtener información sobre este parámetro.</span><span class="sxs-lookup"><span data-stu-id="eefa0-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="eefa0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eefa0-122">Remarks</span></span>

<span data-ttu-id="eefa0-123">Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea de búferes.</span><span class="sxs-lookup"><span data-stu-id="eefa0-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="eefa0-124">Se aplica una desviación adicional al nivel de detalle calculado como parte de la ejecución de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="eefa0-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="eefa0-125">Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) con la adición de la aplicación del valor de *srcLODBias* especificado al nivel de valor detallado calculado como parte de la ejecución de la instrucción antes de seleccionar los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="eefa0-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="eefa0-126">El valor *srcLODBias* se agrega al LOD calculado en cada píxel, junto con el valor MipLODBias de muestra, antes de la abrazadera a MinLOD y MaxLOD.</span><span class="sxs-lookup"><span data-stu-id="eefa0-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="eefa0-127">Restricciones</span><span class="sxs-lookup"><span data-stu-id="eefa0-127">Restrictions</span></span>

-   <span data-ttu-id="eefa0-128">el **ejemplo \_ b** hereda las mismas restricciones que la instrucción de [ejemplo](sample--sm4---asm-.md) , además de restricciones adicionales para su parámetro adicional.</span><span class="sxs-lookup"><span data-stu-id="eefa0-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="eefa0-129">El intervalo de *srcLODBias* es (-16,0 f a 15.99 f); los valores fuera de este intervalo producirán resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="eefa0-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="eefa0-130">*srcLODBias* debe usar un selector de componente único si no es un escalar inmediato.</span><span class="sxs-lookup"><span data-stu-id="eefa0-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="eefa0-131">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="eefa0-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eefa0-132">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="eefa0-132">Vertex Shader</span></span> | <span data-ttu-id="eefa0-133">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="eefa0-133">Geometry Shader</span></span> | <span data-ttu-id="eefa0-134">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="eefa0-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="eefa0-135">x</span><span class="sxs-lookup"><span data-stu-id="eefa0-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eefa0-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="eefa0-136">Minimum Shader Model</span></span>

<span data-ttu-id="eefa0-137">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eefa0-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eefa0-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="eefa0-138">Shader Model</span></span>                                              | <span data-ttu-id="eefa0-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="eefa0-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eefa0-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="eefa0-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eefa0-141">sí</span><span class="sxs-lookup"><span data-stu-id="eefa0-141">yes</span></span>       |
| [<span data-ttu-id="eefa0-142">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="eefa0-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eefa0-143">sí</span><span class="sxs-lookup"><span data-stu-id="eefa0-143">yes</span></span>       |
| [<span data-ttu-id="eefa0-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="eefa0-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eefa0-145">sí</span><span class="sxs-lookup"><span data-stu-id="eefa0-145">yes</span></span>       |
| [<span data-ttu-id="eefa0-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eefa0-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eefa0-147">no</span><span class="sxs-lookup"><span data-stu-id="eefa0-147">no</span></span>        |
| [<span data-ttu-id="eefa0-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eefa0-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eefa0-149">no</span><span class="sxs-lookup"><span data-stu-id="eefa0-149">no</span></span>        |
| [<span data-ttu-id="eefa0-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eefa0-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eefa0-151">no</span><span class="sxs-lookup"><span data-stu-id="eefa0-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eefa0-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eefa0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eefa0-153">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eefa0-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





