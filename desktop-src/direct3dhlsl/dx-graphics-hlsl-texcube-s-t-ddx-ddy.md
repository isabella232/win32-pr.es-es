---
title: 'texCUBE (referencia de HLSL): seleccionar el nivel de MIP'
description: Muestrea una textura de cubo usando un degradado para seleccionar el nivel de MIP. | texCUBE (referencia de HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
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
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987295"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="3c125-105">texCUBE (referencia de HLSL): seleccionar el nivel de MIP</span><span class="sxs-lookup"><span data-stu-id="3c125-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="3c125-106">Muestrea una textura de cubo usando un degradado para seleccionar el nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="3c125-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="3c125-107">RET texCUBE (s, t, DDX, DDY)</span><span class="sxs-lookup"><span data-stu-id="3c125-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3c125-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c125-108">Parameters</span></span>



| <span data-ttu-id="3c125-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="3c125-109">Item</span></span>                                                         | <span data-ttu-id="3c125-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c125-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3c125-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="3c125-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="3c125-112">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="3c125-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="3c125-113"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="3c125-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="3c125-114">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="3c125-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="3c125-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="3c125-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="3c125-116">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="3c125-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="3c125-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="3c125-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="3c125-118">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="3c125-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3c125-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c125-119">Return Value</span></span>

<span data-ttu-id="3c125-120">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="3c125-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="3c125-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="3c125-121">Type Description</span></span>



| <span data-ttu-id="3c125-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="3c125-122">Name</span></span> | <span data-ttu-id="3c125-123">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="3c125-123">In/Out</span></span> | [<span data-ttu-id="3c125-124">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="3c125-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3c125-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3c125-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3c125-126">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3c125-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="3c125-127">s</span><span class="sxs-lookup"><span data-stu-id="3c125-127">s</span></span>    | <span data-ttu-id="3c125-128">in</span><span class="sxs-lookup"><span data-stu-id="3c125-128">in</span></span>     | [<span data-ttu-id="3c125-129">**object**</span><span class="sxs-lookup"><span data-stu-id="3c125-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c125-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="3c125-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="3c125-131">1</span><span class="sxs-lookup"><span data-stu-id="3c125-131">1</span></span>    |
| <span data-ttu-id="3c125-132">t</span><span class="sxs-lookup"><span data-stu-id="3c125-132">t</span></span>    | <span data-ttu-id="3c125-133">in</span><span class="sxs-lookup"><span data-stu-id="3c125-133">in</span></span>     | [<span data-ttu-id="3c125-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c125-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c125-135">**flot**</span><span class="sxs-lookup"><span data-stu-id="3c125-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c125-136">3</span><span class="sxs-lookup"><span data-stu-id="3c125-136">3</span></span>    |
| <span data-ttu-id="3c125-137">DDX</span><span class="sxs-lookup"><span data-stu-id="3c125-137">ddx</span></span>  | <span data-ttu-id="3c125-138">in</span><span class="sxs-lookup"><span data-stu-id="3c125-138">in</span></span>     | [<span data-ttu-id="3c125-139">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c125-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c125-140">**flot**</span><span class="sxs-lookup"><span data-stu-id="3c125-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c125-141">3</span><span class="sxs-lookup"><span data-stu-id="3c125-141">3</span></span>    |
| <span data-ttu-id="3c125-142">ddy</span><span class="sxs-lookup"><span data-stu-id="3c125-142">ddy</span></span>  | <span data-ttu-id="3c125-143">in</span><span class="sxs-lookup"><span data-stu-id="3c125-143">in</span></span>     | [<span data-ttu-id="3c125-144">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c125-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c125-145">**flot**</span><span class="sxs-lookup"><span data-stu-id="3c125-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c125-146">3</span><span class="sxs-lookup"><span data-stu-id="3c125-146">3</span></span>    |
| <span data-ttu-id="3c125-147">direcc</span><span class="sxs-lookup"><span data-stu-id="3c125-147">ret</span></span>  | <span data-ttu-id="3c125-148">out</span><span class="sxs-lookup"><span data-stu-id="3c125-148">out</span></span>    | [<span data-ttu-id="3c125-149">**medios**</span><span class="sxs-lookup"><span data-stu-id="3c125-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3c125-150">**float**</span><span class="sxs-lookup"><span data-stu-id="3c125-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3c125-151">4</span><span class="sxs-lookup"><span data-stu-id="3c125-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3c125-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3c125-152">Minimum Shader Model</span></span>

<span data-ttu-id="3c125-153">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c125-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3c125-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3c125-154">Shader Model</span></span>                                              | <span data-ttu-id="3c125-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="3c125-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="3c125-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3c125-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3c125-157">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c125-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="3c125-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c125-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3c125-159">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c125-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="3c125-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c125-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3c125-161">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="3c125-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="3c125-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c125-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3c125-163">no</span><span class="sxs-lookup"><span data-stu-id="3c125-163">no</span></span>                       |



 

1.  <span data-ttu-id="3c125-164">Se realiza una reordenación importante del código para trasladar los cálculos de degradado fuera del control de flujo.</span><span class="sxs-lookup"><span data-stu-id="3c125-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="3c125-165">Si el extremo de D3DPSHADERCAPS2 \_ 0 se establece con D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, el compilador asigna esta función a texldd.</span><span class="sxs-lookup"><span data-stu-id="3c125-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c125-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c125-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c125-167">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3c125-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

