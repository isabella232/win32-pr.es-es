---
title: sample_c (SM4-ASM)
description: Realiza un filtro de comparación.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996880"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="dfd4a-103">ejemplo \_ c (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dfd4a-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="dfd4a-104">Realiza un filtro de comparación.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="dfd4a-105">el ejemplo \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource. r,//debe ser. r swizzle srcSampler, srcReferenceValue//Single Component seleccionado</span><span class="sxs-lookup"><span data-stu-id="dfd4a-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="dfd4a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfd4a-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="dfd4a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfd4a-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd4a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dfd4a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="dfd4a-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="dfd4a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="dfd4a-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="dfd4a-111">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="dfd4a-112">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd4a-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="dfd4a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="dfd4a-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="dfd4a-114">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-114">\[in\] A texture register.</span></span> <span data-ttu-id="dfd4a-115">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="dfd4a-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="dfd4a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="dfd4a-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="dfd4a-117">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-117">\[in\] A sampler register.</span></span> <span data-ttu-id="dfd4a-118">Para obtener más información, vea la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="dfd4a-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="dfd4a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="dfd4a-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="dfd4a-120">\[en \] un registro con un componente único seleccionado, que se usa en la comparación.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="dfd4a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfd4a-121">Remarks</span></span>

<span data-ttu-id="dfd4a-122">El propósito principal de esta instrucción es proporcionar un bloque de creación para Percentage-Closer filtrado de profundidad.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="dfd4a-123">La "c" en el **ejemplo \_ c** significa comparación.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="dfd4a-124">Los operandos del **ejemplo \_ c** son idénticos a la instrucción de [ejemplo](sample--sm4---asm-.md) , salvo que hay un operando de origen float32 adicional, *srcReferenceValue*, que debe ser un registro con un solo componente seleccionado o un literal escalar.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="dfd4a-125">El parámetro *srcResource* debe tener un swizzle. r (rojo).</span><span class="sxs-lookup"><span data-stu-id="dfd4a-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="dfd4a-126">el **ejemplo \_ c** funciona exclusivamente en el componente rojo y devuelve un valor único.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="dfd4a-127">El swizzle. r en *srcResource* indica que el resultado escalar se replica en todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="dfd4a-128">Cuando se establece un búfer de profundidad como textura de entrada, el valor de profundidad se muestra en el componente rojo.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="dfd4a-129">Si esta instrucción se usa con un recurso que no es Texture1D/2D/2DArray/Cube/CubeArray, genera resultados no definidos.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="dfd4a-130">Cuando se ejecuta esta instrucción, el hardware de muestreo usa el ComparisonFunction de la muestra actual para comparar *srcReferenceValue* con el valor de componente rojo del recurso de origen en cada "TAP" de la ubicación (textura) que el filtro de textura configurado actualmente cubre, en función de las coordenadas proporcionadas en *srcAddress*.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="dfd4a-131">La comparación se produce después de que *srcReferenceValue* se haya cuantificado con la precisión del formato de textura, exactamente de la misma manera que z se cuantifica a la precisión del búfer de profundidad antes de la comparación de profundidad en la prueba de visibilidad de fusión de salida.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="dfd4a-132">Esto incluye una abrazadera al intervalo de formato (por ejemplo, \[ 0.. 1 \] para un formato UNORM).</span><span class="sxs-lookup"><span data-stu-id="dfd4a-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="dfd4a-133">El componente rojo del textura de origen se compara con el *srcReferenceValue* cuantificado.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="dfd4a-134">En el caso de textura que se encuentran fuera del recurso, el valor del componente rojo se determina aplicando los modos de dirección (y BorderColorR si está en el modo de borde) de la muestra.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="dfd4a-135">La comparación admite todas las reglas de comparación de punto flotante de D3D11, en el caso de que el formato de textura sea de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="dfd4a-136">Cada comparación que pasa devuelve 1,0 f como el valor de componente rojo para textura, y cada comparación que produce un error devuelve 0,0 f como el valor rojo de la textura.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="dfd4a-137">A continuación, el filtrado se produce exactamente como lo especifican los Estados de muestra, funcionando solo en el componente rojo y devolver un único resultado de filtro escalar al sombreador, replicado en todos los componentes de *dest* enmascarados.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="dfd4a-138">El uso del **ejemplo \_ c** es ortogonal a todos los demás controles de filtrado de uso general.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="dfd4a-139">el **ejemplo \_ c** funciona sin problemas con los demás modos de filtro de uso general.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="dfd4a-140">el **ejemplo \_ c** cambia el comportamiento de los filtros de uso general, de modo que los valores que se van a filtrar se convierten en 1,0 f o 0.0 f debido a los resultados de la comparación.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="dfd4a-141">La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="dfd4a-142">Para obtener más información, vea la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="dfd4a-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="dfd4a-143">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="dfd4a-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dfd4a-144">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="dfd4a-144">Vertex Shader</span></span> | <span data-ttu-id="dfd4a-145">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="dfd4a-145">Geometry Shader</span></span> | <span data-ttu-id="dfd4a-146">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dfd4a-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="dfd4a-147">x</span><span class="sxs-lookup"><span data-stu-id="dfd4a-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dfd4a-148">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="dfd4a-148">Minimum Shader Model</span></span>

<span data-ttu-id="dfd4a-149">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dfd4a-150">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dfd4a-150">Shader Model</span></span>                                              | <span data-ttu-id="dfd4a-151">Compatible</span><span class="sxs-lookup"><span data-stu-id="dfd4a-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dfd4a-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dfd4a-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dfd4a-153">sí</span><span class="sxs-lookup"><span data-stu-id="dfd4a-153">yes</span></span>       |
| [<span data-ttu-id="dfd4a-154">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dfd4a-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dfd4a-155">sí</span><span class="sxs-lookup"><span data-stu-id="dfd4a-155">yes</span></span>       |
| [<span data-ttu-id="dfd4a-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dfd4a-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dfd4a-157">sí</span><span class="sxs-lookup"><span data-stu-id="dfd4a-157">yes</span></span>       |
| [<span data-ttu-id="dfd4a-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfd4a-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dfd4a-159">no</span><span class="sxs-lookup"><span data-stu-id="dfd4a-159">no</span></span>        |
| [<span data-ttu-id="dfd4a-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfd4a-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dfd4a-161">no</span><span class="sxs-lookup"><span data-stu-id="dfd4a-161">no</span></span>        |
| [<span data-ttu-id="dfd4a-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfd4a-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dfd4a-163">no</span><span class="sxs-lookup"><span data-stu-id="dfd4a-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dfd4a-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfd4a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfd4a-165">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfd4a-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





