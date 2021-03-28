---
title: Objeto TextureCubeArray
description: Tipo TextureCubeArray (tal como existe en el modelo de sombreador 4) más las variables de recurso. Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- HLSL del objeto TextureCubeArray
- HLSL del objeto TextureCubeArray, descrito
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104997989"
---
# <a name="texturecubearray-object"></a><span data-ttu-id="2b69e-106">Objeto TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2b69e-106">TextureCubeArray object</span></span>

<span data-ttu-id="2b69e-107">Tipo **TextureCubeArray** ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="2b69e-107">**TextureCubeArray** type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="2b69e-108">Este objeto de textura admite estos métodos además de los métodos del modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="2b69e-108">This texture object supports these methods in addition to the methods in Shader Model 4.</span></span>

-   [<span data-ttu-id="2b69e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b69e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b69e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b69e-110">Methods</span></span>

<span data-ttu-id="2b69e-111">El objeto **TextureCubeArray** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2b69e-111">The **TextureCubeArray** object has these methods.</span></span>



| <span data-ttu-id="2b69e-112">Método</span><span class="sxs-lookup"><span data-stu-id="2b69e-112">Method</span></span>                                                           | <span data-ttu-id="2b69e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b69e-113">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b69e-114">**Recopilar**</span><span class="sxs-lookup"><span data-stu-id="2b69e-114">**Gather**</span></span>](texturecubearray-gather.md)                         | <span data-ttu-id="2b69e-115">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="2b69e-115">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                                                |
| [<span data-ttu-id="2b69e-116">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="2b69e-116">**GatherAlpha**</span></span>](texturecubearray-gatheralpha.md)               | <span data-ttu-id="2b69e-117">Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="2b69e-117">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="2b69e-118">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="2b69e-118">**GatherBlue**</span></span>](texturecubearray-gatherblue.md)                 | <span data-ttu-id="2b69e-119">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="2b69e-119">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                         |
| [<span data-ttu-id="2b69e-120">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="2b69e-120">**GatherCmp**</span></span>](texturecubearray-gathercmp.md)                   | <span data-ttu-id="2b69e-121">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="2b69e-121">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span><br/>                      |
| [<span data-ttu-id="2b69e-122">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="2b69e-122">**GatherCmpAlpha**</span></span>](texturecubearray-gathercmpalpha.md)         | <span data-ttu-id="2b69e-123">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="2b69e-123">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span><br/> |
| [<span data-ttu-id="2b69e-124">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="2b69e-124">**GatherCmpBlue**</span></span>](texturecubearray-gathercmpblue.md)           | <span data-ttu-id="2b69e-125">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="2b69e-125">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span><br/>  |
| [<span data-ttu-id="2b69e-126">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="2b69e-126">**GatherCmpGreen**</span></span>](texturecubearray-gathercmpgreen.md)         | <span data-ttu-id="2b69e-127">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="2b69e-127">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span><br/> |
| [<span data-ttu-id="2b69e-128">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="2b69e-128">**GatherCmpRed**</span></span>](texturecubearray-gathercmpred.md)             | <span data-ttu-id="2b69e-129">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="2b69e-129">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span><br/>   |
| [<span data-ttu-id="2b69e-130">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="2b69e-130">**GatherGreen**</span></span>](texturecubearray-gathergreen.md)               | <span data-ttu-id="2b69e-131">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="2b69e-131">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                        |
| [<span data-ttu-id="2b69e-132">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="2b69e-132">**GatherRed**</span></span>](texturecubearray-gatherred.md)                   | <span data-ttu-id="2b69e-133">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="2b69e-133">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                          |
| [<span data-ttu-id="2b69e-134">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2b69e-134">**Sample**</span></span>](texturecubearray-sample.md)                         | <span data-ttu-id="2b69e-135">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="2b69e-135">Samples a texture.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="2b69e-136">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="2b69e-136">**SampleBias**</span></span>](texturecubearray-samplebias.md)                 | <span data-ttu-id="2b69e-137">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="2b69e-137">Samples a texture, after applying the bias value to the mipmap level.</span></span><br/>                                                                               |
| [<span data-ttu-id="2b69e-138">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="2b69e-138">**SampleCmp**</span></span>](texturecubearray-samplecmp.md)                   | <span data-ttu-id="2b69e-139">Muestrea una textura con un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="2b69e-139">Samples a texture, using a comparison value to reject samples.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2b69e-140">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="2b69e-140">**SampleCmpLevelZero**</span></span>](texturecubearray-samplecmplevelzero.md) | <span data-ttu-id="2b69e-141">Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="2b69e-141">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span><br/>                                                                |
| [<span data-ttu-id="2b69e-142">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="2b69e-142">**SampleGrad**</span></span>](texturecubearray-samplegrad.md)                 | <span data-ttu-id="2b69e-143">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2b69e-143">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span><br/>                                                          |
| [<span data-ttu-id="2b69e-144">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="2b69e-144">**SampleLevel**</span></span>](texturecubearray-samplelevel.md)               | <span data-ttu-id="2b69e-145">Muestrea una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="2b69e-145">Samples a texture on the specified mipmap level.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="2b69e-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b69e-146">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2b69e-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2b69e-147">Minimum Shader Model</span></span>

<span data-ttu-id="2b69e-148">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2b69e-148">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="2b69e-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2b69e-149">Shader Model</span></span>                                                                | <span data-ttu-id="2b69e-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="2b69e-150">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2b69e-151">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="2b69e-151">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2b69e-152">sí</span><span class="sxs-lookup"><span data-stu-id="2b69e-152">yes</span></span>       |



 

<span data-ttu-id="2b69e-153">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2b69e-153">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2b69e-154">Vértice</span><span class="sxs-lookup"><span data-stu-id="2b69e-154">Vertex</span></span> | <span data-ttu-id="2b69e-155">Casco</span><span class="sxs-lookup"><span data-stu-id="2b69e-155">Hull</span></span> | <span data-ttu-id="2b69e-156">Dominio</span><span class="sxs-lookup"><span data-stu-id="2b69e-156">Domain</span></span> | <span data-ttu-id="2b69e-157">Geometría</span><span class="sxs-lookup"><span data-stu-id="2b69e-157">Geometry</span></span> | <span data-ttu-id="2b69e-158">Píxel</span><span class="sxs-lookup"><span data-stu-id="2b69e-158">Pixel</span></span> | <span data-ttu-id="2b69e-159">Compute</span><span class="sxs-lookup"><span data-stu-id="2b69e-159">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b69e-160">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-160">x</span></span>      | <span data-ttu-id="2b69e-161">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-161">x</span></span>    | <span data-ttu-id="2b69e-162">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-162">x</span></span>      | <span data-ttu-id="2b69e-163">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-163">x</span></span>        | <span data-ttu-id="2b69e-164">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-164">x</span></span>     | <span data-ttu-id="2b69e-165">x</span><span class="sxs-lookup"><span data-stu-id="2b69e-165">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2b69e-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b69e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b69e-167">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2b69e-167">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





