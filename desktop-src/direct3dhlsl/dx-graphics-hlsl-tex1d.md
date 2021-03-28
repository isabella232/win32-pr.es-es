---
title: tex1D (referencia de HLSL)
description: Muestrea una textura 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- HLSL de tex1D
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792303"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="82b64-104">tex1D (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="82b64-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="82b64-105">Muestrea una textura 1D.</span><span class="sxs-lookup"><span data-stu-id="82b64-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="82b64-106">RET tex1D (s, t)</span><span class="sxs-lookup"><span data-stu-id="82b64-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="82b64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82b64-107">Parameters</span></span>



| <span data-ttu-id="82b64-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="82b64-108">Item</span></span>                                                   | <span data-ttu-id="82b64-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="82b64-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="82b64-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="82b64-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="82b64-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="82b64-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="82b64-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="82b64-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="82b64-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="82b64-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="82b64-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82b64-114">Return Value</span></span>

<span data-ttu-id="82b64-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="82b64-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="82b64-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="82b64-116">Type Description</span></span>



| <span data-ttu-id="82b64-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="82b64-117">Name</span></span> | <span data-ttu-id="82b64-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="82b64-118">In/Out</span></span> | [<span data-ttu-id="82b64-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="82b64-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="82b64-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="82b64-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="82b64-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="82b64-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="82b64-122">s</span><span class="sxs-lookup"><span data-stu-id="82b64-122">s</span></span>    | <span data-ttu-id="82b64-123">in</span><span class="sxs-lookup"><span data-stu-id="82b64-123">in</span></span>     | [<span data-ttu-id="82b64-124">**object**</span><span class="sxs-lookup"><span data-stu-id="82b64-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="82b64-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="82b64-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="82b64-126">1</span><span class="sxs-lookup"><span data-stu-id="82b64-126">1</span></span>    |
| <span data-ttu-id="82b64-127">t</span><span class="sxs-lookup"><span data-stu-id="82b64-127">t</span></span>    | <span data-ttu-id="82b64-128">in</span><span class="sxs-lookup"><span data-stu-id="82b64-128">in</span></span>     | [<span data-ttu-id="82b64-129">**escalar**</span><span class="sxs-lookup"><span data-stu-id="82b64-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="82b64-130">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="82b64-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="82b64-131">1</span><span class="sxs-lookup"><span data-stu-id="82b64-131">1</span></span>    |
| <span data-ttu-id="82b64-132">direcc</span><span class="sxs-lookup"><span data-stu-id="82b64-132">ret</span></span>  | <span data-ttu-id="82b64-133">out</span><span class="sxs-lookup"><span data-stu-id="82b64-133">out</span></span>    | [<span data-ttu-id="82b64-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="82b64-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="82b64-135">**float**</span><span class="sxs-lookup"><span data-stu-id="82b64-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="82b64-136">4</span><span class="sxs-lookup"><span data-stu-id="82b64-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82b64-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="82b64-137">Minimum Shader Model</span></span>

<span data-ttu-id="82b64-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82b64-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="82b64-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="82b64-139">Shader Model</span></span>                                              | <span data-ttu-id="82b64-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="82b64-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82b64-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="82b64-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82b64-142">sí (solo sombreador de píxeles), pero debe utilizar la [opción de compilación heredada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) al compilar.</span><span class="sxs-lookup"><span data-stu-id="82b64-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="82b64-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82b64-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82b64-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="82b64-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="82b64-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82b64-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82b64-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="82b64-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="82b64-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82b64-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82b64-148">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="82b64-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="82b64-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="82b64-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b64-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="82b64-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

