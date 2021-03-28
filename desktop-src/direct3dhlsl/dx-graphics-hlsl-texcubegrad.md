---
title: texCUBEgrad
description: Muestrea una textura de cubo usando un degradado para seleccionar el nivel de MIP. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- HLSL de texCUBEgrad
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 694382488754c221c59df72112678a5971e62c0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083624"
---
# <a name="texcubegrad"></a><span data-ttu-id="bddfa-105">texCUBEgrad</span><span class="sxs-lookup"><span data-stu-id="bddfa-105">texCUBEgrad</span></span>

<span data-ttu-id="bddfa-106">Muestrea una textura de cubo usando un degradado para seleccionar el nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="bddfa-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="bddfa-107">RET texCUBEgrad (s, t, DDX, DDY)</span><span class="sxs-lookup"><span data-stu-id="bddfa-107">ret texCUBEgrad(s, t, ddx, ddy)</span></span> |
|---------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="bddfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bddfa-108">Parameters</span></span>



| <span data-ttu-id="bddfa-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="bddfa-109">Item</span></span>                                                         | <span data-ttu-id="bddfa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bddfa-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bddfa-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="bddfa-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="bddfa-112">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="bddfa-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="bddfa-113"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="bddfa-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="bddfa-114">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="bddfa-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="bddfa-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="bddfa-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="bddfa-116">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="bddfa-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="bddfa-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="bddfa-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="bddfa-118">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="bddfa-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bddfa-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bddfa-119">Return Value</span></span>

<span data-ttu-id="bddfa-120">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="bddfa-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="bddfa-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="bddfa-121">Type Description</span></span>



| <span data-ttu-id="bddfa-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bddfa-122">Name</span></span> | <span data-ttu-id="bddfa-123">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="bddfa-123">In/Out</span></span> | [<span data-ttu-id="bddfa-124">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="bddfa-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="bddfa-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="bddfa-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bddfa-126">Tamaño</span><span class="sxs-lookup"><span data-stu-id="bddfa-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="bddfa-127">s</span><span class="sxs-lookup"><span data-stu-id="bddfa-127">s</span></span>    | <span data-ttu-id="bddfa-128">in</span><span class="sxs-lookup"><span data-stu-id="bddfa-128">in</span></span>     | [<span data-ttu-id="bddfa-129">**object**</span><span class="sxs-lookup"><span data-stu-id="bddfa-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bddfa-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="bddfa-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="bddfa-131">1</span><span class="sxs-lookup"><span data-stu-id="bddfa-131">1</span></span>    |
| <span data-ttu-id="bddfa-132">t</span><span class="sxs-lookup"><span data-stu-id="bddfa-132">t</span></span>    | <span data-ttu-id="bddfa-133">in</span><span class="sxs-lookup"><span data-stu-id="bddfa-133">in</span></span>     | [<span data-ttu-id="bddfa-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="bddfa-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bddfa-135">**flot**</span><span class="sxs-lookup"><span data-stu-id="bddfa-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bddfa-136">3</span><span class="sxs-lookup"><span data-stu-id="bddfa-136">3</span></span>    |
| <span data-ttu-id="bddfa-137">DDX</span><span class="sxs-lookup"><span data-stu-id="bddfa-137">ddx</span></span>  | <span data-ttu-id="bddfa-138">in</span><span class="sxs-lookup"><span data-stu-id="bddfa-138">in</span></span>     | [<span data-ttu-id="bddfa-139">**medios**</span><span class="sxs-lookup"><span data-stu-id="bddfa-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bddfa-140">**flot**</span><span class="sxs-lookup"><span data-stu-id="bddfa-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bddfa-141">3</span><span class="sxs-lookup"><span data-stu-id="bddfa-141">3</span></span>    |
| <span data-ttu-id="bddfa-142">ddy</span><span class="sxs-lookup"><span data-stu-id="bddfa-142">ddy</span></span>  | <span data-ttu-id="bddfa-143">in</span><span class="sxs-lookup"><span data-stu-id="bddfa-143">in</span></span>     | [<span data-ttu-id="bddfa-144">**medios**</span><span class="sxs-lookup"><span data-stu-id="bddfa-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bddfa-145">**flot**</span><span class="sxs-lookup"><span data-stu-id="bddfa-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bddfa-146">3</span><span class="sxs-lookup"><span data-stu-id="bddfa-146">3</span></span>    |
| <span data-ttu-id="bddfa-147">direcc</span><span class="sxs-lookup"><span data-stu-id="bddfa-147">ret</span></span>  | <span data-ttu-id="bddfa-148">out</span><span class="sxs-lookup"><span data-stu-id="bddfa-148">out</span></span>    | [<span data-ttu-id="bddfa-149">**medios**</span><span class="sxs-lookup"><span data-stu-id="bddfa-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bddfa-150">**float**</span><span class="sxs-lookup"><span data-stu-id="bddfa-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bddfa-151">4</span><span class="sxs-lookup"><span data-stu-id="bddfa-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bddfa-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="bddfa-152">Minimum Shader Model</span></span>

<span data-ttu-id="bddfa-153">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bddfa-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bddfa-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="bddfa-154">Shader Model</span></span>                                              | <span data-ttu-id="bddfa-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="bddfa-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="bddfa-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bddfa-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bddfa-157">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="bddfa-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="bddfa-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bddfa-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bddfa-159">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="bddfa-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="bddfa-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bddfa-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bddfa-161">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="bddfa-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="bddfa-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bddfa-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bddfa-163">no</span><span class="sxs-lookup"><span data-stu-id="bddfa-163">no</span></span>                       |



 

1.  <span data-ttu-id="bddfa-164">Se realiza una reordenación importante del código para trasladar los cálculos de degradado fuera del control de flujo.</span><span class="sxs-lookup"><span data-stu-id="bddfa-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="bddfa-165">Si el extremo de D3DPSHADERCAPS2 \_ 0 se establece con D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, el compilador asigna esta función a texldd.</span><span class="sxs-lookup"><span data-stu-id="bddfa-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="bddfa-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="bddfa-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddfa-167">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bddfa-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

