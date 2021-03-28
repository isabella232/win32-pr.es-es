---
title: tex1Dbias
description: Muestrea una textura 1D después de sesgar el nivel de MIP por t.w.
ms.assetid: 2619ae23-e4b2-4699-b2ac-5ee711f9569a
keywords:
- HLSL de tex1Dbias
topic_type:
- apiref
api_name:
- tex1Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0328b9328a1406177fa26bd566c0fbf7d384db63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149363"
---
# <a name="tex1dbias"></a><span data-ttu-id="4a9d9-104">tex1Dbias</span><span class="sxs-lookup"><span data-stu-id="4a9d9-104">tex1Dbias</span></span>

<span data-ttu-id="4a9d9-105">Muestrea una textura 1D después de sesgar el nivel de MIP por t.w.</span><span class="sxs-lookup"><span data-stu-id="4a9d9-105">Samples a 1D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="4a9d9-106">RET tex1Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-106">ret tex1Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="4a9d9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a9d9-107">Parameters</span></span>



| <span data-ttu-id="4a9d9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a9d9-108">Item</span></span>                                                   | <span data-ttu-id="4a9d9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a9d9-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="4a9d9-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="4a9d9-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="4a9d9-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="4a9d9-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="4a9d9-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="4a9d9-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="4a9d9-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="4a9d9-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4a9d9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a9d9-114">Return Value</span></span>

<span data-ttu-id="4a9d9-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="4a9d9-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="4a9d9-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="4a9d9-116">Type Description</span></span>



| <span data-ttu-id="4a9d9-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a9d9-117">Name</span></span> | <span data-ttu-id="4a9d9-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="4a9d9-118">In/Out</span></span> | [<span data-ttu-id="4a9d9-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="4a9d9-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4a9d9-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4a9d9-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="4a9d9-122">s</span><span class="sxs-lookup"><span data-stu-id="4a9d9-122">s</span></span>    | <span data-ttu-id="4a9d9-123">in</span><span class="sxs-lookup"><span data-stu-id="4a9d9-123">in</span></span>     | [<span data-ttu-id="4a9d9-124">**object**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a9d9-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="4a9d9-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="4a9d9-126">1</span><span class="sxs-lookup"><span data-stu-id="4a9d9-126">1</span></span>    |
| <span data-ttu-id="4a9d9-127">t</span><span class="sxs-lookup"><span data-stu-id="4a9d9-127">t</span></span>    | <span data-ttu-id="4a9d9-128">in</span><span class="sxs-lookup"><span data-stu-id="4a9d9-128">in</span></span>     | [<span data-ttu-id="4a9d9-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a9d9-130">**float**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a9d9-131">4</span><span class="sxs-lookup"><span data-stu-id="4a9d9-131">4</span></span>    |
| <span data-ttu-id="4a9d9-132">direcc</span><span class="sxs-lookup"><span data-stu-id="4a9d9-132">ret</span></span>  | <span data-ttu-id="4a9d9-133">out</span><span class="sxs-lookup"><span data-stu-id="4a9d9-133">out</span></span>    | [<span data-ttu-id="4a9d9-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="4a9d9-135">**float**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4a9d9-136">4</span><span class="sxs-lookup"><span data-stu-id="4a9d9-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a9d9-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4a9d9-137">Minimum Shader Model</span></span>

<span data-ttu-id="4a9d9-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4a9d9-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4a9d9-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4a9d9-139">Shader Model</span></span>                                              | <span data-ttu-id="4a9d9-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="4a9d9-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="4a9d9-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4a9d9-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4a9d9-142">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="4a9d9-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4a9d9-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="4a9d9-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4a9d9-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="4a9d9-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a9d9-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4a9d9-148">No</span><span class="sxs-lookup"><span data-stu-id="4a9d9-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="4a9d9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a9d9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9d9-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4a9d9-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

