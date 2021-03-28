---
title: gather4_po (SM5-ASM)
description: Una variante de gather4, pero en lugar de admitir un desplazamiento inmediato \-8.. 7 \, el desplazamiento viene como parámetro de la instrucción y también tiene un intervalo mayor de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983874"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="42ff1-103">\_po gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="42ff1-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="42ff1-104">Una variante de [gather4](gather4--sm5---asm-.md), pero en lugar de admitir un desplazamiento inmediato \[ -8.. 7 \] , el desplazamiento viene como parámetro de la instrucción y también tiene un intervalo mayor de \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="42ff1-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="42ff1-105">gather4 \_ po dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcOffset \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="42ff1-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="42ff1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="42ff1-106">Item</span></span>                                                                                                               | <span data-ttu-id="42ff1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="42ff1-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="42ff1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="42ff1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="42ff1-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="42ff1-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="42ff1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="42ff1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="42ff1-111">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="42ff1-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="42ff1-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="42ff1-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="42ff1-113">\[en \] el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="42ff1-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="42ff1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="42ff1-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="42ff1-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="42ff1-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="42ff1-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="42ff1-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="42ff1-117">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="42ff1-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="42ff1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42ff1-118">Remarks</span></span>

<span data-ttu-id="42ff1-119">Los dos primeros componentes del parámetro de desplazamiento de 4 vectores proporcionan desplazamientos de enteros de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42ff1-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="42ff1-120">Los demás componentes de este parámetro se omiten.</span><span class="sxs-lookup"><span data-stu-id="42ff1-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="42ff1-121">Los 6 bits menos significativos de cada valor de desplazamiento se admiten como un valor con signo, lo que produce un \[ intervalo de-32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="42ff1-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="42ff1-122">Esta instrucción solo funciona con texturas 2D, a diferencia de **gather4**, que también funciona con TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="42ff1-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="42ff1-123">Los únicos modos que se respetan en la muestra son los modos de direccionamiento.</span><span class="sxs-lookup"><span data-stu-id="42ff1-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="42ff1-124">Solo se utiliza el MIP más detallado en la vista de recursos.</span><span class="sxs-lookup"><span data-stu-id="42ff1-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="42ff1-125">Si la dirección se encuentra en un centro de textura, esto no significa que el otro textura se pueda poner a cero.</span><span class="sxs-lookup"><span data-stu-id="42ff1-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="42ff1-126">El parámetro *srcSampler* incluye el \[ componente. Select \_ \] , lo que permite recuperar cualquier componente individual de una textura, incluida la devolución de valores predeterminados para los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="42ff1-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="42ff1-127">En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar.</span><span class="sxs-lookup"><span data-stu-id="42ff1-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="42ff1-128">NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN.</span><span class="sxs-lookup"><span data-stu-id="42ff1-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="42ff1-129">En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada, y se pueden vaciar las denormalidades.</span><span class="sxs-lookup"><span data-stu-id="42ff1-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="42ff1-130">Use esta instrucción para extender el intervalo de desplazamiento de **gather4** de forma que sea más grande y programable.</span><span class="sxs-lookup"><span data-stu-id="42ff1-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="42ff1-131">El sufijo "PO" en el nombre significa "desplazamiento programable".</span><span class="sxs-lookup"><span data-stu-id="42ff1-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="42ff1-132">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="42ff1-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="42ff1-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="42ff1-133">Vertex</span></span> | <span data-ttu-id="42ff1-134">Casco</span><span class="sxs-lookup"><span data-stu-id="42ff1-134">Hull</span></span> | <span data-ttu-id="42ff1-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="42ff1-135">Domain</span></span> | <span data-ttu-id="42ff1-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="42ff1-136">Geometry</span></span> | <span data-ttu-id="42ff1-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="42ff1-137">Pixel</span></span> | <span data-ttu-id="42ff1-138">Compute</span><span class="sxs-lookup"><span data-stu-id="42ff1-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42ff1-139">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-139">X</span></span>      | <span data-ttu-id="42ff1-140">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-140">X</span></span>    | <span data-ttu-id="42ff1-141">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-141">X</span></span>      | <span data-ttu-id="42ff1-142">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-142">X</span></span>        | <span data-ttu-id="42ff1-143">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-143">X</span></span>     | <span data-ttu-id="42ff1-144">X</span><span class="sxs-lookup"><span data-stu-id="42ff1-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42ff1-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="42ff1-145">Minimum Shader Model</span></span>

<span data-ttu-id="42ff1-146">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="42ff1-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="42ff1-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="42ff1-147">Shader Model</span></span>                                              | <span data-ttu-id="42ff1-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="42ff1-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="42ff1-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42ff1-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="42ff1-150">sí</span><span class="sxs-lookup"><span data-stu-id="42ff1-150">yes</span></span>       |
| [<span data-ttu-id="42ff1-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="42ff1-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="42ff1-152">no</span><span class="sxs-lookup"><span data-stu-id="42ff1-152">no</span></span>        |
| [<span data-ttu-id="42ff1-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="42ff1-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="42ff1-154">no</span><span class="sxs-lookup"><span data-stu-id="42ff1-154">no</span></span>        |
| [<span data-ttu-id="42ff1-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42ff1-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="42ff1-156">no</span><span class="sxs-lookup"><span data-stu-id="42ff1-156">no</span></span>        |
| [<span data-ttu-id="42ff1-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42ff1-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="42ff1-158">no</span><span class="sxs-lookup"><span data-stu-id="42ff1-158">no</span></span>        |
| [<span data-ttu-id="42ff1-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42ff1-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="42ff1-160">no</span><span class="sxs-lookup"><span data-stu-id="42ff1-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="42ff1-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42ff1-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42ff1-162">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42ff1-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





