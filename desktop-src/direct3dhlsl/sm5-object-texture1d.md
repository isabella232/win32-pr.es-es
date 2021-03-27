---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- HLSL de Texture1D
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994757"
---
# <a name="texture1d"></a><span data-ttu-id="42a7e-104">Texture1D</span><span class="sxs-lookup"><span data-stu-id="42a7e-104">Texture1D</span></span>

<span data-ttu-id="42a7e-105">Un tipo de textura 1D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="42a7e-105">A 1D texture type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="42a7e-106">Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="42a7e-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="42a7e-107">Método</span><span class="sxs-lookup"><span data-stu-id="42a7e-107">Method</span></span>                                                                  | <span data-ttu-id="42a7e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="42a7e-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42a7e-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="42a7e-109">**GetDimensions**</span></span>](sm5-object-texture1d-getdimensions.md)             | <span data-ttu-id="42a7e-110">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="42a7e-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="42a7e-111">**Carga**</span><span class="sxs-lookup"><span data-stu-id="42a7e-111">**Load**</span></span>](texture1d-load.md)                                          | <span data-ttu-id="42a7e-112">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="42a7e-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="42a7e-113">[**Operador\[\]**](sm5-object-texture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="42a7e-113">[**Operator\[\]**](sm5-object-texture1d-operatorindex.md)</span></span>              | <span data-ttu-id="42a7e-114">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42a7e-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="42a7e-115">[**MIPS. Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="42a7e-115">[**mips.Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="42a7e-116">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="42a7e-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="42a7e-117">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="42a7e-117">**Sample**</span></span>](texture1d-sample.md)                                      | <span data-ttu-id="42a7e-118">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="42a7e-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="42a7e-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="42a7e-119">**SampleBias**</span></span>](texture1d-samplebias.md)                              | <span data-ttu-id="42a7e-120">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="42a7e-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="42a7e-121">**SampleCmp**</span><span class="sxs-lookup"><span data-stu-id="42a7e-121">**SampleCmp**</span></span>](texture1d-samplecmp.md)                                | <span data-ttu-id="42a7e-122">Muestrea una textura con un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="42a7e-122">Samples a texture, using a comparison value to reject samples.</span></span>                             |
| [<span data-ttu-id="42a7e-123">**SampleCmpLevelZero**</span><span class="sxs-lookup"><span data-stu-id="42a7e-123">**SampleCmpLevelZero**</span></span>](texture1d-samplecmplevelzero.md)              | <span data-ttu-id="42a7e-124">Muestrea una textura (solo el nivel de mipmap 0), utilizando un valor de comparación para rechazar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="42a7e-124">Samples a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>       |
| [<span data-ttu-id="42a7e-125">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="42a7e-125">**SampleGrad**</span></span>](texture1d-samplegrad.md)                              | <span data-ttu-id="42a7e-126">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="42a7e-126">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="42a7e-127">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="42a7e-127">**SampleLevel**</span></span>](texture1d-samplelevel.md)                            | <span data-ttu-id="42a7e-128">Muestrea una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="42a7e-128">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42a7e-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="42a7e-129">Minimum Shader Model</span></span>

<span data-ttu-id="42a7e-130">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="42a7e-130">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="42a7e-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="42a7e-131">Shader Model</span></span>                                                                | <span data-ttu-id="42a7e-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="42a7e-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42a7e-133">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="42a7e-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="42a7e-134">sí</span><span class="sxs-lookup"><span data-stu-id="42a7e-134">yes</span></span>       |



 

<span data-ttu-id="42a7e-135">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="42a7e-135">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="42a7e-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="42a7e-136">Vertex</span></span> | <span data-ttu-id="42a7e-137">Casco</span><span class="sxs-lookup"><span data-stu-id="42a7e-137">Hull</span></span> | <span data-ttu-id="42a7e-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="42a7e-138">Domain</span></span> | <span data-ttu-id="42a7e-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="42a7e-139">Geometry</span></span> | <span data-ttu-id="42a7e-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="42a7e-140">Pixel</span></span> | <span data-ttu-id="42a7e-141">Compute</span><span class="sxs-lookup"><span data-stu-id="42a7e-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42a7e-142">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-142">x</span></span>      | <span data-ttu-id="42a7e-143">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-143">x</span></span>    | <span data-ttu-id="42a7e-144">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-144">x</span></span>      | <span data-ttu-id="42a7e-145">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-145">x</span></span>        | <span data-ttu-id="42a7e-146">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-146">x</span></span>     | <span data-ttu-id="42a7e-147">x</span><span class="sxs-lookup"><span data-stu-id="42a7e-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="42a7e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="42a7e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a7e-149">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42a7e-149">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




