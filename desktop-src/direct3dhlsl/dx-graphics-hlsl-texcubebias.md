---
title: texCUBEbias
description: Muestrea una textura del cubo después de sesgar el nivel de MIP por t.w.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- HLSL de texCUBEbias
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149315"
---
# <a name="texcubebias"></a><span data-ttu-id="3c0e7-104">texCUBEbias</span><span class="sxs-lookup"><span data-stu-id="3c0e7-104">texCUBEbias</span></span>

<span data-ttu-id="3c0e7-105">Muestrea una textura del cubo después de sesgar el nivel de MIP por t.w.</span><span class="sxs-lookup"><span data-stu-id="3c0e7-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="3c0e7-106">RET texCUBEbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="3c0e7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c0e7-107">Parameters</span></span>



| <span data-ttu-id="3c0e7-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c0e7-108">Item</span></span>                                                   | <span data-ttu-id="3c0e7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c0e7-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3c0e7-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="3c0e7-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="3c0e7-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="3c0e7-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="3c0e7-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="3c0e7-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="3c0e7-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="3c0e7-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3c0e7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c0e7-114">Return Value</span></span>

<span data-ttu-id="3c0e7-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="3c0e7-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="3c0e7-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="3c0e7-116">Type Description</span></span>



| <span data-ttu-id="3c0e7-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c0e7-117">Name</span></span> | <span data-ttu-id="3c0e7-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="3c0e7-118">In/Out</span></span> | [<span data-ttu-id="3c0e7-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3c0e7-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3c0e7-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3c0e7-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="3c0e7-122">s</span><span class="sxs-lookup"><span data-stu-id="3c0e7-122">s</span></span>    | <span data-ttu-id="3c0e7-123">in</span><span class="sxs-lookup"><span data-stu-id="3c0e7-123">in</span></span>     | [<span data-ttu-id="3c0e7-124">**object**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c0e7-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="3c0e7-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="3c0e7-126">1</span><span class="sxs-lookup"><span data-stu-id="3c0e7-126">1</span></span>    |
| <span data-ttu-id="3c0e7-127">t</span><span class="sxs-lookup"><span data-stu-id="3c0e7-127">t</span></span>    | <span data-ttu-id="3c0e7-128">in</span><span class="sxs-lookup"><span data-stu-id="3c0e7-128">in</span></span>     | [<span data-ttu-id="3c0e7-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c0e7-130">**float**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c0e7-131">4</span><span class="sxs-lookup"><span data-stu-id="3c0e7-131">4</span></span>    |
| <span data-ttu-id="3c0e7-132">direcc</span><span class="sxs-lookup"><span data-stu-id="3c0e7-132">ret</span></span>  | <span data-ttu-id="3c0e7-133">out</span><span class="sxs-lookup"><span data-stu-id="3c0e7-133">out</span></span>    | [<span data-ttu-id="3c0e7-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c0e7-135">**float**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c0e7-136">4</span><span class="sxs-lookup"><span data-stu-id="3c0e7-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3c0e7-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3c0e7-137">Minimum Shader Model</span></span>

<span data-ttu-id="3c0e7-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c0e7-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3c0e7-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3c0e7-139">Shader Model</span></span>                                              | <span data-ttu-id="3c0e7-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="3c0e7-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="3c0e7-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3c0e7-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3c0e7-142">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="3c0e7-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3c0e7-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="3c0e7-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3c0e7-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="3c0e7-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c0e7-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3c0e7-148">No</span><span class="sxs-lookup"><span data-stu-id="3c0e7-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="3c0e7-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c0e7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0e7-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3c0e7-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

