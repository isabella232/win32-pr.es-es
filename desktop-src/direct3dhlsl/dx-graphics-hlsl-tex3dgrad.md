---
title: tex3Dgrad
description: Muestrea una textura 3D usando un degradado para seleccionar el nivel de MIP. | tex3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- HLSL de tex3Dgrad
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986446"
---
# <a name="tex3dgrad"></a><span data-ttu-id="1a0ee-105">tex3Dgrad</span><span class="sxs-lookup"><span data-stu-id="1a0ee-105">tex3Dgrad</span></span>

<span data-ttu-id="1a0ee-106">Muestrea una textura 3D usando un degradado para seleccionar el nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="1a0ee-107">RET tex3Dgrad (s, t, DDX, DDY)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-107">ret tex3Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1a0ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a0ee-108">Parameters</span></span>



| <span data-ttu-id="1a0ee-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1a0ee-109">Item</span></span>                                                         | <span data-ttu-id="1a0ee-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a0ee-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1a0ee-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="1a0ee-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="1a0ee-112">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="1a0ee-113"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="1a0ee-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="1a0ee-114">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="1a0ee-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="1a0ee-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="1a0ee-116">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="1a0ee-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="1a0ee-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="1a0ee-118">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1a0ee-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a0ee-119">Return Value</span></span>

<span data-ttu-id="1a0ee-120">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="1a0ee-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="1a0ee-121">Type Description</span></span>



| <span data-ttu-id="1a0ee-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1a0ee-122">Name</span></span> | <span data-ttu-id="1a0ee-123">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="1a0ee-123">In/Out</span></span> | [<span data-ttu-id="1a0ee-124">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="1a0ee-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1a0ee-126">Tamaño</span><span class="sxs-lookup"><span data-stu-id="1a0ee-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="1a0ee-127">s</span><span class="sxs-lookup"><span data-stu-id="1a0ee-127">s</span></span>    | <span data-ttu-id="1a0ee-128">in</span><span class="sxs-lookup"><span data-stu-id="1a0ee-128">in</span></span>     | [<span data-ttu-id="1a0ee-129">**object**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a0ee-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="1a0ee-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="1a0ee-131">1</span><span class="sxs-lookup"><span data-stu-id="1a0ee-131">1</span></span>    |
| <span data-ttu-id="1a0ee-132">t</span><span class="sxs-lookup"><span data-stu-id="1a0ee-132">t</span></span>    | <span data-ttu-id="1a0ee-133">in</span><span class="sxs-lookup"><span data-stu-id="1a0ee-133">in</span></span>     | [<span data-ttu-id="1a0ee-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a0ee-135">**flot**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a0ee-136">3</span><span class="sxs-lookup"><span data-stu-id="1a0ee-136">3</span></span>    |
| <span data-ttu-id="1a0ee-137">DDX</span><span class="sxs-lookup"><span data-stu-id="1a0ee-137">ddx</span></span>  | <span data-ttu-id="1a0ee-138">in</span><span class="sxs-lookup"><span data-stu-id="1a0ee-138">in</span></span>     | [<span data-ttu-id="1a0ee-139">**medios**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a0ee-140">**flot**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a0ee-141">3</span><span class="sxs-lookup"><span data-stu-id="1a0ee-141">3</span></span>    |
| <span data-ttu-id="1a0ee-142">ddy</span><span class="sxs-lookup"><span data-stu-id="1a0ee-142">ddy</span></span>  | <span data-ttu-id="1a0ee-143">in</span><span class="sxs-lookup"><span data-stu-id="1a0ee-143">in</span></span>     | [<span data-ttu-id="1a0ee-144">**medios**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a0ee-145">**flot**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a0ee-146">3</span><span class="sxs-lookup"><span data-stu-id="1a0ee-146">3</span></span>    |
| <span data-ttu-id="1a0ee-147">direcc</span><span class="sxs-lookup"><span data-stu-id="1a0ee-147">ret</span></span>  | <span data-ttu-id="1a0ee-148">out</span><span class="sxs-lookup"><span data-stu-id="1a0ee-148">out</span></span>    | [<span data-ttu-id="1a0ee-149">**medios**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1a0ee-150">**float**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1a0ee-151">4</span><span class="sxs-lookup"><span data-stu-id="1a0ee-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a0ee-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1a0ee-152">Minimum Shader Model</span></span>

<span data-ttu-id="1a0ee-153">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1a0ee-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1a0ee-154">Shader Model</span></span>                                              | <span data-ttu-id="1a0ee-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="1a0ee-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="1a0ee-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1a0ee-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1a0ee-157">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="1a0ee-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1a0ee-159">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="1a0ee-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1a0ee-161">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="1a0ee-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1a0ee-163">no</span><span class="sxs-lookup"><span data-stu-id="1a0ee-163">no</span></span>                       |



 

1.  <span data-ttu-id="1a0ee-164">Se realiza una reordenación importante del código para trasladar los cálculos de degradado fuera del control de flujo.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="1a0ee-165">Si el extremo de D3DPSHADERCAPS2 \_ 0 se establece con D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, el compilador asigna esta función a texldd.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a0ee-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a0ee-166">Remarks</span></span>

<span data-ttu-id="1a0ee-167">Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden reducir las rutas de acceso de control de flujo independientes.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="1a0ee-168">Por lo tanto, se considera que no es válido usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentre dentro de una construcción de control de flujo que podría variar en píxeles para que se rasterizase un primitivo determinado.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="1a0ee-169">Si uno de los lados de una instrucción **If** con el atributo Branch usa una función de degradado, puede generarse un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="1a0ee-170">Vea la [instrucción if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="1a0ee-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a0ee-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a0ee-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0ee-172">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

