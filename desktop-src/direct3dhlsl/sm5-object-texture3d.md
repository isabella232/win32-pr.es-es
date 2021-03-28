---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- HLSL de Texture3D
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076630"
---
# <a name="texture3d"></a><span data-ttu-id="11d54-104">Texture3D</span><span class="sxs-lookup"><span data-stu-id="11d54-104">Texture3D</span></span>

<span data-ttu-id="11d54-105">Tipo Texture3D ([tal como existe en el modelo de sombreador 4](dx-graphics-hlsl-to-type.md)) más las variables de recurso.</span><span class="sxs-lookup"><span data-stu-id="11d54-105">Texture3D type ([as it exists in Shader Model 4](dx-graphics-hlsl-to-type.md)) plus resource variables.</span></span> <span data-ttu-id="11d54-106">Este objeto de textura admite los siguientes métodos además de los métodos del modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="11d54-106">This texture object supports the following methods in addition to the methods in Shader Model 4.</span></span>



| <span data-ttu-id="11d54-107">Método</span><span class="sxs-lookup"><span data-stu-id="11d54-107">Method</span></span>                                                                  | <span data-ttu-id="11d54-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="11d54-108">Description</span></span>                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11d54-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="11d54-109">**GetDimensions**</span></span>](sm5-object-texture3d-getdimensions.md)             | <span data-ttu-id="11d54-110">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="11d54-110">Gets the resource dimensions.</span></span>                                                              |
| [<span data-ttu-id="11d54-111">**Carga**</span><span class="sxs-lookup"><span data-stu-id="11d54-111">**Load**</span></span>](texture3d-load.md)                                          | <span data-ttu-id="11d54-112">Lee los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="11d54-112">Reads texture data.</span></span>                                                                        |
| <span data-ttu-id="11d54-113">[**MIPS. Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="11d54-113">[**mips.Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md)</span></span> | <span data-ttu-id="11d54-114">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11d54-114">Gets a read-only resource variable.</span></span>                                                        |
| <span data-ttu-id="11d54-115">[**Operador\[\]**](sm5-object-texture3d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="11d54-115">[**Operator\[\]**](sm5-object-texture3d-operatorindex.md)</span></span>              | <span data-ttu-id="11d54-116">Obtiene una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11d54-116">Gets a read-only resource variable.</span></span>                                                        |
| [<span data-ttu-id="11d54-117">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="11d54-117">**Sample**</span></span>](texture3d-sample.md)                                      | <span data-ttu-id="11d54-118">Muestrea una textura.</span><span class="sxs-lookup"><span data-stu-id="11d54-118">Samples a texture.</span></span>                                                                         |
| [<span data-ttu-id="11d54-119">**SampleBias**</span><span class="sxs-lookup"><span data-stu-id="11d54-119">**SampleBias**</span></span>](texture3d-samplebias.md)                              | <span data-ttu-id="11d54-120">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="11d54-120">Samples a texture, after applying the bias value to the mipmap level.</span></span>                      |
| [<span data-ttu-id="11d54-121">**SampleGrad**</span><span class="sxs-lookup"><span data-stu-id="11d54-121">**SampleGrad**</span></span>](texture3d-samplegrad.md)                              | <span data-ttu-id="11d54-122">Muestrea una textura mediante un degradado para influir en la forma en que se calcula la ubicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="11d54-122">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span> |
| [<span data-ttu-id="11d54-123">**SampleLevel**</span><span class="sxs-lookup"><span data-stu-id="11d54-123">**SampleLevel**</span></span>](texture3d-samplelevel.md)                            | <span data-ttu-id="11d54-124">Muestrea una textura en el nivel de mipmap especificado.</span><span class="sxs-lookup"><span data-stu-id="11d54-124">Samples a texture on the specified mipmap level.</span></span>                                           |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="11d54-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="11d54-125">Minimum Shader Model</span></span>

<span data-ttu-id="11d54-126">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="11d54-126">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="11d54-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="11d54-127">Shader Model</span></span>                                                                | <span data-ttu-id="11d54-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="11d54-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="11d54-129">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="11d54-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="11d54-130">sí</span><span class="sxs-lookup"><span data-stu-id="11d54-130">yes</span></span>       |



 

<span data-ttu-id="11d54-131">Este objeto es compatible con los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="11d54-131">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="11d54-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="11d54-132">Vertex</span></span> | <span data-ttu-id="11d54-133">Casco</span><span class="sxs-lookup"><span data-stu-id="11d54-133">Hull</span></span> | <span data-ttu-id="11d54-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="11d54-134">Domain</span></span> | <span data-ttu-id="11d54-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="11d54-135">Geometry</span></span> | <span data-ttu-id="11d54-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="11d54-136">Pixel</span></span> | <span data-ttu-id="11d54-137">Compute</span><span class="sxs-lookup"><span data-stu-id="11d54-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="11d54-138">x</span><span class="sxs-lookup"><span data-stu-id="11d54-138">x</span></span>      | <span data-ttu-id="11d54-139">x</span><span class="sxs-lookup"><span data-stu-id="11d54-139">x</span></span>    | <span data-ttu-id="11d54-140">x</span><span class="sxs-lookup"><span data-stu-id="11d54-140">x</span></span>      | <span data-ttu-id="11d54-141">x</span><span class="sxs-lookup"><span data-stu-id="11d54-141">x</span></span>        | <span data-ttu-id="11d54-142">x</span><span class="sxs-lookup"><span data-stu-id="11d54-142">x</span></span>     | <span data-ttu-id="11d54-143">x</span><span class="sxs-lookup"><span data-stu-id="11d54-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="11d54-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="11d54-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d54-145">Objetos del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="11d54-145">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




