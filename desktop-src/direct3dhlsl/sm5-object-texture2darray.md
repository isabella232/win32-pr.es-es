---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- HLSL de Texture2DArray
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104986159"
---
# <a name="texture2darray"></a><span data-ttu-id="6d072-104">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="6d072-104">Texture2DArray</span></span>

<span data-ttu-id="6d072-105">Tipo Texture2DArray ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="6d072-105">Texture2DArray type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="6d072-106">Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="6d072-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="6d072-107">Método</span><span class="sxs-lookup"><span data-stu-id="6d072-107">Method</span></span>                                                                      | <span data-ttu-id="6d072-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d072-108">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d072-109">**Recopilar**</span><span class="sxs-lookup"><span data-stu-id="6d072-109">**Gather**</span></span>](texture2darray-gather.md)                                      | <span data-ttu-id="6d072-110">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6d072-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="6d072-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="6d072-111">**GatherRed**</span></span>](texture2darray-gatherred.md)                                | <span data-ttu-id="6d072-112">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6d072-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="6d072-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="6d072-113">**GatherGreen**</span></span>](texture2darray-gathergreen.md)                            | <span data-ttu-id="6d072-114">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6d072-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="6d072-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="6d072-115">**GatherBlue**</span></span>](texture2darray-gatherblue.md)                              | <span data-ttu-id="6d072-116">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6d072-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="6d072-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="6d072-117">**GatherAlpha**</span></span>](texture2darray-gatheralpha.md)                            | <span data-ttu-id="6d072-118">Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6d072-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="6d072-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="6d072-119">**GatherCmp**</span></span>](texture2darray-gathercmp.md)                                | <span data-ttu-id="6d072-120">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6d072-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="6d072-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="6d072-121">**GatherCmpRed**</span></span>](texture2darray-gathercmpred.md)                          | <span data-ttu-id="6d072-122">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6d072-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="6d072-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="6d072-123">**GatherCmpGreen**</span></span>](texture2darray-gathercmpgreen.md)                      | <span data-ttu-id="6d072-124">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6d072-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="6d072-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="6d072-125">**GatherCmpBlue**</span></span>](texture2darray-gathercmpblue.md)                        | <span data-ttu-id="6d072-126">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6d072-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="6d072-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="6d072-127">**GatherCmpAlpha**</span></span>](texture2darray-gathercmpalpha.md)                      | <span data-ttu-id="6d072-128">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6d072-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="6d072-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="6d072-129">**GetDimensions**</span></span>](sm5-object-texture2darray-getdimensions.md)             | <span data-ttu-id="6d072-130">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d072-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="6d072-131">**Carga**</span><span class="sxs-lookup"><span data-stu-id="6d072-131">**Load**</span></span>](texture2darray-load.md)                                          | <span data-ttu-id="6d072-132">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="6d072-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="6d072-133">[**MIPS. Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="6d072-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md)</span></span> | <span data-ttu-id="6d072-134">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d072-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="6d072-135">[**Operador\[\]**](sm5-object-texture2darray-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="6d072-135">[**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)</span></span>              | <span data-ttu-id="6d072-136">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d072-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="6d072-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6d072-137">**Sample**</span></span>](texture2darray-sample.md)                                      | <span data-ttu-id="6d072-138">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="6d072-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="6d072-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="6d072-139">**SampleBias**</span></span>](texture2darray-samplebias.md)                              | <span data-ttu-id="6d072-140">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="6d072-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="6d072-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="6d072-141">**SampleCmp**</span></span>](texture2darray-samplecmp.md)                                | <span data-ttu-id="6d072-142">Muestrea una textura con un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6d072-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="6d072-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="6d072-143">**SampleCmpLevelZero**</span></span>](texture2darray-samplecmplevelzero.md)              | <span data-ttu-id="6d072-144">Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6d072-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="6d072-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="6d072-145">**SampleGrad**</span></span>](texture2darray-samplegrad.md)                              | <span data-ttu-id="6d072-146">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="6d072-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="6d072-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="6d072-147">**SampleLevel**</span></span>](texture2darray-samplelevel.md)                            | <span data-ttu-id="6d072-148">Muestrea una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="6d072-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6d072-149">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6d072-149">Minimum Shader Model</span></span>

<span data-ttu-id="6d072-150">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6d072-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6d072-151">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6d072-151">Shader Model</span></span>                                                                | <span data-ttu-id="6d072-152">Compatible</span><span class="sxs-lookup"><span data-stu-id="6d072-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6d072-153">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="6d072-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6d072-154">sí</span><span class="sxs-lookup"><span data-stu-id="6d072-154">yes</span></span>       |



 

<span data-ttu-id="6d072-155">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6d072-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6d072-156">Vértice</span><span class="sxs-lookup"><span data-stu-id="6d072-156">Vertex</span></span> | <span data-ttu-id="6d072-157">Casco</span><span class="sxs-lookup"><span data-stu-id="6d072-157">Hull</span></span> | <span data-ttu-id="6d072-158">Dominio</span><span class="sxs-lookup"><span data-stu-id="6d072-158">Domain</span></span> | <span data-ttu-id="6d072-159">Geometría</span><span class="sxs-lookup"><span data-stu-id="6d072-159">Geometry</span></span> | <span data-ttu-id="6d072-160">Píxel</span><span class="sxs-lookup"><span data-stu-id="6d072-160">Pixel</span></span> | <span data-ttu-id="6d072-161">Compute</span><span class="sxs-lookup"><span data-stu-id="6d072-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d072-162">x</span><span class="sxs-lookup"><span data-stu-id="6d072-162">x</span></span>      | <span data-ttu-id="6d072-163">x</span><span class="sxs-lookup"><span data-stu-id="6d072-163">x</span></span>    | <span data-ttu-id="6d072-164">x</span><span class="sxs-lookup"><span data-stu-id="6d072-164">x</span></span>      | <span data-ttu-id="6d072-165">x</span><span class="sxs-lookup"><span data-stu-id="6d072-165">x</span></span>        | <span data-ttu-id="6d072-166">x</span><span class="sxs-lookup"><span data-stu-id="6d072-166">x</span></span>     | <span data-ttu-id="6d072-167">x</span><span class="sxs-lookup"><span data-stu-id="6d072-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6d072-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d072-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d072-169">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6d072-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




