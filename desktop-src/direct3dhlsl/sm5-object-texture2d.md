---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- HLSL de Texture2D
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/14/2021
ms.locfileid: "104986167"
---
# <a name="texture2d"></a><span data-ttu-id="69cc9-104">Texture2D</span><span class="sxs-lookup"><span data-stu-id="69cc9-104">Texture2D</span></span>

<span data-ttu-id="69cc9-105">Tipo Texture2D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="69cc9-105">Texture2D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="69cc9-106">Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="69cc9-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="69cc9-107">Método</span><span class="sxs-lookup"><span data-stu-id="69cc9-107">Method</span></span>                                                                 | <span data-ttu-id="69cc9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="69cc9-108">Description</span></span>                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69cc9-109">**Recopilar**</span><span class="sxs-lookup"><span data-stu-id="69cc9-109">**Gather**</span></span>](texture2d-gather.md)                                      | <span data-ttu-id="69cc9-110">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="69cc9-110">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>                                                                |
| [<span data-ttu-id="69cc9-111">**GatherRed**</span><span class="sxs-lookup"><span data-stu-id="69cc9-111">**GatherRed**</span></span>](texture2d-gatherred.md)                                | <span data-ttu-id="69cc9-112">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="69cc9-112">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                          |
| [<span data-ttu-id="69cc9-113">**GatherGreen**</span><span class="sxs-lookup"><span data-stu-id="69cc9-113">**GatherGreen**</span></span>](texture2d-gathergreen.md)                            | <span data-ttu-id="69cc9-114">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="69cc9-114">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="69cc9-115">**GatherBlue**</span><span class="sxs-lookup"><span data-stu-id="69cc9-115">**GatherBlue**</span></span>](texture2d-gatherblue.md)                              | <span data-ttu-id="69cc9-116">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="69cc9-116">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                         |
| [<span data-ttu-id="69cc9-117">**GatherAlpha**</span><span class="sxs-lookup"><span data-stu-id="69cc9-117">**GatherAlpha**</span></span>](texture2d-gatheralpha.md)                            | <span data-ttu-id="69cc9-118">Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="69cc9-118">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>                                        |
| [<span data-ttu-id="69cc9-119">**GatherCmp**</span><span class="sxs-lookup"><span data-stu-id="69cc9-119">**GatherCmp**</span></span>](texture2d-gathercmp.md)                                | <span data-ttu-id="69cc9-120">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="69cc9-120">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>                      |
| [<span data-ttu-id="69cc9-121">**GatherCmpRed**</span><span class="sxs-lookup"><span data-stu-id="69cc9-121">**GatherCmpRed**</span></span>](texture2d-gathercmpred.md)                          | <span data-ttu-id="69cc9-122">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="69cc9-122">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>   |
| [<span data-ttu-id="69cc9-123">**GatherCmpGreen**</span><span class="sxs-lookup"><span data-stu-id="69cc9-123">**GatherCmpGreen**</span></span>](texture2d-gathercmpgreen.md)                      | <span data-ttu-id="69cc9-124">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="69cc9-124">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span> |
| [<span data-ttu-id="69cc9-125">**GatherCmpBlue**</span><span class="sxs-lookup"><span data-stu-id="69cc9-125">**GatherCmpBlue**</span></span>](texture2d-gathercmpblue.md)                        | <span data-ttu-id="69cc9-126">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="69cc9-126">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>  |
| [<span data-ttu-id="69cc9-127">**GatherCmpAlpha**</span><span class="sxs-lookup"><span data-stu-id="69cc9-127">**GatherCmpAlpha**</span></span>](texture2d-gathercmpalpha.md)                      | <span data-ttu-id="69cc9-128">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="69cc9-128">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span> |
| [<span data-ttu-id="69cc9-129">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="69cc9-129">**GetDimensions**</span></span>](sm5-object-texture2d-getdimensions.md)             | <span data-ttu-id="69cc9-130">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="69cc9-130">Gets the resource dimensions.</span></span>                                                                                                                       |
| [<span data-ttu-id="69cc9-131">**Carga**</span><span class="sxs-lookup"><span data-stu-id="69cc9-131">**Load**</span></span>](texture2d-load.md)                                          | <span data-ttu-id="69cc9-132">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="69cc9-132">Reads texture data.</span></span>                                                                                                                                 |
| <span data-ttu-id="69cc9-133">[**MIPS. Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="69cc9-133">[**mips.Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="69cc9-134">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69cc9-134">Gets a read-only resource variable.</span></span>                                                                                                                 |
| <span data-ttu-id="69cc9-135">[**Operador\[\]**](sm5-object-texture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="69cc9-135">[**Operator\[\]**](sm5-object-texture2d-operatorindex.md)</span></span>              | <span data-ttu-id="69cc9-136">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69cc9-136">Gets a read-only resource variable.</span></span>                                                                                                                 |
| [<span data-ttu-id="69cc9-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="69cc9-137">**Sample**</span></span>](texture-sample-overload.md)                               | <span data-ttu-id="69cc9-138">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="69cc9-138">Samples a texture.</span></span>                                                                                                                                  |
| [<span data-ttu-id="69cc9-139">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="69cc9-139">**SampleBias**</span></span>](texture2d-samplebias.md)                              | <span data-ttu-id="69cc9-140">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="69cc9-140">Samples a texture, after applying the bias value to the mipmap level.</span></span>                                                                               |
| [<span data-ttu-id="69cc9-141">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="69cc9-141">**SampleCmp**</span></span>](texture2d-samplecmp.md)                                | <span data-ttu-id="69cc9-142">Muestrea una textura con un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="69cc9-142">Samples a texture, using a comparison value to reject samples.</span></span>                                                                                      |
| [<span data-ttu-id="69cc9-143">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="69cc9-143">**SampleCmpLevelZero**</span></span>](texture2d-samplecmplevelzero.md)              | <span data-ttu-id="69cc9-144">Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="69cc9-144">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                                                                |
| [<span data-ttu-id="69cc9-145">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="69cc9-145">**SampleGrad**</span></span>](texture2d-samplegrad.md)                              | <span data-ttu-id="69cc9-146">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="69cc9-146">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>                                                          |
| [<span data-ttu-id="69cc9-147">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="69cc9-147">**SampleLevel**</span></span>](texture2d-samplelevel.md)                            | <span data-ttu-id="69cc9-148">Muestrea una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="69cc9-148">Samples a texture on the specified mipmap level.</span></span>                                                                                                    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69cc9-149">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="69cc9-149">Minimum Shader Model</span></span>

<span data-ttu-id="69cc9-150">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="69cc9-150">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="69cc9-151">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="69cc9-151">Shader Model</span></span>                                                                | <span data-ttu-id="69cc9-152">Compatible</span><span class="sxs-lookup"><span data-stu-id="69cc9-152">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="69cc9-153">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="69cc9-153">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="69cc9-154">sí</span><span class="sxs-lookup"><span data-stu-id="69cc9-154">yes</span></span>       |



 

<span data-ttu-id="69cc9-155">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="69cc9-155">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="69cc9-156">Vértice</span><span class="sxs-lookup"><span data-stu-id="69cc9-156">Vertex</span></span> | <span data-ttu-id="69cc9-157">Casco</span><span class="sxs-lookup"><span data-stu-id="69cc9-157">Hull</span></span> | <span data-ttu-id="69cc9-158">Dominio</span><span class="sxs-lookup"><span data-stu-id="69cc9-158">Domain</span></span> | <span data-ttu-id="69cc9-159">Geometría</span><span class="sxs-lookup"><span data-stu-id="69cc9-159">Geometry</span></span> | <span data-ttu-id="69cc9-160">Píxel</span><span class="sxs-lookup"><span data-stu-id="69cc9-160">Pixel</span></span> | <span data-ttu-id="69cc9-161">Compute</span><span class="sxs-lookup"><span data-stu-id="69cc9-161">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="69cc9-162">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-162">x</span></span>      | <span data-ttu-id="69cc9-163">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-163">x</span></span>    | <span data-ttu-id="69cc9-164">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-164">x</span></span>      | <span data-ttu-id="69cc9-165">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-165">x</span></span>        | <span data-ttu-id="69cc9-166">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-166">x</span></span>     | <span data-ttu-id="69cc9-167">x</span><span class="sxs-lookup"><span data-stu-id="69cc9-167">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="69cc9-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="69cc9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69cc9-169">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="69cc9-169">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




