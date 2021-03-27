---
title: 'tex3D (referencia de HLSL): seleccionar el nivel de MIP'
description: Muestrea una textura 3D usando un degradado para seleccionar el nivel de MIP. | tex3D (referencia de HLSL)
ms.assetid: b48a6791-61b7-4a13-9357-923910515164
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
ms.openlocfilehash: 965c9229d4d54fafdb2da9a84119365075a3f903
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104280535"
---
# <a name="tex3d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="e8532-105">tex3D (referencia de HLSL): seleccionar el nivel de MIP</span><span class="sxs-lookup"><span data-stu-id="e8532-105">tex3D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="e8532-106">Muestrea una textura 3D usando un degradado para seleccionar el nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="e8532-106">Samples a 3D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="e8532-107">RET tex3D (s, t, DDX, DDY)</span><span class="sxs-lookup"><span data-stu-id="e8532-107">ret tex3D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="e8532-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8532-108">Parameters</span></span>



| <span data-ttu-id="e8532-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8532-109">Item</span></span>                                                         | <span data-ttu-id="e8532-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8532-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e8532-111"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="e8532-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="e8532-112">\[en \] el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="e8532-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="e8532-113"><span id="t"></span><span id="T"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="e8532-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="e8532-114">\[en \] la coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="e8532-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="e8532-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="e8532-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="e8532-116">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="e8532-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="e8532-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="e8532-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="e8532-118">\[en \] la velocidad de cambio de la geometría de la superficie en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="e8532-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="e8532-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8532-119">Return Value</span></span>

<span data-ttu-id="e8532-120">Valor de los datos de textura.</span><span class="sxs-lookup"><span data-stu-id="e8532-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="e8532-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="e8532-121">Type Description</span></span>



| <span data-ttu-id="e8532-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8532-122">Name</span></span> | <span data-ttu-id="e8532-123">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="e8532-123">In/Out</span></span> | [<span data-ttu-id="e8532-124">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="e8532-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="e8532-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="e8532-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="e8532-126">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e8532-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="e8532-127">s</span><span class="sxs-lookup"><span data-stu-id="e8532-127">s</span></span>    | <span data-ttu-id="e8532-128">in</span><span class="sxs-lookup"><span data-stu-id="e8532-128">in</span></span>     | [<span data-ttu-id="e8532-129">**object**</span><span class="sxs-lookup"><span data-stu-id="e8532-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8532-130">sampler3D</span><span class="sxs-lookup"><span data-stu-id="e8532-130">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="e8532-131">1</span><span class="sxs-lookup"><span data-stu-id="e8532-131">1</span></span>    |
| <span data-ttu-id="e8532-132">t</span><span class="sxs-lookup"><span data-stu-id="e8532-132">t</span></span>    | <span data-ttu-id="e8532-133">in</span><span class="sxs-lookup"><span data-stu-id="e8532-133">in</span></span>     | [<span data-ttu-id="e8532-134">**medios**</span><span class="sxs-lookup"><span data-stu-id="e8532-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8532-135">**flot**</span><span class="sxs-lookup"><span data-stu-id="e8532-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8532-136">3</span><span class="sxs-lookup"><span data-stu-id="e8532-136">3</span></span>    |
| <span data-ttu-id="e8532-137">DDX</span><span class="sxs-lookup"><span data-stu-id="e8532-137">ddx</span></span>  | <span data-ttu-id="e8532-138">in</span><span class="sxs-lookup"><span data-stu-id="e8532-138">in</span></span>     | [<span data-ttu-id="e8532-139">**medios**</span><span class="sxs-lookup"><span data-stu-id="e8532-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8532-140">**flot**</span><span class="sxs-lookup"><span data-stu-id="e8532-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8532-141">3</span><span class="sxs-lookup"><span data-stu-id="e8532-141">3</span></span>    |
| <span data-ttu-id="e8532-142">ddy</span><span class="sxs-lookup"><span data-stu-id="e8532-142">ddy</span></span>  | <span data-ttu-id="e8532-143">in</span><span class="sxs-lookup"><span data-stu-id="e8532-143">in</span></span>     | [<span data-ttu-id="e8532-144">**medios**</span><span class="sxs-lookup"><span data-stu-id="e8532-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8532-145">**flot**</span><span class="sxs-lookup"><span data-stu-id="e8532-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8532-146">3</span><span class="sxs-lookup"><span data-stu-id="e8532-146">3</span></span>    |
| <span data-ttu-id="e8532-147">direcc</span><span class="sxs-lookup"><span data-stu-id="e8532-147">ret</span></span>  | <span data-ttu-id="e8532-148">out</span><span class="sxs-lookup"><span data-stu-id="e8532-148">out</span></span>    | [<span data-ttu-id="e8532-149">**medios**</span><span class="sxs-lookup"><span data-stu-id="e8532-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="e8532-150">**float**</span><span class="sxs-lookup"><span data-stu-id="e8532-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="e8532-151">4</span><span class="sxs-lookup"><span data-stu-id="e8532-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8532-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e8532-152">Minimum Shader Model</span></span>

<span data-ttu-id="e8532-153">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e8532-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e8532-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e8532-154">Shader Model</span></span>                                              | <span data-ttu-id="e8532-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="e8532-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="e8532-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e8532-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8532-157">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="e8532-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="e8532-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8532-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8532-159">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="e8532-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="e8532-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8532-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8532-161">sí (solo sombreador de píxeles)</span><span class="sxs-lookup"><span data-stu-id="e8532-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="e8532-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8532-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8532-163">no</span><span class="sxs-lookup"><span data-stu-id="e8532-163">no</span></span>                       |



 

1.  <span data-ttu-id="e8532-164">Se realiza una reordenación importante del código para trasladar los cálculos de degradado fuera del control de flujo.</span><span class="sxs-lookup"><span data-stu-id="e8532-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="e8532-165">Si el extremo de D3DPSHADERCAPS2 \_ 0 se establece con D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, el compilador asigna esta función a texldd.</span><span class="sxs-lookup"><span data-stu-id="e8532-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8532-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8532-166">Remarks</span></span>

<span data-ttu-id="e8532-167">Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden reducir las rutas de acceso de control de flujo independientes.</span><span class="sxs-lookup"><span data-stu-id="e8532-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="e8532-168">Por lo tanto, se considera que no es válido usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentre dentro de una construcción de control de flujo que podría variar en píxeles para que se rasterizase un primitivo determinado.</span><span class="sxs-lookup"><span data-stu-id="e8532-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="e8532-169">Si uno de los lados de una instrucción **If** con el atributo Branch usa una función de degradado, puede generarse un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="e8532-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="e8532-170">Vea la [instrucción if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="e8532-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e8532-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8532-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8532-172">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="e8532-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

