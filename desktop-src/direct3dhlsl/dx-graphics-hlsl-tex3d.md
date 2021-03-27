---
title: tex3D (referencia de HLSL)
description: Muestrea una textura 3D.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- HLSL de tex3D
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793288"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="d61ab-104">tex3D (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="d61ab-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="d61ab-105">Muestrea una textura 3D.</span><span class="sxs-lookup"><span data-stu-id="d61ab-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="d61ab-106">RET tex3D (s, t)</span><span class="sxs-lookup"><span data-stu-id="d61ab-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="d61ab-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d61ab-107">Parameters</span></span>



| <span data-ttu-id="d61ab-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d61ab-108">Item</span></span>                                                   | <span data-ttu-id="d61ab-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d61ab-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d61ab-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="d61ab-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="d61ab-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="d61ab-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="d61ab-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="d61ab-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="d61ab-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="d61ab-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d61ab-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d61ab-114">Return Value</span></span>

<span data-ttu-id="d61ab-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="d61ab-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d61ab-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="d61ab-116">Type Description</span></span>



| <span data-ttu-id="d61ab-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="d61ab-117">Name</span></span> | <span data-ttu-id="d61ab-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="d61ab-118">In/Out</span></span> | [<span data-ttu-id="d61ab-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="d61ab-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d61ab-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="d61ab-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d61ab-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="d61ab-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d61ab-122">s</span><span class="sxs-lookup"><span data-stu-id="d61ab-122">s</span></span>    | <span data-ttu-id="d61ab-123">in</span><span class="sxs-lookup"><span data-stu-id="d61ab-123">in</span></span>     | [<span data-ttu-id="d61ab-124">**object**</span><span class="sxs-lookup"><span data-stu-id="d61ab-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d61ab-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="d61ab-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="d61ab-126">1</span><span class="sxs-lookup"><span data-stu-id="d61ab-126">1</span></span>    |
| <span data-ttu-id="d61ab-127">t</span><span class="sxs-lookup"><span data-stu-id="d61ab-127">t</span></span>    | <span data-ttu-id="d61ab-128">in</span><span class="sxs-lookup"><span data-stu-id="d61ab-128">in</span></span>     | [<span data-ttu-id="d61ab-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="d61ab-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d61ab-130">**flot**</span><span class="sxs-lookup"><span data-stu-id="d61ab-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d61ab-131">3</span><span class="sxs-lookup"><span data-stu-id="d61ab-131">3</span></span>    |
| <span data-ttu-id="d61ab-132">direcc</span><span class="sxs-lookup"><span data-stu-id="d61ab-132">ret</span></span>  | <span data-ttu-id="d61ab-133">out</span><span class="sxs-lookup"><span data-stu-id="d61ab-133">out</span></span>    | [<span data-ttu-id="d61ab-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="d61ab-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d61ab-135">**float**</span><span class="sxs-lookup"><span data-stu-id="d61ab-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d61ab-136">4</span><span class="sxs-lookup"><span data-stu-id="d61ab-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d61ab-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d61ab-137">Minimum Shader Model</span></span>

<span data-ttu-id="d61ab-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d61ab-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d61ab-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d61ab-139">Shader Model</span></span>                                              | <span data-ttu-id="d61ab-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="d61ab-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d61ab-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d61ab-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d61ab-142">sí (solo sombreador de píxeles), pero debe utilizar la [opción de compilación heredada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) al compilar.</span><span class="sxs-lookup"><span data-stu-id="d61ab-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="d61ab-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d61ab-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d61ab-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="d61ab-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="d61ab-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d61ab-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d61ab-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="d61ab-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="d61ab-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d61ab-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d61ab-148">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="d61ab-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="d61ab-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d61ab-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d61ab-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d61ab-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

