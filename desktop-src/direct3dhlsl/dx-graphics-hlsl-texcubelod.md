---
title: texCUBElod
description: Muestrea una textura de cubo con mapas MIP. El LOD de mipmap se especifica en t.w.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- HLSL de texCUBElod
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984079"
---
# <a name="texcubelod"></a><span data-ttu-id="6b978-105">texCUBElod</span><span class="sxs-lookup"><span data-stu-id="6b978-105">texCUBElod</span></span>

<span data-ttu-id="6b978-106">Muestrea una textura de cubo con mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="6b978-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="6b978-107">El LOD de mipmap se especifica en t.w.</span><span class="sxs-lookup"><span data-stu-id="6b978-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="6b978-108">RET texCUBElod (s, t)</span><span class="sxs-lookup"><span data-stu-id="6b978-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="6b978-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b978-109">Parameters</span></span>



| <span data-ttu-id="6b978-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="6b978-110">Item</span></span>                                                   | <span data-ttu-id="6b978-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b978-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6b978-112"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="6b978-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="6b978-113">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="6b978-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="6b978-114"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="6b978-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="6b978-115">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="6b978-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6b978-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b978-116">Return Value</span></span>

<span data-ttu-id="6b978-117">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="6b978-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="6b978-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="6b978-118">Type Description</span></span>



| <span data-ttu-id="6b978-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b978-119">Name</span></span> | <span data-ttu-id="6b978-120">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="6b978-120">In/Out</span></span> | [<span data-ttu-id="6b978-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="6b978-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6b978-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="6b978-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6b978-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6b978-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="6b978-124">s</span><span class="sxs-lookup"><span data-stu-id="6b978-124">s</span></span>    | <span data-ttu-id="6b978-125">in</span><span class="sxs-lookup"><span data-stu-id="6b978-125">in</span></span>     | [<span data-ttu-id="6b978-126">**object**</span><span class="sxs-lookup"><span data-stu-id="6b978-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b978-127">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="6b978-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="6b978-128">1</span><span class="sxs-lookup"><span data-stu-id="6b978-128">1</span></span>    |
| <span data-ttu-id="6b978-129">t</span><span class="sxs-lookup"><span data-stu-id="6b978-129">t</span></span>    | <span data-ttu-id="6b978-130">in</span><span class="sxs-lookup"><span data-stu-id="6b978-130">in</span></span>     | [<span data-ttu-id="6b978-131">**medios**</span><span class="sxs-lookup"><span data-stu-id="6b978-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b978-132">**float**</span><span class="sxs-lookup"><span data-stu-id="6b978-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6b978-133">4</span><span class="sxs-lookup"><span data-stu-id="6b978-133">4</span></span>    |
| <span data-ttu-id="6b978-134">direcc</span><span class="sxs-lookup"><span data-stu-id="6b978-134">ret</span></span>  | <span data-ttu-id="6b978-135">out</span><span class="sxs-lookup"><span data-stu-id="6b978-135">out</span></span>    | [<span data-ttu-id="6b978-136">**medios**</span><span class="sxs-lookup"><span data-stu-id="6b978-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6b978-137">**float**</span><span class="sxs-lookup"><span data-stu-id="6b978-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6b978-138">4</span><span class="sxs-lookup"><span data-stu-id="6b978-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6b978-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6b978-139">Minimum Shader Model</span></span>

<span data-ttu-id="6b978-140">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6b978-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6b978-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6b978-141">Shader Model</span></span>                                              | <span data-ttu-id="6b978-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="6b978-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="6b978-143">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6b978-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6b978-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="6b978-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6b978-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b978-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6b978-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="6b978-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6b978-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b978-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6b978-148">no</span><span class="sxs-lookup"><span data-stu-id="6b978-148">no</span></span>                      |
| [<span data-ttu-id="6b978-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b978-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6b978-150">No</span><span class="sxs-lookup"><span data-stu-id="6b978-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="6b978-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b978-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b978-152">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6b978-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

