---
title: LOD (SM 4.1-ASM)
description: Devuelve el nivel de detalle (LOD) que se utilizaría para el filtrado de textura.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784948"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="f688d-103">LOD (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="f688d-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="f688d-104">Devuelve el nivel de detalle (LOD) que se utilizaría para el filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="f688d-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="f688d-105">LOD dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="f688d-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="f688d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f688d-106">Item</span></span>                                                                                                               | <span data-ttu-id="f688d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f688d-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f688d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f688d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="f688d-109">\[en \] la dirección de los resultados.</span><span class="sxs-lookup"><span data-stu-id="f688d-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="f688d-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f688d-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="f688d-111">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f688d-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="f688d-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f688d-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="f688d-113">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="f688d-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="f688d-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f688d-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="f688d-115">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="f688d-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="f688d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f688d-116">Remarks</span></span>

<span data-ttu-id="f688d-117">Esto se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado.</span><span class="sxs-lookup"><span data-stu-id="f688d-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="f688d-118">La instrucción calcula el vector siguiente (ClampedLOD, NonClampedLOD, 0,0).</span><span class="sxs-lookup"><span data-stu-id="f688d-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="f688d-119">NonClampedLOD es un valor de LOD calculado que omite cualquier fijación de la muestra o la textura (es decir, puede devolver valores negativos). ClampedLOD es un valor de LOD calculado que utilizaría la instrucción de **ejemplo** real.</span><span class="sxs-lookup"><span data-stu-id="f688d-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="f688d-120">Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.</span><span class="sxs-lookup"><span data-stu-id="f688d-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="f688d-121">Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="f688d-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="f688d-122">Si el muestreador usa el filtrado anisotrópico, el LOD debe corresponder al nivel de MIP fraccionario basado en el eje más pequeño de la superficie elíptica.</span><span class="sxs-lookup"><span data-stu-id="f688d-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="f688d-123">Esto es válido para los tipos de textura siguientes: Texture1D, Texture2D, Texture3D y TextureCube.</span><span class="sxs-lookup"><span data-stu-id="f688d-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="f688d-124">La instrucción **LOD** no se define cuando se usa con un muestreador que especifica el filtrado del punto MIP, en concreto, cualquier \_ enumeración de filtro D3D10 que termine en el \_ punto MIP.</span><span class="sxs-lookup"><span data-stu-id="f688d-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="f688d-125">(Un ejemplo sería D3D10 \_ FILTRAr el \_ \_ \_ punto de MIP mínimo \_</span><span class="sxs-lookup"><span data-stu-id="f688d-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="f688d-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f688d-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f688d-127">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f688d-127">Vertex Shader</span></span> | <span data-ttu-id="f688d-128">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f688d-128">Geometry Shader</span></span> | <span data-ttu-id="f688d-129">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f688d-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="f688d-130">x</span><span class="sxs-lookup"><span data-stu-id="f688d-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f688d-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f688d-131">Minimum Shader Model</span></span>

<span data-ttu-id="f688d-132">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f688d-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f688d-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f688d-133">Shader Model</span></span>                                              | <span data-ttu-id="f688d-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="f688d-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f688d-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f688d-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f688d-136">sí</span><span class="sxs-lookup"><span data-stu-id="f688d-136">yes</span></span>       |
| [<span data-ttu-id="f688d-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f688d-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f688d-138">sí</span><span class="sxs-lookup"><span data-stu-id="f688d-138">yes</span></span>       |
| [<span data-ttu-id="f688d-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f688d-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f688d-140">no</span><span class="sxs-lookup"><span data-stu-id="f688d-140">no</span></span>        |
| [<span data-ttu-id="f688d-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f688d-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f688d-142">no</span><span class="sxs-lookup"><span data-stu-id="f688d-142">no</span></span>        |
| [<span data-ttu-id="f688d-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f688d-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f688d-144">no</span><span class="sxs-lookup"><span data-stu-id="f688d-144">no</span></span>        |
| [<span data-ttu-id="f688d-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f688d-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f688d-146">no</span><span class="sxs-lookup"><span data-stu-id="f688d-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f688d-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f688d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f688d-148">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f688d-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





