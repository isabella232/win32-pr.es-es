---
title: gather4_c (SM5-ASM)
description: Igual que gather4, salvo que esta inestación realiza una comparación en textura, similar al ejemplo \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996936"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="f9ec9-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="f9ec9-104">Igual que [**gather4**](gather4--sm5---asm-.md), salvo que esta inestación realiza una comparación en textura, similar al [**ejemplo \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec9-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="f9ec9-105">gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="f9ec9-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f9ec9-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9ec9-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="f9ec9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9ec9-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ec9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f9ec9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="f9ec9-109">\[en \] la dirección del resultado de la operación</span><span class="sxs-lookup"><span data-stu-id="f9ec9-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="f9ec9-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="f9ec9-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="f9ec9-111">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="f9ec9-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="f9ec9-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="f9ec9-113">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="f9ec9-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="f9ec9-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="f9ec9-115">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="f9ec9-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="f9ec9-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="f9ec9-117">\[en \] un registro con un componente único seleccionado, que se usa en la comparación.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9ec9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9ec9-118">Remarks</span></span>

<span data-ttu-id="f9ec9-119">Vea el [**ejemplo \_ c**](sample-c--sm4---asm-.md) para obtener una descripción de cómo se compara *srcReferenceValue* con cada textura capturado.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="f9ec9-120">A diferencia del **ejemplo \_ c**, **gather4 \_ c** devuelve cada resultado de comparación, en lugar de filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="f9ec9-121">En el caso de las esquinas TextureCube, donde hay tres textura reales y un cuarto se deben sintetizar, la síntesis debe aparecer después del paso de comparación.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="f9ec9-122">Esto significa que el resultado de la comparación devuelto para syntesized textura puede ser 0, 0,33, 0,66 o 1.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="f9ec9-123">Algunas implementaciones solo pueden devolver 0 o 1 para el textura sintetizado.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="f9ec9-124">Además de esta lista de resultados posibles, no se especifica el método para sintetizar el textura.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="f9ec9-125">En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado o +-INF, se usa en la operación de comparación sin tocar.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="f9ec9-126">NaN se usa en la operación de comparación como NaN, pero se puede cambiar la representación de bits exacta del NaN.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="f9ec9-127">Las desnormaciones se vacían en cero entrando en la comparación.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="f9ec9-128">En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para la textura sintetizada.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="f9ec9-129">Los formatos admitidos para *gather4 \_ c* son los mismos que los que se admiten para el *ejemplo \_ c*.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="f9ec9-130">Son formatos de un solo componente, por lo tanto,. R en *srcSampler*, en lugar de un swizzle arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="f9ec9-131">**gather4 \_ c** en un recurso sin enlazar devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="f9ec9-132">Use esta instrucción para el filtrado de mapa de instantáneas personalizado.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="f9ec9-133">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f9ec9-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f9ec9-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="f9ec9-134">Vertex</span></span> | <span data-ttu-id="f9ec9-135">Casco</span><span class="sxs-lookup"><span data-stu-id="f9ec9-135">Hull</span></span> | <span data-ttu-id="f9ec9-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="f9ec9-136">Domain</span></span> | <span data-ttu-id="f9ec9-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="f9ec9-137">Geometry</span></span> | <span data-ttu-id="f9ec9-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="f9ec9-138">Pixel</span></span> | <span data-ttu-id="f9ec9-139">Compute</span><span class="sxs-lookup"><span data-stu-id="f9ec9-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f9ec9-140">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-140">X</span></span>      | <span data-ttu-id="f9ec9-141">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-141">X</span></span>    | <span data-ttu-id="f9ec9-142">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-142">X</span></span>      | <span data-ttu-id="f9ec9-143">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-143">X</span></span>        | <span data-ttu-id="f9ec9-144">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-144">X</span></span>     | <span data-ttu-id="f9ec9-145">X</span><span class="sxs-lookup"><span data-stu-id="f9ec9-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f9ec9-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f9ec9-146">Minimum Shader Model</span></span>

<span data-ttu-id="f9ec9-147">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f9ec9-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f9ec9-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f9ec9-148">Shader Model</span></span>                                              | <span data-ttu-id="f9ec9-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="f9ec9-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f9ec9-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f9ec9-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f9ec9-151">sí</span><span class="sxs-lookup"><span data-stu-id="f9ec9-151">yes</span></span>       |
| [<span data-ttu-id="f9ec9-152">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f9ec9-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f9ec9-153">no</span><span class="sxs-lookup"><span data-stu-id="f9ec9-153">no</span></span>        |
| [<span data-ttu-id="f9ec9-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f9ec9-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f9ec9-155">no</span><span class="sxs-lookup"><span data-stu-id="f9ec9-155">no</span></span>        |
| [<span data-ttu-id="f9ec9-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f9ec9-157">no</span><span class="sxs-lookup"><span data-stu-id="f9ec9-157">no</span></span>        |
| [<span data-ttu-id="f9ec9-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f9ec9-159">no</span><span class="sxs-lookup"><span data-stu-id="f9ec9-159">no</span></span>        |
| [<span data-ttu-id="f9ec9-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f9ec9-161">no</span><span class="sxs-lookup"><span data-stu-id="f9ec9-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f9ec9-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9ec9-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9ec9-163">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





