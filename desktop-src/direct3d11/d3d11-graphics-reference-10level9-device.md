---
title: Métodos 10Level9 ID3D11Device
description: En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421155"
---
# <a name="10level9-id3d11device-methods"></a><span data-ttu-id="1c568-103">Métodos 10Level9 ID3D11Device</span><span class="sxs-lookup"><span data-stu-id="1c568-103">10Level9 ID3D11Device Methods</span></span>

<span data-ttu-id="1c568-104">En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="1c568-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) methods.</span></span>

-   [<span data-ttu-id="1c568-105">ID3D11Device:: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="1c568-105">ID3D11Device::CheckCounter</span></span>](#id3d11devicecheckcounter)
-   [<span data-ttu-id="1c568-106">ID3D11Device:: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="1c568-106">ID3D11Device::CheckFormatSupport</span></span>](#id3d11devicecheckformatsupport)
-   [<span data-ttu-id="1c568-107">ID3D11Device:: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="1c568-107">ID3D11Device::CheckMultisampleQualityLevels</span></span>](#id3d11devicecheckmultisamplequalitylevels)
-   [<span data-ttu-id="1c568-108">ID3D11Device:: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="1c568-108">ID3D11Device::CreateBlendState</span></span>](#id3d11devicecreateblendstate)
-   [<span data-ttu-id="1c568-109">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="1c568-109">ID3D11Device::CreateBlendState1</span></span>](#id3d11devicecreateblendstate1)
-   [<span data-ttu-id="1c568-110">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="1c568-110">ID3D11Device::CreateBuffer</span></span>](#id3d11devicecreatebuffer)
-   [<span data-ttu-id="1c568-111">ID3D11Device:: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="1c568-111">ID3D11Device::CreateCounter</span></span>](#id3d11devicecreatecounter)
-   [<span data-ttu-id="1c568-112">ID3D11Device:: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="1c568-112">ID3D11Device::CreateDepthStencilView</span></span>](#id3d11devicecreatedepthstencilview)
-   [<span data-ttu-id="1c568-113">ID3D11Device:: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="1c568-113">ID3D11Device::CreateDomainShader</span></span>](#id3d11devicecreatedomainshader)
-   [<span data-ttu-id="1c568-114">ID3D11Device:: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="1c568-114">ID3D11Device::CreateGeometryShader</span></span>](#id3d11devicecreategeometryshader)
-   [<span data-ttu-id="1c568-115">ID3D11Device:: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="1c568-115">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="1c568-116">ID3D11Device:: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="1c568-116">ID3D11Device::CreateHullShader</span></span>](#id3d11devicecreatehullshader)
-   [<span data-ttu-id="1c568-117">ID3D11Device:: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="1c568-117">ID3D11Device::CreateInputLayout</span></span>](#id3d11devicecreateinputlayout)
-   [<span data-ttu-id="1c568-118">ID3D11Device:: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="1c568-118">ID3D11Device::CreatePixelShader</span></span>](#id3d11devicecreatepixelshader)
-   [<span data-ttu-id="1c568-119">ID3D11Device:: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="1c568-119">ID3D11Device::CreatePredicate</span></span>](#id3d11devicecreatepredicate)
-   [<span data-ttu-id="1c568-120">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="1c568-120">ID3D11Device::CreateQuery</span></span>](#id3d11devicecreatequery)
-   [<span data-ttu-id="1c568-121">ID3D11Device:: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="1c568-121">ID3D11Device::CreateRasterizerState</span></span>](#id3d11devicecreaterasterizerstate)
-   [<span data-ttu-id="1c568-122">ID3D11Device:: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="1c568-122">ID3D11Device::CreateRenderTargetView</span></span>](#id3d11devicecreaterendertargetview)
-   [<span data-ttu-id="1c568-123">ID3D11Device:: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="1c568-123">ID3D11Device::CreateSamplerState</span></span>](#id3d11devicecreatesamplerstate)
-   [<span data-ttu-id="1c568-124">ID3D11Device:: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="1c568-124">ID3D11Device::CreateShaderResourceView</span></span>](#id3d11devicecreateshaderresourceview)
-   [<span data-ttu-id="1c568-125">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="1c568-125">ID3D11Device::CreateTexture1D</span></span>](#id3d11devicecreatetexture1d)
-   [<span data-ttu-id="1c568-126">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="1c568-126">ID3D11Device::CreateTexture2D</span></span>](#id3d11devicecreatetexture2d)
-   [<span data-ttu-id="1c568-127">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="1c568-127">ID3D11Device::CreateTexture3D</span></span>](#id3d11devicecreatetexture3d)
-   [<span data-ttu-id="1c568-128">ID3D11Device:: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="1c568-128">ID3D11Device::CreateUnorderedAccessView</span></span>](#id3d11devicecreateunorderedaccessview)
-   [<span data-ttu-id="1c568-129">ID3D11Device:: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="1c568-129">ID3D11Device::CreateVertexShader</span></span>](#id3d11devicecreatevertexshader)
-   [<span data-ttu-id="1c568-130">ID3D11Device:: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="1c568-130">ID3D11Device::OpenSharedResource</span></span>](#id3d11deviceopensharedresource)
-   [<span data-ttu-id="1c568-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c568-131">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecheckcounter"></a><span data-ttu-id="1c568-132">ID3D11Device:: CheckCounter</span><span class="sxs-lookup"><span data-stu-id="1c568-132">ID3D11Device::CheckCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-133">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-133">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-134">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-134">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-135">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-135">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-136">Los contadores dependientes del dispositivo se admiten opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="1c568-136">Device-dependent counters are optionally supported.</span></span> <span data-ttu-id="1c568-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> para determinar la compatibilidad. $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1c568-137">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> to determine support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-138">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-138">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-139">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-139">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a><span data-ttu-id="1c568-140">ID3D11Device:: CheckFormatSupport</span><span class="sxs-lookup"><span data-stu-id="1c568-140">ID3D11Device::CheckFormatSupport</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-141">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-141">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-142">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-142">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-143">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-143">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-144">Consulte compatibilidad con el formato de <a href="overviews-direct3d-11-devices-downlevel-intro.md">nivel de característica</a>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="1c568-144">See format support by <a href="overviews-direct3d-11-devices-downlevel-intro.md">feature level</a>${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-145">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-145">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-146">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-146">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a><span data-ttu-id="1c568-147">ID3D11Device:: CheckMultisampleQualityLevels</span><span class="sxs-lookup"><span data-stu-id="1c568-147">ID3D11Device::CheckMultisampleQualityLevels</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-148">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-148">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-149">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-149">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-150">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-150">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-151">Los niveles de características no ofrecen ninguna garantía sobre el soporte técnico de MSAA. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-151">Feature levels make no guarantees concerning MSAA support.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-152">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-152">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-153">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-153">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a><span data-ttu-id="1c568-154">ID3D11Device:: CreateBlendState</span><span class="sxs-lookup"><span data-stu-id="1c568-154">ID3D11Device::CreateBlendState</span></span>



| <span data-ttu-id="1c568-155">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-155">Feature Level</span></span>              | <span data-ttu-id="1c568-156">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-156">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c568-157">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-157">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="1c568-158">AlphaToCoverageEnable debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="1c568-158">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="1c568-159">Los primeros cuatro BlendEnables deben tener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="1c568-159">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="1c568-160">\_No se admite D3D11 Blend \_ src \_ ALPHASAT.</span><span class="sxs-lookup"><span data-stu-id="1c568-160">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="1c568-161">No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)</span><span class="sxs-lookup"><span data-stu-id="1c568-161">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="1c568-162">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-162">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="1c568-163">AlphaToCoverageEnable debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="1c568-163">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="1c568-164">Los primeros cuatro BlendEnables deben tener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="1c568-164">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="1c568-165">Los primeros cuatro RenderTargetWriteMasks deben tener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="1c568-165">The first four RenderTargetWriteMasks must all have the same value.</span></span><br/> <span data-ttu-id="1c568-166">\_No se admite D3D11 Blend \_ src \_ ALPHASAT.</span><span class="sxs-lookup"><span data-stu-id="1c568-166">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="1c568-167">No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)</span><span class="sxs-lookup"><span data-stu-id="1c568-167">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/> |
| <span data-ttu-id="1c568-168">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-168">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="1c568-169">AlphaToCoverageEnable debe ser **false**.</span><span class="sxs-lookup"><span data-stu-id="1c568-169">AlphaToCoverageEnable must be **FALSE**.</span></span><br/> <span data-ttu-id="1c568-170">Los primeros cuatro BlendEnables deben tener el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="1c568-170">The first four BlendEnables must all have the same value.</span></span><br/> <span data-ttu-id="1c568-171">\_No se admite D3D11 Blend \_ src \_ ALPHASAT.</span><span class="sxs-lookup"><span data-stu-id="1c568-171">D3D11\_BLEND\_SRC\_ALPHASAT not supported.</span></span><br/> <span data-ttu-id="1c568-172">No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)</span><span class="sxs-lookup"><span data-stu-id="1c568-172">Dual-source color blend not supported (any SrcBlend or DestBlend with SRC1 in the name)</span></span><br/>                                                                                |
| <span data-ttu-id="1c568-173">Nivel de característica de D3D \_ \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1c568-173">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="1c568-174">Agrega alfa a cobertura</span><span class="sxs-lookup"><span data-stu-id="1c568-174">Adds alpha-to-coverage</span></span>                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a><span data-ttu-id="1c568-175">ID3D11Device:: CreateBlendState1</span><span class="sxs-lookup"><span data-stu-id="1c568-175">ID3D11Device::CreateBlendState1</span></span>



| <span data-ttu-id="1c568-176">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-176">Feature Level</span></span>              | <span data-ttu-id="1c568-177">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-177">Behavior Differences</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c568-178">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-178">D3D\_FEATURE\_LEVEL\_9\_1</span></span>  | <span data-ttu-id="1c568-179">No compatible</span><span class="sxs-lookup"><span data-stu-id="1c568-179">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1c568-180">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-180">D3D\_FEATURE\_LEVEL\_9\_2</span></span>  | <span data-ttu-id="1c568-181">No compatible</span><span class="sxs-lookup"><span data-stu-id="1c568-181">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1c568-182">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-182">D3D\_FEATURE\_LEVEL\_9\_3</span></span>  | <span data-ttu-id="1c568-183">No compatible</span><span class="sxs-lookup"><span data-stu-id="1c568-183">Unsupported</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1c568-184">Nivel de característica de D3D \_ \_ \_ 10 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1c568-184">D3D\_FEATURE\_LEVEL\_10\_0</span></span> | <span data-ttu-id="1c568-185">El miembro *OutputMergerLogicOp* se ha agregado a [**\_ \_ \_ \_ las opciones de D3D11 de datos de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), para determinar la compatibilidad con las operaciones lógicas (operaciones de lógica bit a bit entre el resultado del sombreador de píxeles y el contenido de destino de representación, consulte [**D3D11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span><span class="sxs-lookup"><span data-stu-id="1c568-185">The *OutputMergerLogicOp* member has been added to [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), to determine support for logical operations (bitwise logic operations between pixel shader output and render target contents, refer to [**D3D11\_RENDER\_TARGET\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)).</span></span> |



 

## <a name="id3d11devicecreatebuffer"></a><span data-ttu-id="1c568-186">ID3D11Device:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="1c568-186">ID3D11Device::CreateBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-187">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-187">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-188">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-188">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-189">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-189">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="1c568-190">Los búferes no pueden tener vistas de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1c568-190">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="1c568-191">Los búferes deben tener exactamente uno de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="1c568-191">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="1c568-192">Solo permite búferes de índice con el formato de DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="1c568-192">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-193">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-193">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="1c568-194">Los búferes no pueden tener vistas de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1c568-194">Buffers can't have render target views.</span></span><br/> <span data-ttu-id="1c568-195">Los búferes deben tener exactamente uno de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.</span><span class="sxs-lookup"><span data-stu-id="1c568-195">Buffers must have exactly one of D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER, or D3D11_BIND_CONSTANT_BUFFER.</span></span><br/> <span data-ttu-id="1c568-196">Permite búferes de índice con los formatos DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1c568-196">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="1c568-197">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-197">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-198">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-198">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a><span data-ttu-id="1c568-199">ID3D11Device:: CreateCounter</span><span class="sxs-lookup"><span data-stu-id="1c568-199">ID3D11Device::CreateCounter</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-200">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-200">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-201">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-201">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-202">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-202">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-203">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-203">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-204">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-204">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-205">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-205">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a><span data-ttu-id="1c568-206">ID3D11Device:: CreateDepthStencilView</span><span class="sxs-lookup"><span data-stu-id="1c568-206">ID3D11Device::CreateDepthStencilView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-207">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-207">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-208">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-208">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-209">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-209">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-210">No admite la galería de símbolos de dos caras. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-210">Does not support two-sided stencil.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-211">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-211">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-212">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-212">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a><span data-ttu-id="1c568-213">ID3D11Device:: CreateDomainShader</span><span class="sxs-lookup"><span data-stu-id="1c568-213">ID3D11Device::CreateDomainShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-214">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-214">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-215">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-215">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-216">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-216">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1c568-217">No se admite en cualquier nivel de características 9. \* o 10. \*.</span><span class="sxs-lookup"><span data-stu-id="1c568-217">Not supported on any 9.\* or 10.\* feature level.</span></span> <span data-ttu-id="1c568-218">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-218">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-219">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-219">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-220">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-220">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1c568-221">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1c568-221">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-222">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1c568-222">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a><span data-ttu-id="1c568-223">ID3D11Device:: CreateGeometryShader</span><span class="sxs-lookup"><span data-stu-id="1c568-223">ID3D11Device::CreateGeometryShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-224">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-224">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-225">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-225">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-226">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-226">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-227">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-227">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-228">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-228">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-229">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-229">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a><span data-ttu-id="1c568-230">ID3D11Device:: CreateGeometryShaderWithStreamOutput</span><span class="sxs-lookup"><span data-stu-id="1c568-230">ID3D11Device::CreateGeometryShaderWithStreamOutput</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-231">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-231">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-232">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-232">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-233">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-233">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-234">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-234">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-235">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-235">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-236">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-236">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a><span data-ttu-id="1c568-237">ID3D11Device:: CreateHullShader</span><span class="sxs-lookup"><span data-stu-id="1c568-237">ID3D11Device::CreateHullShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-238">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-238">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-239">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-239">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-240">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-240">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="1c568-241">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-241">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-242">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-242">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-243">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-243">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="1c568-244">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="1c568-244">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-245">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="1c568-245">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a><span data-ttu-id="1c568-246">ID3D11Device:: CreateInputLayout</span><span class="sxs-lookup"><span data-stu-id="1c568-246">ID3D11Device::CreateInputLayout</span></span>



| <span data-ttu-id="1c568-247">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-247">Feature Level</span></span>             | <span data-ttu-id="1c568-248">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-248">Behavior Differences</span></span>                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c568-249">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-249">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-250">No admite datos de \_ entrada D3D11 \_ por \_ instancia \_</span><span class="sxs-lookup"><span data-stu-id="1c568-250">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="1c568-251">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-251">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-252">No admite datos de \_ entrada D3D11 \_ por \_ instancia \_</span><span class="sxs-lookup"><span data-stu-id="1c568-252">Does not support D3D11\_INPUT\_PER\_INSTANCE\_DATA</span></span>                                                                |
| <span data-ttu-id="1c568-253">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-253">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-254">El flujo de vértices cero debe tener \_ una entrada D3D11 \_ por \_ \_ datos de vértice, si alguna secuencia tiene una \_ entrada D3D11 \_ por \_ datos de vértice \_</span><span class="sxs-lookup"><span data-stu-id="1c568-254">Vertex stream zero must have D3D11\_INPUT\_PER\_VERTEX\_DATA, if any streams have D3D11\_INPUT\_PER\_VERTEX\_DATA</span></span> |



 

<span data-ttu-id="1c568-255">Para más información sobre los formatos que se pueden usar para los datos de vértices en cada nivel de característica, vea el gráfico compatibilidad con el formato de [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) .</span><span class="sxs-lookup"><span data-stu-id="1c568-255">See the format support by [feature level chart](overviews-direct3d-11-devices-downlevel-intro.md) for details on what formats can be used for vertex data at each feature level.</span></span>

## <a name="id3d11devicecreatepixelshader"></a><span data-ttu-id="1c568-256">ID3D11Device:: CreatePixelShader</span><span class="sxs-lookup"><span data-stu-id="1c568-256">ID3D11Device::CreatePixelShader</span></span>



| <span data-ttu-id="1c568-257">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-257">Feature Level</span></span>             | <span data-ttu-id="1c568-258">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-258">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="1c568-259">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-259">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-260">Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-260">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="1c568-261">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-261">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-262">Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-262">Must use ps\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="1c568-263">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-264">Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 3 o PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-264">Must use ps\_4\_0\_level\_9\_3 or ps\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11devicecreatepredicate"></a><span data-ttu-id="1c568-265">ID3D11Device:: CreatePredicate</span><span class="sxs-lookup"><span data-stu-id="1c568-265">ID3D11Device::CreatePredicate</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-266">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-266">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-267">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-267">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-268">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-268">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-269">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-269">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-270">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-270">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-271">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-271">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a><span data-ttu-id="1c568-272">ID3D11Device:: CreateQuery</span><span class="sxs-lookup"><span data-stu-id="1c568-272">ID3D11Device::CreateQuery</span></span>



| <span data-ttu-id="1c568-273">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-273">Feature Level</span></span>             | <span data-ttu-id="1c568-274">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-274">Behavior Differences</span></span>                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c568-275">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-275">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-276">Se admiten las consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="1c568-276">Event queries are supported.</span></span> <span data-ttu-id="1c568-277">Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="1c568-277">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span>               |
| <span data-ttu-id="1c568-278">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-278">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-279">Se admiten las consultas de eventos y de oclusión.</span><span class="sxs-lookup"><span data-stu-id="1c568-279">Event and occlusion queries are supported.</span></span> <span data-ttu-id="1c568-280">Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="1c568-280">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |
| <span data-ttu-id="1c568-281">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-281">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-282">Se admiten las consultas de eventos y de oclusión.</span><span class="sxs-lookup"><span data-stu-id="1c568-282">Event and occlusion queries are supported.</span></span> <span data-ttu-id="1c568-283">Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="1c568-283">Timestamp queries are optional: call [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) to determine support.</span></span> |



 

## <a name="id3d11devicecreaterasterizerstate"></a><span data-ttu-id="1c568-284">ID3D11Device:: CreateRasterizerState</span><span class="sxs-lookup"><span data-stu-id="1c568-284">ID3D11Device::CreateRasterizerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-285">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-285">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-286">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-286">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-287">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-287">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-288">DepthClipEnable debe ser <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c568-288">DepthClipEnable must be <strong>TRUE</strong>.</span></span> <span data-ttu-id="1c568-289">DepthBiasClamp debe establecerse en 0. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-289">DepthBiasClamp must be set to 0.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-290">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-290">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-291">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-291">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a><span data-ttu-id="1c568-292">ID3D11Device:: CreateRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="1c568-292">ID3D11Device::CreateRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-293">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-293">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-294">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-294">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-295">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-295">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-296">Solo puede admitir vistas de destino de representación de objetos Texture2D. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-296">Can only support render target views of Texture2D objects.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-297">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-297">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-298">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-298">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a><span data-ttu-id="1c568-299">ID3D11Device:: CreateSamplerState</span><span class="sxs-lookup"><span data-stu-id="1c568-299">ID3D11Device::CreateSamplerState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-300">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-300">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-301">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-301">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-302">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-302">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="1c568-303">No se admite el filtro de comparación.</span><span class="sxs-lookup"><span data-stu-id="1c568-303">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="1c568-304">El color del borde debe estar comprendido entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="1c568-304">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="1c568-305">El LOD mínimo no puede ser fraccionario</span><span class="sxs-lookup"><span data-stu-id="1c568-305">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="1c568-306">El máximo de LOD debe ser FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="1c568-306">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="1c568-307">El valor máximo de anisotropía es 2.</span><span class="sxs-lookup"><span data-stu-id="1c568-307">Maximum anisotropy is 2.</span></span><br/> <span data-ttu-id="1c568-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE no se admiten.</span><span class="sxs-lookup"><span data-stu-id="1c568-308">D3D11_TEXTURE_ADDRESS_MIRRORONCE not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-309">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-309">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="1c568-310">No se admite el filtro de comparación.</span><span class="sxs-lookup"><span data-stu-id="1c568-310">Comparison filter is not supported.</span></span><br/> <span data-ttu-id="1c568-311">El color del borde debe estar comprendido entre [0, 1]</span><span class="sxs-lookup"><span data-stu-id="1c568-311">Border color must be within [0,1]</span></span><br/> <span data-ttu-id="1c568-312">El LOD mínimo no puede ser fraccionario</span><span class="sxs-lookup"><span data-stu-id="1c568-312">Min LOD cannot be fractional</span></span><br/> <span data-ttu-id="1c568-313">El máximo de LOD debe ser FLT_MAX</span><span class="sxs-lookup"><span data-stu-id="1c568-313">Max LOD must be FLT_MAX</span></span><br/> <span data-ttu-id="1c568-314">El valor máximo de anisotropía es 16.</span><span class="sxs-lookup"><span data-stu-id="1c568-314">Maximum anisotropy is 16.</span></span><br/> <span data-ttu-id="1c568-315">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-315">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-316">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-316">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a><span data-ttu-id="1c568-317">ID3D11Device:: CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="1c568-317">ID3D11Device::CreateShaderResourceView</span></span>



| <span data-ttu-id="1c568-318">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-318">Feature Level</span></span>             | <span data-ttu-id="1c568-319">MostDetailedMip Plus MipLevels debe incluir el valor de LOD más bajo (subrecurso más pequeño</span><span class="sxs-lookup"><span data-stu-id="1c568-319">MostDetailedMip plus MipLevels must include lowest LOD (smallest subresource</span></span> | <span data-ttu-id="1c568-320">La vista debe incluir todos los elementos de la matriz de recursos</span><span class="sxs-lookup"><span data-stu-id="1c568-320">View must include all resource array elements</span></span> |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="1c568-321">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-321">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-322">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-322">Yes</span></span>                                                                          | <span data-ttu-id="1c568-323">sí</span><span class="sxs-lookup"><span data-stu-id="1c568-323">yes</span></span>                                           |
| <span data-ttu-id="1c568-324">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-324">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-325">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-325">Yes</span></span>                                                                          | <span data-ttu-id="1c568-326">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-326">Yes</span></span>                                           |
| <span data-ttu-id="1c568-327">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-327">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-328">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-328">Yes</span></span>                                                                          | <span data-ttu-id="1c568-329">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-329">Yes</span></span>                                           |



 

## <a name="id3d11devicecreatetexture1d"></a><span data-ttu-id="1c568-330">ID3D11Device:: CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="1c568-330">ID3D11Device::CreateTexture1D</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-331">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-331">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-332">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-332">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-333">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-333">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-334">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-334">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-335">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-335">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-336">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-336">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a><span data-ttu-id="1c568-337">ID3D11Device:: CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="1c568-337">ID3D11Device::CreateTexture2D</span></span>

<span data-ttu-id="1c568-338">Los recursos de Texture2D tienen límites en el ancho y el alto que difieren entre [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md).</span><span class="sxs-lookup"><span data-stu-id="1c568-338">Texture2D resources have limits on their width and height that differ across [feature levels](overviews-direct3d-11-devices-downlevel-intro.md).</span></span> <span data-ttu-id="1c568-339">En los niveles de características 9 \_ 3, los siguientes son mínimos garantizados y las implementaciones individuales pueden superar los requisitos.</span><span class="sxs-lookup"><span data-stu-id="1c568-339">In feature levels 9\_3, the following are guaranteed minima, and individual implementations may exceed the requirements.</span></span>



| <span data-ttu-id="1c568-340">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-340">Feature Level</span></span>             | <span data-ttu-id="1c568-341">Si MipCount > 1, las dimensiones deben ser potencia integral de dos.</span><span class="sxs-lookup"><span data-stu-id="1c568-341">If MipCount > 1, Dimensions must be integral power of two</span></span> | <span data-ttu-id="1c568-342">Dimensión de textura mínima admitida</span><span class="sxs-lookup"><span data-stu-id="1c568-342">Minimum supported texture dimension</span></span> | <span data-ttu-id="1c568-343">Las dimensiones de las texturas del cubo deben ser potencia de dos</span><span class="sxs-lookup"><span data-stu-id="1c568-343">Cube textures dimensions must be power of two</span></span> | <span data-ttu-id="1c568-344">Si \_ se establece varios TEXTURECUBE, el valor de tamaño es:</span><span class="sxs-lookup"><span data-stu-id="1c568-344">If MISC\_TEXTURECUBE is set, the ArraySize is:</span></span> | <span data-ttu-id="1c568-345">Si \_ no se establece TEXTURECUBE, el valor de tamaño es.</span><span class="sxs-lookup"><span data-stu-id="1c568-345">If MISC\_TEXTURECUBE is not set, the ArraySize is.</span></span> |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="1c568-346">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-346">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-347">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-347">Yes</span></span>                                                          | <span data-ttu-id="1c568-348">2048</span><span class="sxs-lookup"><span data-stu-id="1c568-348">2048</span></span>                                | <span data-ttu-id="1c568-349">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-349">Yes</span></span>                                           | <span data-ttu-id="1c568-350">6</span><span class="sxs-lookup"><span data-stu-id="1c568-350">6</span></span>                                              | <span data-ttu-id="1c568-351">1</span><span class="sxs-lookup"><span data-stu-id="1c568-351">1</span></span>                                                  |
| <span data-ttu-id="1c568-352">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-352">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-353">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-353">Yes</span></span>                                                          | <span data-ttu-id="1c568-354">2048</span><span class="sxs-lookup"><span data-stu-id="1c568-354">2048</span></span>                                | <span data-ttu-id="1c568-355">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-355">Yes</span></span>                                           | <span data-ttu-id="1c568-356">6</span><span class="sxs-lookup"><span data-stu-id="1c568-356">6</span></span>                                              | <span data-ttu-id="1c568-357">1</span><span class="sxs-lookup"><span data-stu-id="1c568-357">1</span></span>                                                  |
| <span data-ttu-id="1c568-358">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-358">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-359">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-359">Yes</span></span>                                                          | <span data-ttu-id="1c568-360">4096</span><span class="sxs-lookup"><span data-stu-id="1c568-360">4096</span></span>                                | <span data-ttu-id="1c568-361">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-361">Yes</span></span>                                           | <span data-ttu-id="1c568-362">6</span><span class="sxs-lookup"><span data-stu-id="1c568-362">6</span></span>                                              | <span data-ttu-id="1c568-363">1</span><span class="sxs-lookup"><span data-stu-id="1c568-363">1</span></span>                                                  |



 

<span data-ttu-id="1c568-364">En la tabla anterior, el nombre completo de **\_ TEXTURECUBE** es [**D3D11 \_ Resource \_ Misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="1c568-364">In the previous table, the full name of **MISC\_TEXTURECUBE** is [**D3D11\_RESOURCE\_MISC\_TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).</span></span>

<span data-ttu-id="1c568-365">Lo siguiente es cierto para los 9 \_ \* [niveles de características](overviews-direct3d-11-devices-downlevel-intro.md):</span><span class="sxs-lookup"><span data-stu-id="1c568-365">The following are true for all 9\_\* [feature levels](overviews-direct3d-11-devices-downlevel-intro.md):</span></span>

-   <span data-ttu-id="1c568-366">Cuando se usa \_ el \_ valor predeterminado de uso de D3D11 o el \_ uso \_ de D3D11 inmutable, BindFlags no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="1c568-366">When using D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>
-   <span data-ttu-id="1c568-367">Al usar la \_ \_ \_ Galería de símbolos de profundidad de enlace de D3D11, MipLevels debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="1c568-367">When using D3D11\_BIND\_DEPTH\_STENCIL, MipLevels must be 1.</span></span>
-   <span data-ttu-id="1c568-368">Al usar el \_ \_ \_ recurso de sombreador de enlace de D3D11, SampleDesc. Count debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="1c568-368">When using D3D11\_BIND\_SHADER\_RESOURCE, SampleDesc.Count must be 1.</span></span>
-   <span data-ttu-id="1c568-369">Cuando se usa el \_ enlace D3D11 \_ presente, el recurso no puede tener el \_ recurso de sombreador de enlace D3D11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1c568-369">When using D3D11\_BIND\_PRESENT, resource cannot have D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
-   <span data-ttu-id="1c568-370">Cuando se usa \_ el \_ recurso D3D10 DDI \_ varios \_ compartido, el formato no puede ser dxgi \_ format \_ R8G8B8A8 \_ UNORM o dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="1c568-370">When using D3D10\_DDI\_RESOURCE\_MISC\_SHARED, Format cannot be DXGI\_FORMAT\_R8G8B8A8\_UNORM or DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="id3d11devicecreatetexture3d"></a><span data-ttu-id="1c568-371">ID3D11Device:: CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="1c568-371">ID3D11Device::CreateTexture3D</span></span>



| <span data-ttu-id="1c568-372">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-372">Feature Level</span></span>             | <span data-ttu-id="1c568-373">Dimensión máxima (cualquier eje)</span><span class="sxs-lookup"><span data-stu-id="1c568-373">Maximum Dimension (any axis)</span></span> | <span data-ttu-id="1c568-374">Las dimensiones deben ser potencia de dos</span><span class="sxs-lookup"><span data-stu-id="1c568-374">Dimensions must be power of two</span></span> |
|---------------------------|------------------------------|---------------------------------|
| <span data-ttu-id="1c568-375">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-375">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-376">256</span><span class="sxs-lookup"><span data-stu-id="1c568-376">256</span></span>                          | <span data-ttu-id="1c568-377">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-377">Yes</span></span>                             |
| <span data-ttu-id="1c568-378">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-378">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-379">512</span><span class="sxs-lookup"><span data-stu-id="1c568-379">512</span></span>                          | <span data-ttu-id="1c568-380">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-380">Yes</span></span>                             |
| <span data-ttu-id="1c568-381">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-381">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-382">512</span><span class="sxs-lookup"><span data-stu-id="1c568-382">512</span></span>                          | <span data-ttu-id="1c568-383">Sí</span><span class="sxs-lookup"><span data-stu-id="1c568-383">Yes</span></span>                             |



 

<span data-ttu-id="1c568-384">Si el recurso es \_ un \_ valor predeterminado de uso de D3D11 o el \_ uso de D3D11 es \_ inmutable, BindFlags no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="1c568-384">If resource is D3D11\_USAGE\_DEFAULT or D3D11\_USAGE\_IMMUTABLE, BindFlags cannot be zero.</span></span>

## <a name="id3d11devicecreateunorderedaccessview"></a><span data-ttu-id="1c568-385">ID3D11Device:: CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="1c568-385">ID3D11Device::CreateUnorderedAccessView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-386">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-386">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-387">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="1c568-389">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a><span data-ttu-id="1c568-392">ID3D11Device:: CreateVertexShader</span><span class="sxs-lookup"><span data-stu-id="1c568-392">ID3D11Device::CreateVertexShader</span></span>



| <span data-ttu-id="1c568-393">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-393">Feature Level</span></span>             | <span data-ttu-id="1c568-394">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-394">Behavior Differences</span></span>                                    |
|---------------------------|---------------------------------------------------------|
| <span data-ttu-id="1c568-395">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-395">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="1c568-396">Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-396">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="1c568-397">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="1c568-397">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="1c568-398">Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-398">Must use vs\_4\_0\_level\_9\_1</span></span>                          |
| <span data-ttu-id="1c568-399">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1c568-399">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="1c568-400">Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 3 o vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1c568-400">Must use vs\_4\_0\_level\_9\_3 or vs\_4\_0\_level\_9\_1</span></span> |



 

## <a name="id3d11deviceopensharedresource"></a><span data-ttu-id="1c568-401">ID3D11Device:: OpenSharedResource</span><span class="sxs-lookup"><span data-stu-id="1c568-401">ID3D11Device::OpenSharedResource</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c568-402">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="1c568-402">Feature Level</span></span></th>
<th><span data-ttu-id="1c568-403">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="1c568-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c568-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="1c568-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="1c568-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> con el valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> y la estructura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> para determinar si se puede compartir un formato.</span><span class="sxs-lookup"><span data-stu-id="1c568-405">Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> with the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> value and the <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> structure to determine if a format can be shared.</span></span> <span data-ttu-id="1c568-406">Si el formato se puede compartir, <strong>CheckFeatureSupport</strong> devuelve la marca <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1c568-406">If the format can be shared, <strong>CheckFeatureSupport</strong> returns the <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> flag.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1c568-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca se pueden compartir cuando se usa el nivel de característica 9, incluso si el dispositivo indica compatibilidad con características opcionales para <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c568-407">[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> are never shareable when using feature level 9, even if the device indicates optional feature support for <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>.</span></span> <span data-ttu-id="1c568-408">Al intentar crear recursos compartidos con formatos de DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> , siempre se producirá un error a menos que el nivel de característica sea 10_0 o superior.</span><span class="sxs-lookup"><span data-stu-id="1c568-408">Attempting to create shared resources with DXGI formats <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> and <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> will always fail unless the feature level is 10_0 or higher.</span></span>
</blockquote>
<br/> <span data-ttu-id="1c568-409">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="1c568-409">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c568-410">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="1c568-410">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1c568-411">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="1c568-411">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1c568-412">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c568-412">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c568-413">Referencia de 10Level9</span><span class="sxs-lookup"><span data-stu-id="1c568-413">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

