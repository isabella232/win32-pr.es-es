---
title: tex3Dlod
description: Muestrea una textura 3D con mapas MIP. El LOD de mipmap se especifica en t.w.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- HLSL de tex3Dlod
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983994"
---
# <a name="tex3dlod"></a><span data-ttu-id="86f4d-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="86f4d-105">tex3Dlod</span></span>

<span data-ttu-id="86f4d-106">Muestrea una textura 3D con mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="86f4d-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="86f4d-107">El LOD de mipmap se especifica en t.w.</span><span class="sxs-lookup"><span data-stu-id="86f4d-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="86f4d-108">RET tex3Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="86f4d-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="86f4d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86f4d-109">Parameters</span></span>



| <span data-ttu-id="86f4d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="86f4d-110">Item</span></span>                                                   | <span data-ttu-id="86f4d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="86f4d-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="86f4d-112"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="86f4d-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="86f4d-113">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="86f4d-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="86f4d-114"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="86f4d-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="86f4d-115">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="86f4d-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="86f4d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86f4d-116">Return Value</span></span>

<span data-ttu-id="86f4d-117">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="86f4d-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="86f4d-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="86f4d-118">Type Description</span></span>



| <span data-ttu-id="86f4d-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="86f4d-119">Name</span></span> | <span data-ttu-id="86f4d-120">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="86f4d-120">In/Out</span></span> | [<span data-ttu-id="86f4d-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="86f4d-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="86f4d-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="86f4d-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="86f4d-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="86f4d-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="86f4d-124">s</span><span class="sxs-lookup"><span data-stu-id="86f4d-124">s</span></span>    | <span data-ttu-id="86f4d-125">in</span><span class="sxs-lookup"><span data-stu-id="86f4d-125">in</span></span>     | [<span data-ttu-id="86f4d-126">**object**</span><span class="sxs-lookup"><span data-stu-id="86f4d-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="86f4d-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="86f4d-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="86f4d-128">1</span><span class="sxs-lookup"><span data-stu-id="86f4d-128">1</span></span>    |
| <span data-ttu-id="86f4d-129">t</span><span class="sxs-lookup"><span data-stu-id="86f4d-129">t</span></span>    | <span data-ttu-id="86f4d-130">in</span><span class="sxs-lookup"><span data-stu-id="86f4d-130">in</span></span>     | [<span data-ttu-id="86f4d-131">**medios**</span><span class="sxs-lookup"><span data-stu-id="86f4d-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="86f4d-132">**float**</span><span class="sxs-lookup"><span data-stu-id="86f4d-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="86f4d-133">4</span><span class="sxs-lookup"><span data-stu-id="86f4d-133">4</span></span>    |
| <span data-ttu-id="86f4d-134">direcc</span><span class="sxs-lookup"><span data-stu-id="86f4d-134">ret</span></span>  | <span data-ttu-id="86f4d-135">out</span><span class="sxs-lookup"><span data-stu-id="86f4d-135">out</span></span>    | [<span data-ttu-id="86f4d-136">**medios**</span><span class="sxs-lookup"><span data-stu-id="86f4d-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="86f4d-137">**float**</span><span class="sxs-lookup"><span data-stu-id="86f4d-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="86f4d-138">4</span><span class="sxs-lookup"><span data-stu-id="86f4d-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="86f4d-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="86f4d-139">Minimum Shader Model</span></span>

<span data-ttu-id="86f4d-140">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="86f4d-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="86f4d-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="86f4d-141">Shader Model</span></span>                                              | <span data-ttu-id="86f4d-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="86f4d-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="86f4d-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="86f4d-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="86f4d-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="86f4d-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="86f4d-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86f4d-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="86f4d-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="86f4d-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="86f4d-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86f4d-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="86f4d-148">no</span><span class="sxs-lookup"><span data-stu-id="86f4d-148">no</span></span>                      |
| [<span data-ttu-id="86f4d-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="86f4d-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="86f4d-150">No</span><span class="sxs-lookup"><span data-stu-id="86f4d-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="86f4d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f4d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f4d-152">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="86f4d-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

