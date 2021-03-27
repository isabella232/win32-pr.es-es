---
title: Métodos 10Level9 ID3D11DeviceContext
description: En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075258"
---
# <a name="10level9-id3d11devicecontext-methods"></a><span data-ttu-id="e22e5-103">Métodos 10Level9 ID3D11DeviceContext</span><span class="sxs-lookup"><span data-stu-id="e22e5-103">10Level9 ID3D11DeviceContext Methods</span></span>

<span data-ttu-id="e22e5-104">En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="e22e5-104">This section lists the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span>

-   [<span data-ttu-id="e22e5-105">ID3D11DeviceContext:: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="e22e5-105">ID3D11DeviceContext::CopySubresourceRegion</span></span>](#id3d11devicecontextcopysubresourceregion)
-   [<span data-ttu-id="e22e5-106">ID3D11DeviceContext:: CopyResource</span><span class="sxs-lookup"><span data-stu-id="e22e5-106">ID3D11DeviceContext::CopyResource</span></span>](#id3d11devicecontextcopyresource)
-   [<span data-ttu-id="e22e5-107">ID3D11DeviceContext:: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="e22e5-107">ID3D11DeviceContext::CopyStructureCount</span></span>](#id3d11devicecontextcopystructurecount)
-   [<span data-ttu-id="e22e5-108">ID3D11DeviceContext:: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="e22e5-108">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [<span data-ttu-id="e22e5-109">ID3D11DeviceContext:: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="e22e5-109">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>](#id3d11devicecontextclearunorderedaccessviewuint)
-   [<span data-ttu-id="e22e5-110">ID3D11DeviceContext:: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="e22e5-110">ID3D11DeviceContext::ClearRenderTargetView</span></span>](#id3d11devicecontextclearrendertargetview)
-   [<span data-ttu-id="e22e5-111">ID3D11DeviceContext:: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-111">ID3D11DeviceContext::CSSetConstantBuffers</span></span>](#id3d11devicecontextcssetconstantbuffers)
-   [<span data-ttu-id="e22e5-112">ID3D11DeviceContext:: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-112">ID3D11DeviceContext::CSSetSamplers</span></span>](#id3d11devicecontextcssetsamplers)
-   [<span data-ttu-id="e22e5-113">ID3D11DeviceContext:: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-113">ID3D11DeviceContext::CSSetShader</span></span>](#id3d11devicecontextcssetshader)
-   [<span data-ttu-id="e22e5-114">ID3D11DeviceContext:: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-114">ID3D11DeviceContext::CSSetShaderResources</span></span>](#id3d11devicecontextcssetshaderresources)
-   [<span data-ttu-id="e22e5-115">ID3D11DeviceContext:: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="e22e5-115">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>](#id3d11devicecontextcssetunorderedaccessviews)
-   [<span data-ttu-id="e22e5-116">ID3D11DeviceContext::D ispatch</span><span class="sxs-lookup"><span data-stu-id="e22e5-116">ID3D11DeviceContext::Dispatch</span></span>](#id3d11devicecontextdispatch)
-   [<span data-ttu-id="e22e5-117">ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-117">ID3D11DeviceContext::DispatchIndirect</span></span>](#id3d11devicecontextdispatchindirect)
-   [<span data-ttu-id="e22e5-118">ID3D11DeviceContext::D RAW</span><span class="sxs-lookup"><span data-stu-id="e22e5-118">ID3D11DeviceContext::Draw</span></span>](#id3d11devicecontextdraw)
-   [<span data-ttu-id="e22e5-119">ID3D11DeviceContext::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="e22e5-119">ID3D11DeviceContext::DrawAuto</span></span>](#id3d11devicecontextdrawauto)
-   [<span data-ttu-id="e22e5-120">ID3D11DeviceContext::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="e22e5-120">ID3D11DeviceContext::DrawIndexed</span></span>](#id3d11devicecontextdrawindexed)
-   [<span data-ttu-id="e22e5-121">ID3D11DeviceContext::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="e22e5-121">ID3D11DeviceContext::DrawIndexedInstanced</span></span>](#id3d11devicecontextdrawindexedinstanced)
-   [<span data-ttu-id="e22e5-122">ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-122">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>](#id3d11devicecontextdrawindexedinstancedindirect)
-   [<span data-ttu-id="e22e5-123">ID3D11DeviceContext::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="e22e5-123">ID3D11DeviceContext::DrawInstanced</span></span>](#id3d11devicecontextdrawinstanced)
-   [<span data-ttu-id="e22e5-124">ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-124">ID3D11DeviceContext::DrawInstancedIndirect</span></span>](#id3d11devicecontextdrawinstancedindirect)
-   [<span data-ttu-id="e22e5-125">ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-125">ID3D11DeviceContext::DSSetConstantBuffers</span></span>](#id3d11devicecontextdssetconstantbuffers)
-   [<span data-ttu-id="e22e5-126">ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-126">ID3D11DeviceContext::DSSetSamplers</span></span>](#id3d11devicecontextdssetsamplers)
-   [<span data-ttu-id="e22e5-127">ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-127">ID3D11DeviceContext::DSSetShader</span></span>](#id3d11devicecontextdssetshader)
-   [<span data-ttu-id="e22e5-128">ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-128">ID3D11DeviceContext::DSSetShaderResources</span></span>](#id3d11devicecontextdssetshaderresources)
-   [<span data-ttu-id="e22e5-129">ID3D11DeviceContext:: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-129">ID3D11DeviceContext::GSSetConstantBuffers</span></span>](#id3d11devicecontextgssetconstantbuffers)
-   [<span data-ttu-id="e22e5-130">ID3D11DeviceContext:: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-130">ID3D11DeviceContext::GSSetSamplers</span></span>](#id3d11devicecontextgssetsamplers)
-   [<span data-ttu-id="e22e5-131">ID3D11DeviceContext:: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-131">ID3D11DeviceContext::GSSetShader</span></span>](#id3d11devicecontextgssetshader)
-   [<span data-ttu-id="e22e5-132">ID3D11DeviceContext:: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-132">ID3D11DeviceContext::GSSetShaderResources</span></span>](#id3d11devicecontextgssetshaderresources)
-   [<span data-ttu-id="e22e5-133">ID3D11DeviceContext:: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-133">ID3D11DeviceContext::HSSetConstantBuffers</span></span>](#id3d11devicecontexthssetconstantbuffers)
-   [<span data-ttu-id="e22e5-134">ID3D11DeviceContext:: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-134">ID3D11DeviceContext::HSSetSamplers</span></span>](#id3d11devicecontexthssetsamplers)
-   [<span data-ttu-id="e22e5-135">ID3D11DeviceContext:: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-135">ID3D11DeviceContext::HSSetShader</span></span>](#id3d11devicecontexthssetshader)
-   [<span data-ttu-id="e22e5-136">ID3D11DeviceContext:: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-136">ID3D11DeviceContext::HSSetShaderResources</span></span>](#id3d11devicecontexthssetshaderresources)
-   [<span data-ttu-id="e22e5-137">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="e22e5-137">ID3D11DeviceContext::IASetIndexBuffer</span></span>](#id3d11devicecontextiasetindexbuffer)
-   [<span data-ttu-id="e22e5-138">ID3D11DeviceContext:: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="e22e5-138">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>](#id3d11devicecontextiasetprimitivetopology)
-   [<span data-ttu-id="e22e5-139">ID3D11DeviceContext:: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="e22e5-139">ID3D11DeviceContext::OMSetBlendState</span></span>](#id3d11devicecontextomsetblendstate)
-   [<span data-ttu-id="e22e5-140">ID3D11DeviceContext:: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="e22e5-140">ID3D11DeviceContext::OMSetRenderTargets</span></span>](#id3d11devicecontextomsetrendertargets)
-   [<span data-ttu-id="e22e5-141">ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="e22e5-141">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [<span data-ttu-id="e22e5-142">ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-142">ID3D11DeviceContext::PSSetConstantBuffers</span></span>](#id3d11devicecontextpssetconstantbuffers)
-   [<span data-ttu-id="e22e5-143">ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-143">ID3D11DeviceContext::PSSetSamplers</span></span>](#id3d11devicecontextpssetsamplers)
-   [<span data-ttu-id="e22e5-144">ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-144">ID3D11DeviceContext::PSSetShader</span></span>](#id3d11devicecontextpssetshader)
-   [<span data-ttu-id="e22e5-145">ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-145">ID3D11DeviceContext::PSSetShaderResources</span></span>](#id3d11devicecontextpssetshaderresources)
-   [<span data-ttu-id="e22e5-146">ID3D11DeviceContext:: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="e22e5-146">ID3D11DeviceContext::RSSetScissorRects</span></span>](#id3d11devicecontextrssetscissorrects)
-   [<span data-ttu-id="e22e5-147">ID3D11DeviceContext:: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="e22e5-147">ID3D11DeviceContext::RSSetViewports</span></span>](#id3d11devicecontextrssetviewports)
-   [<span data-ttu-id="e22e5-148">ID3D11DeviceContext:: SetPredication</span><span class="sxs-lookup"><span data-stu-id="e22e5-148">ID3D11DeviceContext::SetPredication</span></span>](#id3d11devicecontextsetpredication)
-   [<span data-ttu-id="e22e5-149">ID3D11DeviceContext:: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="e22e5-149">ID3D11DeviceContext::SOSetTargets</span></span>](#id3d11devicecontextsosettargets)
-   [<span data-ttu-id="e22e5-150">ID3D11DeviceContext:: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-150">ID3D11DeviceContext::VSSetConstantBuffers</span></span>](#id3d11devicecontextvssetconstantbuffers)
-   [<span data-ttu-id="e22e5-151">ID3D11DeviceContext:: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-151">ID3D11DeviceContext::VSSetSamplers</span></span>](#id3d11devicecontextvssetsamplers)
-   [<span data-ttu-id="e22e5-152">ID3D11DeviceContext:: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-152">ID3D11DeviceContext::VSSetShader</span></span>](#id3d11devicecontextvssetshader)
-   [<span data-ttu-id="e22e5-153">ID3D11DeviceContext:: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-153">ID3D11DeviceContext::VSSetShaderResources</span></span>](#id3d11devicecontextvssetshaderresources)
-   [<span data-ttu-id="e22e5-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e22e5-154">Related topics</span></span>](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a><span data-ttu-id="e22e5-155">ID3D11DeviceContext:: CopySubresourceRegion</span><span class="sxs-lookup"><span data-stu-id="e22e5-155">ID3D11DeviceContext::CopySubresourceRegion</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-156">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-156">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-157">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-157">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-158">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-158">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="e22e5-159">Solo se pueden copiar Texture2D y búferes en la memoria accesible desde la GPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-159">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-160">Texture3D no se puede copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-160">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-161">Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-161">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-162">No se pueden copiar texturas de volumen de mipmapped.</span><span class="sxs-lookup"><span data-stu-id="e22e5-162">You can't copy mipmapped volume textures.</span></span> <br/> <span data-ttu-id="e22e5-163">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-163">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-164">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-164">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-165">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-165">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a><span data-ttu-id="e22e5-166">ID3D11DeviceContext:: CopyResource</span><span class="sxs-lookup"><span data-stu-id="e22e5-166">ID3D11DeviceContext::CopyResource</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-167">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-167">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-168">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-168">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-169">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-169">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"> <span data-ttu-id="e22e5-170">Solo se pueden copiar Texture2D y búferes en la memoria accesible desde la GPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-170">Only Texture2D and buffers may be copied within GPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-171">Texture3D no se puede copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-171">Texture3D cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-172">Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.</span><span class="sxs-lookup"><span data-stu-id="e22e5-172">Any resource that has only D3D10_BIND_SHADER_RESOURCE cannot be copied from GPU-accessible memory to CPU-accessible memory.</span></span><br/> <span data-ttu-id="e22e5-173">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-173">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-174">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-174">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-175">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-175">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a><span data-ttu-id="e22e5-176">ID3D11DeviceContext:: CopyStructureCount</span><span class="sxs-lookup"><span data-stu-id="e22e5-176">ID3D11DeviceContext::CopyStructureCount</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-177">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-177">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-178">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-178">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-179">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-179">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-180">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-180">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-181">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-181">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-182">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-182">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a><span data-ttu-id="e22e5-183">ID3D11DeviceContext:: ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="e22e5-183">ID3D11DeviceContext::ClearUnorderedAccessViewFloat</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-184">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-184">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-185">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-185">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-186">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-186">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-187">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-187">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-188">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-188">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-189">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-189">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a><span data-ttu-id="e22e5-190">ID3D11DeviceContext:: ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="e22e5-190">ID3D11DeviceContext::ClearUnorderedAccessViewUint</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-191">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-191">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-192">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-192">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-193">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-193">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-194">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-194">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-195">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-195">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-196">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-196">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a><span data-ttu-id="e22e5-197">ID3D11DeviceContext:: ClearRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="e22e5-197">ID3D11DeviceContext::ClearRenderTargetView</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-198">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-198">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-199">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-199">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-200">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-200">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-201">Solo se borrará el primer segmento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e22e5-201">Only the first array slice will be cleared.</span></span> <span data-ttu-id="e22e5-202">Las aplicaciones deben crear una vista de destino de representación para cada superficie o segmento de matriz y, a continuación, borrar cada vista individualmente. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-202">Applications should create a render target view for each face or array slice, then clear each view individually.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-203">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-203">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-204">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-204">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a><span data-ttu-id="e22e5-205">ID3D11DeviceContext:: CSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-205">ID3D11DeviceContext::CSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-206">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-206">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-207">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-207">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-208">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-208">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-209">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-209">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-210">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-210">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-211">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-211">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a><span data-ttu-id="e22e5-212">ID3D11DeviceContext:: CSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-212">ID3D11DeviceContext::CSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-213">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-213">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-214">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-214">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-215">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-215">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-216">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-216">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-217">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-217">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-218">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-218">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a><span data-ttu-id="e22e5-219">ID3D11DeviceContext:: CSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-219">ID3D11DeviceContext::CSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-220">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-220">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-221">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-221">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-222">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-222">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-223">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-223">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-224">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-224">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-225">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-225">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a><span data-ttu-id="e22e5-226">ID3D11DeviceContext:: CSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-226">ID3D11DeviceContext::CSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-227">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-227">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-228">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-228">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-229">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-229">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-230">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-230">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-231">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-231">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-232">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-232">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a><span data-ttu-id="e22e5-233">ID3D11DeviceContext:: CSSetUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="e22e5-233">ID3D11DeviceContext::CSSetUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-234">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-234">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-235">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-235">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-236">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-236">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-237">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-237">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-238">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-238">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-239">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-239">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a><span data-ttu-id="e22e5-240">ID3D11DeviceContext::D ispatch</span><span class="sxs-lookup"><span data-stu-id="e22e5-240">ID3D11DeviceContext::Dispatch</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-241">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-241">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-242">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-242">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-243">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-243">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-244">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-244">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-245">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-245">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-246">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-246">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a><span data-ttu-id="e22e5-247">ID3D11DeviceContext::D ispatchIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-247">ID3D11DeviceContext::DispatchIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-248">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-248">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-249">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-249">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-250">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-250">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-251">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-251">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-252">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-252">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-253">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-253">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a><span data-ttu-id="e22e5-254">ID3D11DeviceContext::D RAW</span><span class="sxs-lookup"><span data-stu-id="e22e5-254">ID3D11DeviceContext::Draw</span></span>



| <span data-ttu-id="e22e5-255">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-255">Feature Level</span></span>             | <span data-ttu-id="e22e5-256">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-256">Behavior Differences</span></span>                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22e5-257">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e22e5-257">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="e22e5-258">El número de primitivas no puede superar 65535.</span><span class="sxs-lookup"><span data-stu-id="e22e5-258">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="e22e5-259">Las texturas no se pueden repetir más de 128 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-259">Textures cannot repeat over one primitive more than 128 times.</span></span><br/>    |
| <span data-ttu-id="e22e5-260">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="e22e5-260">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="e22e5-261">El número de primitivas no puede superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-261">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-262">Las texturas no se pueden repetir más de 2048 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-262">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> |
| <span data-ttu-id="e22e5-263">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e22e5-263">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="e22e5-264">El número de primitivas no puede superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-264">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-265">Las texturas no se pueden repetir más de 8192 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-265">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawauto"></a><span data-ttu-id="e22e5-266">ID3D11DeviceContext::D rawAuto</span><span class="sxs-lookup"><span data-stu-id="e22e5-266">ID3D11DeviceContext::DrawAuto</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-267">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-267">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-268">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-268">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-269">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-269">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-270">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-270">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-271">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-271">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-272">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-272">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a><span data-ttu-id="e22e5-273">ID3D11DeviceContext::D rawIndexed</span><span class="sxs-lookup"><span data-stu-id="e22e5-273">ID3D11DeviceContext::DrawIndexed</span></span>



| <span data-ttu-id="e22e5-274">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-274">Feature Level</span></span>             | <span data-ttu-id="e22e5-275">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-275">Behavior Differences</span></span>                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e22e5-276">Nivel de característica de D3D \_ \_ \_ 9 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e22e5-276">D3D\_FEATURE\_LEVEL\_9\_1</span></span> | <span data-ttu-id="e22e5-277">El número de primitivas no puede superar 65535.</span><span class="sxs-lookup"><span data-stu-id="e22e5-277">Number of primitives may not exceed 65535.</span></span><br/> <span data-ttu-id="e22e5-278">Las texturas no se pueden repetir más de 128 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-278">Textures cannot repeat over one primitive more than 128 times.</span></span><br/> <span data-ttu-id="e22e5-279">Los valores de índice no pueden superar 65534.</span><span class="sxs-lookup"><span data-stu-id="e22e5-279">Index values cannot exceed 65534.</span></span><br/> <span data-ttu-id="e22e5-280">No se admiten las listas de puntos indexados.</span><span class="sxs-lookup"><span data-stu-id="e22e5-280">Indexed point lists not supported.</span></span><br/>      |
| <span data-ttu-id="e22e5-281">Nivel de característica de D3D \_ \_ \_ 9 \_ 2</span><span class="sxs-lookup"><span data-stu-id="e22e5-281">D3D\_FEATURE\_LEVEL\_9\_2</span></span> | <span data-ttu-id="e22e5-282">El número de primitivas no puede superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-282">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-283">Las texturas no se pueden repetir más de 2048 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-283">Textures cannot repeat over one primitive more than 2048 times.</span></span><br/> <span data-ttu-id="e22e5-284">Los valores de índice no pueden superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-284">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-285">No se admiten las listas de puntos indexados.</span><span class="sxs-lookup"><span data-stu-id="e22e5-285">Indexed point lists not supported.</span></span><br/> |
| <span data-ttu-id="e22e5-286">Nivel de característica de D3D \_ \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e22e5-286">D3D\_FEATURE\_LEVEL\_9\_3</span></span> | <span data-ttu-id="e22e5-287">El número de primitivas no puede superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-287">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-288">Las texturas no se pueden repetir más de 8192 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-288">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="e22e5-289">Los valores de índice no pueden superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-289">Index values cannot exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-290">No se admiten las listas de puntos indexados.</span><span class="sxs-lookup"><span data-stu-id="e22e5-290">Indexed point lists not supported.</span></span><br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a><span data-ttu-id="e22e5-291">ID3D11DeviceContext::D rawIndexedInstanced</span><span class="sxs-lookup"><span data-stu-id="e22e5-291">ID3D11DeviceContext::DrawIndexedInstanced</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-292">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-292">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-293">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-293">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-294">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-294">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="e22e5-295">No se admite $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-295">Not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-296">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-296">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-297">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-297">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="e22e5-298">El número de primitivas no puede superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-298">Number of primitives may not exceed 1048575.</span></span><br/> <span data-ttu-id="e22e5-299">Las texturas no se pueden repetir más de 8192 veces en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="e22e5-299">Textures cannot repeat over one primitive more than 8192 times.</span></span><br/> <span data-ttu-id="e22e5-300">Los valores de índice no pueden superar 1048575.</span><span class="sxs-lookup"><span data-stu-id="e22e5-300">Index values cannot exceed 1048575.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e22e5-301">Cuando se llama al método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un sombreador de vértices que está enlazado a la canalización y que no importa ningún dato por instancia, es posible que algún hardware gráfico de Direct3D 9 no dibuje nada.</span><span class="sxs-lookup"><span data-stu-id="e22e5-301">When you call the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> method with a vertex shader that is bound to the pipeline and that doesn't import any per-instance data, some Direct3D 9 graphics hardware might not draw anything.</span></span> <span data-ttu-id="e22e5-302">En concreto, si el sombreador de vértices no usa ningún dato por instancia, llamar a <strong>DrawIndexedInstanced</strong> con 1 instancia no es equivalente a llamar a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e22e5-302">In particular, if the vertex shader does not use any per-instance data, calling <strong>DrawIndexedInstanced</strong> with 1 instance is not equivalent to calling <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a><span data-ttu-id="e22e5-303">ID3D11DeviceContext::D rawIndexedInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-303">ID3D11DeviceContext::DrawIndexedInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-304">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-304">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-305">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-305">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-306">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-306">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-307">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-307">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-308">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-308">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-309">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-309">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-310">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-310">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-311">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-311">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a><span data-ttu-id="e22e5-312">ID3D11DeviceContext::D rawInstanced</span><span class="sxs-lookup"><span data-stu-id="e22e5-312">ID3D11DeviceContext::DrawInstanced</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-313">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-313">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-314">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-314">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-315">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-315">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-316">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-316">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-317">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-317">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-318">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-318">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a><span data-ttu-id="e22e5-319">ID3D11DeviceContext::D rawInstancedIndirect</span><span class="sxs-lookup"><span data-stu-id="e22e5-319">ID3D11DeviceContext::DrawInstancedIndirect</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-320">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-320">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-321">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-321">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-322">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-322">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-323">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-323">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-324">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-324">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-325">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-325">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-326">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-326">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-327">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-327">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a><span data-ttu-id="e22e5-328">ID3D11DeviceContext::D SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-328">ID3D11DeviceContext::DSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-329">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-329">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-330">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-330">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-331">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-331">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-332">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-332">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-333">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-333">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-334">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-334">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-335">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-335">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-336">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-336">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a><span data-ttu-id="e22e5-337">ID3D11DeviceContext::D SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-337">ID3D11DeviceContext::DSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-338">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-338">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-339">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-339">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-340">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-340">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-341">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-341">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-342">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-342">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-343">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-343">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-344">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-344">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-345">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-345">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a><span data-ttu-id="e22e5-346">ID3D11DeviceContext::D SSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-346">ID3D11DeviceContext::DSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-347">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-347">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-348">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-348">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-349">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-349">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-350">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-350">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-351">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-351">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-352">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-352">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-353">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-353">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-354">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-354">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a><span data-ttu-id="e22e5-355">ID3D11DeviceContext::D SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-355">ID3D11DeviceContext::DSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-356">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-356">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-357">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-357">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-358">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-358">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-359">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-359">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-360">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-360">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-361">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-361">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-362">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-362">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-363">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-363">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a><span data-ttu-id="e22e5-364">ID3D11DeviceContext:: GSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-364">ID3D11DeviceContext::GSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-365">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-365">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-366">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-366">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-367">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-367">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-368">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-368">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-369">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-369">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-370">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-370">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a><span data-ttu-id="e22e5-371">ID3D11DeviceContext:: GSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-371">ID3D11DeviceContext::GSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-372">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-372">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-373">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-373">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-374">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-374">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-375">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-375">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-376">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-376">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-377">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-377">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a><span data-ttu-id="e22e5-378">ID3D11DeviceContext:: GSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-378">ID3D11DeviceContext::GSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-379">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-379">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-380">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-380">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-381">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-381">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-382">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-382">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-383">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-383">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-384">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-384">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a><span data-ttu-id="e22e5-385">ID3D11DeviceContext:: GSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-385">ID3D11DeviceContext::GSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-386">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-386">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-387">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-387">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-388">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-388">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-389">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-389">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-390">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-390">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-391">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-391">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a><span data-ttu-id="e22e5-392">ID3D11DeviceContext:: HSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-392">ID3D11DeviceContext::HSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-393">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-393">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-394">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-394">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-395">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-395">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-396">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-396">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-397">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-397">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-398">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-398">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-399">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-399">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-400">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-400">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a><span data-ttu-id="e22e5-401">ID3D11DeviceContext:: HSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-401">ID3D11DeviceContext::HSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-402">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-402">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-403">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-403">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-404">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-404">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-405">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-405">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-406">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-406">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-407">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-407">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-408">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-408">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-409">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-409">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a><span data-ttu-id="e22e5-410">ID3D11DeviceContext:: HSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-410">ID3D11DeviceContext::HSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-411">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-411">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-412">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-412">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-413">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-413">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-414">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-414">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-415">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-415">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-416">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-416">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-417">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-417">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-418">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-418">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a><span data-ttu-id="e22e5-419">ID3D11DeviceContext:: HSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-419">ID3D11DeviceContext::HSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-420">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-420">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-421">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-421">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-422">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-422">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="5"><span data-ttu-id="e22e5-423">No se admite en ningún nivel de características 9. \* o 10. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-423">Not supported on any 9.\* or 10.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-424">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-424">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-425">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-425">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-426">D3D_FEATURE_LEVEL_10_0</span><span class="sxs-lookup"><span data-stu-id="e22e5-426">D3D_FEATURE_LEVEL_10_0</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-427">D3D_FEATURE_LEVEL_10_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-427">D3D_FEATURE_LEVEL_10_1</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a><span data-ttu-id="e22e5-428">ID3D11DeviceContext::IASetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="e22e5-428">ID3D11DeviceContext::IASetIndexBuffer</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-429">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-429">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-430">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-430">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-431">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-431">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td><span data-ttu-id="e22e5-432">El formato puede ser diferente del especificado al crear el búfer, pero se incurrirá en una traducción costosa.</span><span class="sxs-lookup"><span data-stu-id="e22e5-432">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="e22e5-433">Solo permite búferes de índice con el formato de DXGI_FORMAT_R16_UINT.</span><span class="sxs-lookup"><span data-stu-id="e22e5-433">Only allows index buffers with the DXGI_FORMAT_R16_UINT format.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-434">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-434">D3D_FEATURE_LEVEL_9_2</span></span></td>
<td rowspan="2"> <span data-ttu-id="e22e5-435">El formato puede ser diferente del especificado al crear el búfer, pero se incurrirá en una traducción costosa.</span><span class="sxs-lookup"><span data-stu-id="e22e5-435">Format is allowed to be different from that specified at buffer creation, but an expensive translation will be incurred.</span></span><br/> <span data-ttu-id="e22e5-436">Permite búferes de índice con los formatos DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e22e5-436">Allows index buffers with the DXGI_FORMAT_R16_UINT and DXGI_FORMAT_R32_UINT formats like D3D_FEATURE_LEVEL_10_0 and higher.</span></span> <br/> <span data-ttu-id="e22e5-437">$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-437">${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-438">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-438">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a><span data-ttu-id="e22e5-439">ID3D11DeviceContext:: IASetPrimitiveTopology</span><span class="sxs-lookup"><span data-stu-id="e22e5-439">ID3D11DeviceContext::IASetPrimitiveTopology</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-440">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-440">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-441">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-441">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-442">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-442">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-443">No se admiten topologías primitivas con adyacen $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-443">Primitive topologies with adjacency are not supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-444">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-444">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-445">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-445">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a><span data-ttu-id="e22e5-446">ID3D11DeviceContext:: OMSetBlendState</span><span class="sxs-lookup"><span data-stu-id="e22e5-446">ID3D11DeviceContext::OMSetBlendState</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-447">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-447">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-448">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-448">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-449">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-449">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-450">SampleMask no puede ser cero $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-450">SampleMask cannot be zero${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-451">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-451">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-452">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-452">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a><span data-ttu-id="e22e5-453">ID3D11DeviceContext:: OMSetRenderTargets</span><span class="sxs-lookup"><span data-stu-id="e22e5-453">ID3D11DeviceContext::OMSetRenderTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-454">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-454">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-455">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-455">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-456">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-456">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="e22e5-457">Solo se admite un destino de representación $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-457">Only one render target supported${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-458">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-458">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-459">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-459">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="e22e5-460">Solo se admiten cuatro destinos de representación, y todos los recursos enlazados deben tener la misma profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="e22e5-460">Only four render targets supported, and all bound resources must have same bit depth.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a><span data-ttu-id="e22e5-461">ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews</span><span class="sxs-lookup"><span data-stu-id="e22e5-461">ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-462">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-462">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-463">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-463">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-464">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-464">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-465">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-465">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-466">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-466">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-467">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-467">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a><span data-ttu-id="e22e5-468">ID3D11DeviceContext::P SSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-468">ID3D11DeviceContext::PSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-469">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-469">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-470">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-470">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-471">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-471">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-472">Vea el nivel de característica 10,0, pero el número total de constantes usadas por el sombreador no puede superar los 32 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-472">See feature level 10.0, but total number of constants used by shader cannot exceed 32${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-473">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-473">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-474">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-474">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a><span data-ttu-id="e22e5-475">ID3D11DeviceContext::P SSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-475">ID3D11DeviceContext::PSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-476">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-476">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-477">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-477">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-478">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-478">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-479">No se pueden enlazar más de 16 muestras enlazadas $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-479">No more than 16 samplers can be bound${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-480">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-480">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-481">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-481">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a><span data-ttu-id="e22e5-482">ID3D11DeviceContext::P SSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-482">ID3D11DeviceContext::PSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-483">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-483">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-484">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-484">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-485">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-485">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="e22e5-486">Solo ps_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-486">Only ps_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-487">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-487">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-488">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-488">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="e22e5-489">Solo ps_4_0_level_9_3 o ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-489">Only ps_4_0_level_9_3 or ps_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a><span data-ttu-id="e22e5-490">ID3D11DeviceContext::P SSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-490">ID3D11DeviceContext::PSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-491">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-491">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-492">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-492">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-493">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-493">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-494">No más de 8 recursos de sombreador enlazados simultáneamente $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-494">No more than 8 simultaneously bound shader resources${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-495">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-495">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-496">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-496">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a><span data-ttu-id="e22e5-497">ID3D11DeviceContext:: RSSetScissorRects</span><span class="sxs-lookup"><span data-stu-id="e22e5-497">ID3D11DeviceContext::RSSetScissorRects</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-498">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-498">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-499">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-499">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-500">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-500">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-501">Solo el rectángulo de tijeras de inicial está disponible $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-501">Only the zeroth scissor rect is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-502">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-502">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-503">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-503">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a><span data-ttu-id="e22e5-504">ID3D11DeviceContext:: RSSetViewports</span><span class="sxs-lookup"><span data-stu-id="e22e5-504">ID3D11DeviceContext::RSSetViewports</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-505">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-505">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-506">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-506">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-507">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-507">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-508">Solo está disponible la ventanilla de inicial $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-508">Only the zeroth viewport is available${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-509">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-509">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-510">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-510">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="e22e5-511">Aunque se especifican valores Float para los miembros de la estructura de la [**\_ ventanilla de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) para la matriz *pViewports* en una llamada a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** usa los DWords internamente.</span><span class="sxs-lookup"><span data-stu-id="e22e5-511">Even though you specify float values to the members of the [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) structure for the *pViewports* array in a call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9\_x, **RSSetViewports** uses DWORDs internally.</span></span> <span data-ttu-id="e22e5-512">Debido a este comportamiento, cuando se usa una esquina superior izquierda negativa para la ventanilla, se produce un error en la llamada a **RSSetViewports** para los niveles de características 9 \_ x.</span><span class="sxs-lookup"><span data-stu-id="e22e5-512">Because of this behavior, when you use a negative top left corner for the viewport, the call to **RSSetViewports** for feature levels 9\_x fails.</span></span> <span data-ttu-id="e22e5-513">Este error se produce porque **RSSetViewports** para 9 \_ x convierte los valores de punto flotante en enteros sin signo sin validación, lo que da como resultado un desbordamiento de enteros.</span><span class="sxs-lookup"><span data-stu-id="e22e5-513">This failure occurs because **RSSetViewports** for 9\_x casts the floating point values into unsigned integers without validation, which results in integer overflow.</span></span>

<span data-ttu-id="e22e5-514">La llamada a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [los niveles de característica](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x y 11 \_ x funciona como se espera, incluso cuando se usa una esquina superior izquierda negativa para la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="e22e5-514">The call to [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) for [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10\_x and 11\_x works as you expect even when you use a negative top left corner for the viewport.</span></span>

## <a name="id3d11devicecontextsetpredication"></a><span data-ttu-id="e22e5-515">ID3D11DeviceContext:: SetPredication</span><span class="sxs-lookup"><span data-stu-id="e22e5-515">ID3D11DeviceContext::SetPredication</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-516">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-516">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-517">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-517">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-518">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-518">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-519">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-519">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-520">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-520">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-521">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-521">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a><span data-ttu-id="e22e5-522">ID3D11DeviceContext:: SOSetTargets</span><span class="sxs-lookup"><span data-stu-id="e22e5-522">ID3D11DeviceContext::SOSetTargets</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-523">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-523">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-524">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-524">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-525">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-525">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-526">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-526">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-527">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-527">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-528">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-528">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a><span data-ttu-id="e22e5-529">ID3D11DeviceContext:: VSSetConstantBuffers</span><span class="sxs-lookup"><span data-stu-id="e22e5-529">ID3D11DeviceContext::VSSetConstantBuffers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-530">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-530">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-531">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-531">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-532">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-532">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-533">Vea el nivel de característica 10,0, pero el número total de constantes usadas por el sombreador no puede superar los 255 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-533">See feature level 10.0, but total number of constants used by shader cannot exceed 255${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-534">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-534">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-535">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-535">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a><span data-ttu-id="e22e5-536">ID3D11DeviceContext:: VSSetSamplers</span><span class="sxs-lookup"><span data-stu-id="e22e5-536">ID3D11DeviceContext::VSSetSamplers</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-537">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-537">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-538">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-538">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-539">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-539">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-540">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-540">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-541">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-541">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-542">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-542">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a><span data-ttu-id="e22e5-543">ID3D11DeviceContext:: VSSetShader</span><span class="sxs-lookup"><span data-stu-id="e22e5-543">ID3D11DeviceContext::VSSetShader</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-544">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-544">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-545">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-545">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-546">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-546">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="2"><span data-ttu-id="e22e5-547">Solo vs_4_0_level_9_1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-547">Only vs_4_0_level_9_1${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-548">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-548">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-549">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-549">D3D_FEATURE_LEVEL_9_3</span></span></td>
<td><span data-ttu-id="e22e5-550">Solo vs_4_0_level_9_3 o vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-550">Only vs_4_0_level_9_3 or vs_4_0_level_9_1</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a><span data-ttu-id="e22e5-551">ID3D11DeviceContext:: VSSetShaderResources</span><span class="sxs-lookup"><span data-stu-id="e22e5-551">ID3D11DeviceContext::VSSetShaderResources</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e22e5-552">Nivel de características</span><span class="sxs-lookup"><span data-stu-id="e22e5-552">Feature Level</span></span></th>
<th><span data-ttu-id="e22e5-553">Diferencias de comportamiento</span><span class="sxs-lookup"><span data-stu-id="e22e5-553">Behavior Differences</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e22e5-554">D3D_FEATURE_LEVEL_9_1</span><span class="sxs-lookup"><span data-stu-id="e22e5-554">D3D_FEATURE_LEVEL_9_1</span></span></td>
<td rowspan="3"><span data-ttu-id="e22e5-555">No se admite en cualquier nivel de características 9. \*. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="e22e5-555">Not supported on any 9.\* feature level.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e22e5-556">D3D_FEATURE_LEVEL_9_2</span><span class="sxs-lookup"><span data-stu-id="e22e5-556">D3D_FEATURE_LEVEL_9_2</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="e22e5-557">D3D_FEATURE_LEVEL_9_3</span><span class="sxs-lookup"><span data-stu-id="e22e5-557">D3D_FEATURE_LEVEL_9_3</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e22e5-558">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e22e5-558">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e22e5-559">Referencia de 10Level9</span><span class="sxs-lookup"><span data-stu-id="e22e5-559">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





