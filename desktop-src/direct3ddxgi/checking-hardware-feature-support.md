---
description: En esta sección se explica cómo comprobar la compatibilidad con el formato de hardware de nivel de característica de Direct3D mediante llamadas API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 'Comprobando la compatibilidad con las características de hardware '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b14f0de50c4236c4fce46ceda1896ee32721c3bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997883"
---
# <a name="checking-hardware-feature-support"></a><span data-ttu-id="aecf7-103">Comprobando la compatibilidad con las características de hardware </span><span class="sxs-lookup"><span data-stu-id="aecf7-103">Checking Hardware Feature Support</span></span>

<span data-ttu-id="aecf7-104">En esta sección se explica cómo comprobar la compatibilidad con el formato de hardware de nivel de característica de Direct3D mediante llamadas API.</span><span class="sxs-lookup"><span data-stu-id="aecf7-104">This section covers how to check on Format Support for Direct3D Feature Level Hardware using API calls.</span></span>

<span data-ttu-id="aecf7-105">En el caso de D3D11, use [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) para comprobar mediante programación la información de las secciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="aecf7-105">For D3D11, use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) to programmatically verify the info in the previous sections.</span></span> <span data-ttu-id="aecf7-106">Para D3D12, use [**ID3D12:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="aecf7-106">For D3D12 use [**ID3D12::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aecf7-107">Destino de formato</span><span class="sxs-lookup"><span data-stu-id="aecf7-107">Format target</span></span></th>
<th><span data-ttu-id="aecf7-108">D3D12</span><span class="sxs-lookup"><span data-stu-id="aecf7-108">D3D12</span></span></th>
<th><span data-ttu-id="aecf7-109">D3D11</span><span class="sxs-lookup"><span data-stu-id="aecf7-109">D3D11</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aecf7-110">Buffer</span><span class="sxs-lookup"><span data-stu-id="aecf7-110">Buffer</span></span></td>
<td><span data-ttu-id="aecf7-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-113">Búfer de vértice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="aecf7-113">Input Assembler Vertex Buffer</span></span></td>
<td><span data-ttu-id="aecf7-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-116">Búfer de índice del ensamblador de entrada</span><span class="sxs-lookup"><span data-stu-id="aecf7-116">Input Assembler Index Buffer</span></span></td>
<td><span data-ttu-id="aecf7-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-119">Búfer de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="aecf7-119">Stream Output Buffer</span></span></td>
<td><span data-ttu-id="aecf7-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-122">Texture1D</span><span class="sxs-lookup"><span data-stu-id="aecf7-122">Texture1D</span></span></td>
<td><span data-ttu-id="aecf7-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="aecf7-125">Texture2D</span></span></td>
<td><span data-ttu-id="aecf7-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-128">Texture3D</span><span class="sxs-lookup"><span data-stu-id="aecf7-128">Texture3D</span></span></td>
<td><span data-ttu-id="aecf7-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="aecf7-131">TextureCube</span></span></td>
<td><span data-ttu-id="aecf7-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-134">Sombreador LD</span><span class="sxs-lookup"><span data-stu-id="aecf7-134">Shader ld</span></span></td>
<td><span data-ttu-id="aecf7-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-137">Ejemplo de sombreador (cualquier filtro)</span><span class="sxs-lookup"><span data-stu-id="aecf7-137">Shader sample (any filter)</span></span></td>
<td><span data-ttu-id="aecf7-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-140">Sample_c del sombreador (filtro de comparación)</span><span class="sxs-lookup"><span data-stu-id="aecf7-140">Shader sample_c (comparison filter)</span></span></td>
<td><span data-ttu-id="aecf7-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-143">Ejemplo de sombreador (1_bit_filter mono)</span><span class="sxs-lookup"><span data-stu-id="aecf7-143">Shader sample (mono 1_bit_filter)</span></span></td>
<td><span data-ttu-id="aecf7-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-146">Sombreador gather4</span><span class="sxs-lookup"><span data-stu-id="aecf7-146">Shader gather4</span></span></td>
<td><span data-ttu-id="aecf7-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-149">Gather4_c del sombreador</span><span class="sxs-lookup"><span data-stu-id="aecf7-149">Shader gather4_c</span></span></td>
<td><span data-ttu-id="aecf7-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-152">Mapa</span><span class="sxs-lookup"><span data-stu-id="aecf7-152">Mipmap</span></span></td>
<td><span data-ttu-id="aecf7-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-155">Generación automática de mipmap</span><span class="sxs-lookup"><span data-stu-id="aecf7-155">Mipmap Auto-Generation</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="aecf7-156">D3D12 ya no tiene una funcionalidad de generación de mipmap dedicada.</span><span class="sxs-lookup"><span data-stu-id="aecf7-156">D3D12 no longer has a dedicated mipmap generation functionality.</span></span> <span data-ttu-id="aecf7-157">Las aplicaciones deben implementarlo por su cuenta mediante sombreadores.</span><span class="sxs-lookup"><span data-stu-id="aecf7-157">Applications must implement it on their own using shaders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="aecf7-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="aecf7-159">RenderTarget</span></span></td>
<td><span data-ttu-id="aecf7-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-162">RenderTarget combinable</span><span class="sxs-lookup"><span data-stu-id="aecf7-162">Blendable RenderTarget</span></span></td>
<td><span data-ttu-id="aecf7-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-165">Operación de lógica de fusión de salida</span><span class="sxs-lookup"><span data-stu-id="aecf7-165">Output Merger Logic Op</span></span></td>
<td><span data-ttu-id="aecf7-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span><span class="sxs-lookup"><span data-stu-id="aecf7-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span></span></td>
<td><span data-ttu-id="aecf7-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-168">Destino de estarcido o profundidad</span><span class="sxs-lookup"><span data-stu-id="aecf7-168">Depth/Stencil Target</span></span></td>
<td><span data-ttu-id="aecf7-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-171">UAV y SRV sin formato</span><span class="sxs-lookup"><span data-stu-id="aecf7-171">Raw UAV and SRV</span></span></td>


</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-172">UAV estructurado y SRV</span><span class="sxs-lookup"><span data-stu-id="aecf7-172">Structured UAV and SRV</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-173">UAV con tipo</span><span class="sxs-lookup"><span data-stu-id="aecf7-173">Typed UAV</span></span></td>
<td><span data-ttu-id="aecf7-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-176">UAV almacén de tipos</span><span class="sxs-lookup"><span data-stu-id="aecf7-176">UAV Typed Store</span></span></td>
<td><span data-ttu-id="aecf7-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-179">Carga con tipo UAV</span><span class="sxs-lookup"><span data-stu-id="aecf7-179">UAV Typed Load</span></span></td>
<td><span data-ttu-id="aecf7-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-182">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="aecf7-182">UAV Atomic Add</span></span></td>
<td><span data-ttu-id="aecf7-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-185">Operaciones bit a bit atómicas UAV</span><span class="sxs-lookup"><span data-stu-id="aecf7-185">UAV Atomic Bitwise Ops</span></span></td>
<td><span data-ttu-id="aecf7-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="aecf7-188">UAV Atomic Cmp&Store/ Cmp&Exch</span></span></td>
<td><span data-ttu-id="aecf7-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-191">Intercambio atómico UAV</span><span class="sxs-lookup"><span data-stu-id="aecf7-191">UAV Atomic Exchange</span></span></td>
<td><span data-ttu-id="aecf7-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-194">UAV Atomic con signo mín./máx.</span><span class="sxs-lookup"><span data-stu-id="aecf7-194">UAV Atomic Signed Min/Max</span></span></td>
<td><span data-ttu-id="aecf7-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-197">UAV Atomic sin signo mín./máx.</span><span class="sxs-lookup"><span data-stu-id="aecf7-197">UAV Atomic Unsigned Min/Max</span></span></td>
<td><span data-ttu-id="aecf7-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-200">CPU bloqueada</span><span class="sxs-lookup"><span data-stu-id="aecf7-200">CPU Lockable</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="aecf7-201">Un solo formato impide el acceso a la CPU (420_OPAQUE).</span><span class="sxs-lookup"><span data-stu-id="aecf7-201">Only a single format precludes cpu access (420_OPAQUE).</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="aecf7-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-203">RenderTarget de muestreo Multimuestra 4x</span><span class="sxs-lookup"><span data-stu-id="aecf7-203">4x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="aecf7-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-206">RenderTarget de muestreo Multimuestra</span><span class="sxs-lookup"><span data-stu-id="aecf7-206">8x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="aecf7-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-209">Otro número de muestras Multimuestra RT</span><span class="sxs-lookup"><span data-stu-id="aecf7-209">Other Multisample Count RT</span></span></td>
<td><span data-ttu-id="aecf7-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-212">Resolución de muestreo multiejemplo</span><span class="sxs-lookup"><span data-stu-id="aecf7-212">Multisample Resolve</span></span></td>
<td><span data-ttu-id="aecf7-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-215">Carga Multimuestra</span><span class="sxs-lookup"><span data-stu-id="aecf7-215">Multisample Load</span></span></td>
<td><span data-ttu-id="aecf7-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-218">Mostrar Scan-Out</span><span class="sxs-lookup"><span data-stu-id="aecf7-218">Display Scan-Out</span></span></td>
<td><span data-ttu-id="aecf7-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-221">Conversión en el diseño de bits</span><span class="sxs-lookup"><span data-stu-id="aecf7-221">Cast Within Bit Layout</span></span></td>
<td><span data-ttu-id="aecf7-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-224">Compatibilidad con el descodificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="aecf7-224">Video Decoder Support</span></span></td>
<td><span data-ttu-id="aecf7-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-227">Entrada del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="aecf7-227">Video Processor Input</span></span></td>
<td><span data-ttu-id="aecf7-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-230">Salida del procesador de vídeo</span><span class="sxs-lookup"><span data-stu-id="aecf7-230">Video Processor Output</span></span></td>
<td><span data-ttu-id="aecf7-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-233">Recurso compartido</span><span class="sxs-lookup"><span data-stu-id="aecf7-233">Shared Resource</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="aecf7-234">Las texturas de todos los formatos pueden ser recursos compartidos comprometidos o colocarse en montones compartidos.</span><span class="sxs-lookup"><span data-stu-id="aecf7-234">Textures of all formats may be shared committed resources or be placed in shared heaps.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="aecf7-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-236">Conversión de búferes de reserva totalmente tipado</span><span class="sxs-lookup"><span data-stu-id="aecf7-236">BackBuffer Castable Even Fully Typed</span></span></td>
<td><span data-ttu-id="aecf7-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="aecf7-238">No hay ninguna API disponible.</span><span class="sxs-lookup"><span data-stu-id="aecf7-238">No API available.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-239">Recurso en mosaico</span><span class="sxs-lookup"><span data-stu-id="aecf7-239">Tiled Resource</span></span></td>
<td><span data-ttu-id="aecf7-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aecf7-242">Codificador de vídeo</span><span class="sxs-lookup"><span data-stu-id="aecf7-242">Video Encoder</span></span></td>
<td><span data-ttu-id="aecf7-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER(<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aecf7-245">Superposición de Multiplan</span><span class="sxs-lookup"><span data-stu-id="aecf7-245">Multiplane Overlay</span></span></td>
<td><span data-ttu-id="aecf7-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="aecf7-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="aecf7-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="aecf7-248">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aecf7-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aecf7-249">Niveles de características de hardware de D3D12</span><span class="sxs-lookup"><span data-stu-id="aecf7-249">D3D12 Hardware Feature Levels</span></span>](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[<span data-ttu-id="aecf7-250">**formato de DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="aecf7-250">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[<span data-ttu-id="aecf7-251">**\_Compatibilidad con el formato D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="aecf7-251">**D3D11\_FORMAT\_SUPPORT**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[<span data-ttu-id="aecf7-252">**D3D11 \_ formato del \_ cliente2**</span><span class="sxs-lookup"><span data-stu-id="aecf7-252">**D3D11\_FORMAT\_SUPPORT2**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[<span data-ttu-id="aecf7-253">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="aecf7-253">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

