---
title: tex1Dproj
description: Muestrea una textura 1D mediante una división proyectada; la coordenada de textura se divide entre t. w antes de que tenga lugar la búsqueda.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- HLSL de tex1Dproj
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984051"
---
# <a name="tex1dproj"></a><span data-ttu-id="98f04-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="98f04-104">tex1Dproj</span></span>

<span data-ttu-id="98f04-105">Muestrea una textura 1D mediante una división proyectada; la coordenada de textura se divide entre t. w antes de que tenga lugar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="98f04-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="98f04-106">RET tex1Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="98f04-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="98f04-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98f04-107">Parameters</span></span>



| <span data-ttu-id="98f04-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="98f04-108">Item</span></span>                                                   | <span data-ttu-id="98f04-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="98f04-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="98f04-110"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="98f04-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="98f04-111">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="98f04-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="98f04-112"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="98f04-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="98f04-113">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="98f04-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="98f04-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98f04-114">Return Value</span></span>

<span data-ttu-id="98f04-115">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="98f04-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="98f04-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="98f04-116">Type Description</span></span>



| <span data-ttu-id="98f04-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="98f04-117">Name</span></span> | <span data-ttu-id="98f04-118">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="98f04-118">In/Out</span></span> | [<span data-ttu-id="98f04-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="98f04-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="98f04-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="98f04-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="98f04-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="98f04-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="98f04-122">s</span><span class="sxs-lookup"><span data-stu-id="98f04-122">s</span></span>    | <span data-ttu-id="98f04-123">in</span><span class="sxs-lookup"><span data-stu-id="98f04-123">in</span></span>     | [<span data-ttu-id="98f04-124">**object**</span><span class="sxs-lookup"><span data-stu-id="98f04-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="98f04-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="98f04-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="98f04-126">1</span><span class="sxs-lookup"><span data-stu-id="98f04-126">1</span></span>    |
| <span data-ttu-id="98f04-127">t</span><span class="sxs-lookup"><span data-stu-id="98f04-127">t</span></span>    | <span data-ttu-id="98f04-128">in</span><span class="sxs-lookup"><span data-stu-id="98f04-128">in</span></span>     | [<span data-ttu-id="98f04-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="98f04-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="98f04-130">**float**</span><span class="sxs-lookup"><span data-stu-id="98f04-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="98f04-131">4</span><span class="sxs-lookup"><span data-stu-id="98f04-131">4</span></span>    |
| <span data-ttu-id="98f04-132">direcc</span><span class="sxs-lookup"><span data-stu-id="98f04-132">ret</span></span>  | <span data-ttu-id="98f04-133">out</span><span class="sxs-lookup"><span data-stu-id="98f04-133">out</span></span>    | [<span data-ttu-id="98f04-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="98f04-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="98f04-135">**float**</span><span class="sxs-lookup"><span data-stu-id="98f04-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="98f04-136">4</span><span class="sxs-lookup"><span data-stu-id="98f04-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="98f04-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="98f04-137">Minimum Shader Model</span></span>

<span data-ttu-id="98f04-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98f04-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="98f04-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="98f04-139">Shader Model</span></span>                                              | <span data-ttu-id="98f04-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="98f04-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="98f04-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="98f04-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="98f04-142">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="98f04-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="98f04-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98f04-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="98f04-144">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="98f04-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="98f04-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98f04-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="98f04-146">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="98f04-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="98f04-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98f04-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="98f04-148">No</span><span class="sxs-lookup"><span data-stu-id="98f04-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="98f04-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="98f04-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f04-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="98f04-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

