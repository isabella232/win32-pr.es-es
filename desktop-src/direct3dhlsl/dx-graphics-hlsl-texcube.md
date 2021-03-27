---
title: texCUBE (referencia de HLSL)
description: Muestrea una textura del cubo.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
keywords:
- HLSL de texCUBE
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077884"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="ef79c-104">texCUBE (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="ef79c-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="ef79c-105">Muestrea una textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="ef79c-105">Samples a cube texture.</span></span>



| <span data-ttu-id="ef79c-106">RET texCUBE (s, t)</span><span class="sxs-lookup"><span data-stu-id="ef79c-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="ef79c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef79c-107">Parameters</span></span>



| <span data-ttu-id="ef79c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ef79c-108">Item</span></span>                                                   | <span data-ttu-id="ef79c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef79c-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ef79c-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="ef79c-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ef79c-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="ef79c-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="ef79c-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="ef79c-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="ef79c-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="ef79c-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ef79c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef79c-114">Return Value</span></span>

<span data-ttu-id="ef79c-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="ef79c-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="ef79c-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="ef79c-116">Type Description</span></span>



| <span data-ttu-id="ef79c-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef79c-117">Name</span></span> | <span data-ttu-id="ef79c-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="ef79c-118">In/Out</span></span> | [<span data-ttu-id="ef79c-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="ef79c-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ef79c-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ef79c-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ef79c-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ef79c-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ef79c-122">s</span><span class="sxs-lookup"><span data-stu-id="ef79c-122">s</span></span>    | <span data-ttu-id="ef79c-123">in</span><span class="sxs-lookup"><span data-stu-id="ef79c-123">in</span></span>     | [<span data-ttu-id="ef79c-124">**object**</span><span class="sxs-lookup"><span data-stu-id="ef79c-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ef79c-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="ef79c-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="ef79c-126">1</span><span class="sxs-lookup"><span data-stu-id="ef79c-126">1</span></span>    |
| <span data-ttu-id="ef79c-127">t</span><span class="sxs-lookup"><span data-stu-id="ef79c-127">t</span></span>    | <span data-ttu-id="ef79c-128">in</span><span class="sxs-lookup"><span data-stu-id="ef79c-128">in</span></span>     | [<span data-ttu-id="ef79c-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="ef79c-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ef79c-130">**flot**</span><span class="sxs-lookup"><span data-stu-id="ef79c-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ef79c-131">3</span><span class="sxs-lookup"><span data-stu-id="ef79c-131">3</span></span>    |
| <span data-ttu-id="ef79c-132">direcc</span><span class="sxs-lookup"><span data-stu-id="ef79c-132">ret</span></span>  | <span data-ttu-id="ef79c-133">out</span><span class="sxs-lookup"><span data-stu-id="ef79c-133">out</span></span>    | [<span data-ttu-id="ef79c-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="ef79c-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ef79c-135">**float**</span><span class="sxs-lookup"><span data-stu-id="ef79c-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ef79c-136">4</span><span class="sxs-lookup"><span data-stu-id="ef79c-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ef79c-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ef79c-137">Minimum Shader Model</span></span>

<span data-ttu-id="ef79c-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ef79c-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ef79c-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ef79c-139">Shader Model</span></span>                                              | <span data-ttu-id="ef79c-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="ef79c-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="ef79c-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ef79c-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ef79c-142">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="ef79c-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ef79c-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ef79c-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ef79c-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="ef79c-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ef79c-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ef79c-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ef79c-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="ef79c-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="ef79c-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ef79c-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ef79c-148">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="ef79c-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ef79c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef79c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef79c-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ef79c-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

