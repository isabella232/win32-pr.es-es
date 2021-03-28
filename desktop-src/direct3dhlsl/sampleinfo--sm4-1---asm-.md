---
title: sampleinfo (SM 4.1-ASM)
description: Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904307"
---
# <a name="sampleinfo-sm41---asm"></a><span data-ttu-id="e83fe-103">sampleinfo (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="e83fe-103">sampleinfo (sm4.1 - asm)</span></span>

<span data-ttu-id="e83fe-104">Consulta el número de muestras en una vista de recursos de sombreador determinada o en el rasterizador.</span><span class="sxs-lookup"><span data-stu-id="e83fe-104">Queries the number of samples in a given shader resource view or in the rasterizer.</span></span>



| <span data-ttu-id="e83fe-105">\[\_uint \] dest \[ . Mask \] , srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e83fe-105">\[\_uint\] dest\[.mask\], srcResource\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="e83fe-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e83fe-106">Item</span></span>                                                                                                               | <span data-ttu-id="e83fe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e83fe-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e83fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e83fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="e83fe-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="e83fe-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="e83fe-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="e83fe-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="e83fe-111">\[en \] el recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e83fe-111">\[in\] The shader resource.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="e83fe-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e83fe-112">Remarks</span></span>

<span data-ttu-id="e83fe-113">Esta instrucción devuelve el número de muestras para el recurso o el rasterizador especificados.</span><span class="sxs-lookup"><span data-stu-id="e83fe-113">This instruction returns the number of samples for the given resource or the rasterizer.</span></span> <span data-ttu-id="e83fe-114">Solo es válido para los recursos que se pueden cargar mediante [**ld2dms**](ld2dms--sm4-1---asm-.md) a menos que el rasterizador se especifique como *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="e83fe-114">It is valid only for resources that can be loaded using [**ld2dms**](ld2dms--sm4-1---asm-.md) unless the rasterizer is specified as *srcResource*.</span></span> <span data-ttu-id="e83fe-115">*srcResource* podría ser un registro de t \# (una vista de recursos del sombreador) o un registro de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="e83fe-115">*srcResource* could be a t\# register (a shader resource view) or a rasterizer register.</span></span>

<span data-ttu-id="e83fe-116">La instrucción calcula el vector (SampleCount, 0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e83fe-116">The instruction computes the vector (SampleCount,0,0,0).</span></span>

<span data-ttu-id="e83fe-117">Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.</span><span class="sxs-lookup"><span data-stu-id="e83fe-117">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span> <span data-ttu-id="e83fe-118">El valor devuelto es el punto flotante, a menos que \_ se use el modificador uint, en cuyo caso el valor devuelto es Integer.</span><span class="sxs-lookup"><span data-stu-id="e83fe-118">The returned value is floating point, unless the \_uint modifier is used, in which case the returned value is integer.</span></span> <span data-ttu-id="e83fe-119">Si no hay ningún recurso enlazado a la ranura especificada, se devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="e83fe-119">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="e83fe-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e83fe-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e83fe-121">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="e83fe-121">Vertex Shader</span></span> | <span data-ttu-id="e83fe-122">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="e83fe-122">Geometry Shader</span></span> | <span data-ttu-id="e83fe-123">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e83fe-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e83fe-124">X</span><span class="sxs-lookup"><span data-stu-id="e83fe-124">X</span></span>             | <span data-ttu-id="e83fe-125">X</span><span class="sxs-lookup"><span data-stu-id="e83fe-125">X</span></span>               | <span data-ttu-id="e83fe-126">x</span><span class="sxs-lookup"><span data-stu-id="e83fe-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e83fe-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e83fe-127">Minimum Shader Model</span></span>

<span data-ttu-id="e83fe-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e83fe-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e83fe-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e83fe-129">Shader Model</span></span>                                              | <span data-ttu-id="e83fe-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="e83fe-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e83fe-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e83fe-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e83fe-132">sí</span><span class="sxs-lookup"><span data-stu-id="e83fe-132">yes</span></span>       |
| [<span data-ttu-id="e83fe-133">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e83fe-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e83fe-134">sí</span><span class="sxs-lookup"><span data-stu-id="e83fe-134">yes</span></span>       |
| [<span data-ttu-id="e83fe-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e83fe-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e83fe-136">no</span><span class="sxs-lookup"><span data-stu-id="e83fe-136">no</span></span>        |
| [<span data-ttu-id="e83fe-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e83fe-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e83fe-138">no</span><span class="sxs-lookup"><span data-stu-id="e83fe-138">no</span></span>        |
| [<span data-ttu-id="e83fe-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e83fe-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e83fe-140">no</span><span class="sxs-lookup"><span data-stu-id="e83fe-140">no</span></span>        |
| [<span data-ttu-id="e83fe-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e83fe-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e83fe-142">no</span><span class="sxs-lookup"><span data-stu-id="e83fe-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e83fe-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e83fe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83fe-144">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e83fe-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





