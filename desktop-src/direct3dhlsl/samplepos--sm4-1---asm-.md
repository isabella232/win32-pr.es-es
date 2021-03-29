---
title: samplepos (SM 4.1-ASM)
description: Consulta la posición de una muestra en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419976"
---
# <a name="samplepos-sm41---asm"></a><span data-ttu-id="e9de5-103">samplepos (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="e9de5-103">samplepos (sm4.1 - asm)</span></span>

<span data-ttu-id="e9de5-104">Consulta la posición de una muestra en una vista de recursos de sombreador determinada o en el rasterizador.</span><span class="sxs-lookup"><span data-stu-id="e9de5-104">Queries the position of a sample in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="e9de5-105">samplepos dest \[ . Mask \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar)</span><span class="sxs-lookup"><span data-stu-id="e9de5-105">samplepos dest\[.mask\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="e9de5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9de5-106">Item</span></span>                                                                                                               | <span data-ttu-id="e9de5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9de5-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e9de5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e9de5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="e9de5-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="e9de5-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="e9de5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="e9de5-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="e9de5-111">\[en \] el recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9de5-111">\[in\] The shader resource.</span></span><br/>                         |
| <span data-ttu-id="e9de5-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="e9de5-112"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="e9de5-113">\[en \] el índice del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e9de5-113">\[in\] The index of the sample.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e9de5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9de5-114">Remarks</span></span>

<span data-ttu-id="e9de5-115">Esta instrucción devuelve la posición de ejemplo en 2D del *sampleIndex* de ejemplo para el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="e9de5-115">This instruction returns the 2D sample position of sample *sampleIndex* for the given resource.</span></span> <span data-ttu-id="e9de5-116">Solo es válido para los recursos que se pueden cargar mediante [**ld2dms**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique como *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="e9de5-116">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span>

<span data-ttu-id="e9de5-117">*srcResource* puede ser un registro de t \# (una vista de recursos del sombreador) o un registro de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="e9de5-117">*srcResource* can be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="e9de5-118">La instrucción calcula el vector de punto flotante (XPosition, YPosition, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e9de5-118">The instruction computes the floating point vector (Xposition, Yposition, 0, 0).</span></span>

<span data-ttu-id="e9de5-119">Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.</span><span class="sxs-lookup"><span data-stu-id="e9de5-119">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="e9de5-120">La posición del ejemplo es relativa al centro del píxel, basado en el sistema de coordenadas de píxeles.</span><span class="sxs-lookup"><span data-stu-id="e9de5-120">The sample position is relative to the pixel's center, based on the Pixel Coordinate System.</span></span>

<span data-ttu-id="e9de5-121">Si *sampleIndex* está fuera de los límites, se devuelve un vector de cero.</span><span class="sxs-lookup"><span data-stu-id="e9de5-121">If *sampleIndex* is out of bounds a zero vector is returned.</span></span> <span data-ttu-id="e9de5-122">Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="e9de5-122">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="e9de5-123">**samplepos** se puede usar para cosas como las resoluciones personalizadas en el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9de5-123">**samplepos** can be used for things like custom resolves in shader code.</span></span>

<span data-ttu-id="e9de5-124">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e9de5-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e9de5-125">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="e9de5-125">Vertex Shader</span></span> | <span data-ttu-id="e9de5-126">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="e9de5-126">Geometry Shader</span></span> | <span data-ttu-id="e9de5-127">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e9de5-127">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="e9de5-128">x</span><span class="sxs-lookup"><span data-stu-id="e9de5-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e9de5-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e9de5-129">Minimum Shader Model</span></span>

<span data-ttu-id="e9de5-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9de5-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e9de5-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e9de5-131">Shader Model</span></span>                                              | <span data-ttu-id="e9de5-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="e9de5-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e9de5-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e9de5-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e9de5-134">sí</span><span class="sxs-lookup"><span data-stu-id="e9de5-134">yes</span></span>       |
| [<span data-ttu-id="e9de5-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e9de5-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e9de5-136">sí</span><span class="sxs-lookup"><span data-stu-id="e9de5-136">yes</span></span>       |
| [<span data-ttu-id="e9de5-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e9de5-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e9de5-138">no</span><span class="sxs-lookup"><span data-stu-id="e9de5-138">no</span></span>        |
| [<span data-ttu-id="e9de5-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e9de5-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e9de5-140">no</span><span class="sxs-lookup"><span data-stu-id="e9de5-140">no</span></span>        |
| [<span data-ttu-id="e9de5-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e9de5-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e9de5-142">no</span><span class="sxs-lookup"><span data-stu-id="e9de5-142">no</span></span>        |
| [<span data-ttu-id="e9de5-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e9de5-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e9de5-144">no</span><span class="sxs-lookup"><span data-stu-id="e9de5-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e9de5-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9de5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9de5-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e9de5-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





