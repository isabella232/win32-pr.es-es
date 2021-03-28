---
title: tex1Dlod
description: Muestrea una textura 1D con mapas MIP. El LOD de mipmap se especifica en t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- HLSL de tex1Dlod
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793018"
---
# <a name="tex1dlod"></a><span data-ttu-id="b5a85-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="b5a85-105">tex1Dlod</span></span>

<span data-ttu-id="b5a85-106">Muestrea una textura 1D con mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="b5a85-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="b5a85-107">El LOD de mipmap se especifica en t.w.</span><span class="sxs-lookup"><span data-stu-id="b5a85-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="b5a85-108">RET tex1Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="b5a85-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="b5a85-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5a85-109">Parameters</span></span>



| <span data-ttu-id="b5a85-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b5a85-110">Item</span></span>                                                   | <span data-ttu-id="b5a85-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5a85-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b5a85-112"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="b5a85-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="b5a85-113">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="b5a85-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="b5a85-114"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="b5a85-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="b5a85-115">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="b5a85-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b5a85-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5a85-116">Return Value</span></span>

<span data-ttu-id="b5a85-117">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="b5a85-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b5a85-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="b5a85-118">Type Description</span></span>



| <span data-ttu-id="b5a85-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5a85-119">Name</span></span> | <span data-ttu-id="b5a85-120">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="b5a85-120">In/Out</span></span> | [<span data-ttu-id="b5a85-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="b5a85-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b5a85-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b5a85-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b5a85-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b5a85-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b5a85-124">s</span><span class="sxs-lookup"><span data-stu-id="b5a85-124">s</span></span>    | <span data-ttu-id="b5a85-125">in</span><span class="sxs-lookup"><span data-stu-id="b5a85-125">in</span></span>     | [<span data-ttu-id="b5a85-126">**object**</span><span class="sxs-lookup"><span data-stu-id="b5a85-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b5a85-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="b5a85-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="b5a85-128">1</span><span class="sxs-lookup"><span data-stu-id="b5a85-128">1</span></span>    |
| <span data-ttu-id="b5a85-129">t</span><span class="sxs-lookup"><span data-stu-id="b5a85-129">t</span></span>    | <span data-ttu-id="b5a85-130">in</span><span class="sxs-lookup"><span data-stu-id="b5a85-130">in</span></span>     | [<span data-ttu-id="b5a85-131">**medios**</span><span class="sxs-lookup"><span data-stu-id="b5a85-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b5a85-132">**float**</span><span class="sxs-lookup"><span data-stu-id="b5a85-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b5a85-133">4</span><span class="sxs-lookup"><span data-stu-id="b5a85-133">4</span></span>    |
| <span data-ttu-id="b5a85-134">direcc</span><span class="sxs-lookup"><span data-stu-id="b5a85-134">ret</span></span>  | <span data-ttu-id="b5a85-135">out</span><span class="sxs-lookup"><span data-stu-id="b5a85-135">out</span></span>    | [<span data-ttu-id="b5a85-136">**medios**</span><span class="sxs-lookup"><span data-stu-id="b5a85-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b5a85-137">**float**</span><span class="sxs-lookup"><span data-stu-id="b5a85-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b5a85-138">4</span><span class="sxs-lookup"><span data-stu-id="b5a85-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b5a85-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b5a85-139">Minimum Shader Model</span></span>

<span data-ttu-id="b5a85-140">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b5a85-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b5a85-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b5a85-141">Shader Model</span></span>                                              | <span data-ttu-id="b5a85-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="b5a85-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="b5a85-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b5a85-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b5a85-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="b5a85-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b5a85-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5a85-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b5a85-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="b5a85-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b5a85-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5a85-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b5a85-148">no</span><span class="sxs-lookup"><span data-stu-id="b5a85-148">no</span></span>                      |
| [<span data-ttu-id="b5a85-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b5a85-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b5a85-150">No</span><span class="sxs-lookup"><span data-stu-id="b5a85-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="b5a85-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5a85-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a85-152">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b5a85-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

