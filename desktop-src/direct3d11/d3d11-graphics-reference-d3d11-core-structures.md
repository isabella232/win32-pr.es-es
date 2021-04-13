---
title: Estructuras básicas de Direct3D 11
description: Esta sección contiene información sobre las estructuras principales.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- estructuras, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421050"
---
# <a name="direct3d-11-core-structures"></a><span data-ttu-id="414d1-104">Estructuras básicas de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="414d1-104">Direct3D 11 core structures</span></span>

<span data-ttu-id="414d1-105">Esta sección contiene información sobre las estructuras principales.</span><span class="sxs-lookup"><span data-stu-id="414d1-105">This section contains information about the core structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="414d1-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="414d1-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="414d1-107">Tema</span><span class="sxs-lookup"><span data-stu-id="414d1-107">Topic</span></span></th>
<th><span data-ttu-id="414d1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="414d1-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="414d1-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-110">Describe el estado de Blend que se usa en una llamada a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: CreateBlendState</strong></a> para crear un objeto de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="414d1-110">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-112">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-112">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-113">Describe el estado de Blend que se usa en una llamada a <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> para crear un objeto de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="414d1-113">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-115">Define un cuadro 3D.</span><span class="sxs-lookup"><span data-stu-id="414d1-115">Defines a 3D box.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-117">Describe un contador.</span><span class="sxs-lookup"><span data-stu-id="414d1-117">Describes a counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-119">Información acerca de las capacidades del contador de rendimiento de la tarjeta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="414d1-119">Information about the video card's performance counter capabilities.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-121">Describe el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="414d1-121">Describes depth-stencil state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-123">Las operaciones de estarcido que se pueden realizar en función de los resultados de la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="414d1-123">Stencil operations that can be performed based on the results of stencil test.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-125">Argumentos para dibujar instancias indizadas indirectas.</span><span class="sxs-lookup"><span data-stu-id="414d1-125">Arguments for draw indexed instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-127">Argumentos para la instancia de Draw indirecta.</span><span class="sxs-lookup"><span data-stu-id="414d1-127">Arguments for draw instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-129">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-129">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-130">Describe información acerca de la arquitectura del adaptador de Direct3D 11,1.</span><span class="sxs-lookup"><span data-stu-id="414d1-130">Describes information about Direct3D 11.1 adapter architecture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-132">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-132">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-133">Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-133">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-135">Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-135">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-137">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-137">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-138">Describe la compatibilidad con las sombras de Direct3D 9 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-138">Describes Direct3D 9 shadow support in the current graphics driver.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-140">Describe si se admite la creación de instancias simples.</span><span class="sxs-lookup"><span data-stu-id="414d1-140">Describes whether simple instancing is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-142">Describe el sombreador de cálculo y la compatibilidad con el búfer sin formato y estructurado en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-142">Describes compute shader and raw and structured buffer support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-144">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-144">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-145">Describe las opciones de características de Direct3D 11,1 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-145">Describes Direct3D 11.1 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-147">Describe las opciones de características de Direct3D 11,2 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-147">Describes Direct3D 11.2 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-149">Describe las opciones de características de Direct3D 11,3 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-149">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-151">Describe las opciones de características de Direct3D 11,3 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-151">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-153">Describe las opciones de características de Direct3D 11,4 en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-153">Describes Direct3D 11.4 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-155">Describe el nivel de compatibilidad para los recursos compartidos en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-155">Describes the level of support for shared resources in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-157">Describe la compatibilidad de tipos de datos Double en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-157">Describes double data type support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-159">Describe qué recursos son compatibles con el controlador de gráficos actual para un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="414d1-159">Describes which resources are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-161">Describe qué opciones de recursos no ordenados son compatibles con el controlador de gráficos actual para un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="414d1-161">Describes which unordered resource options are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-163">Describe la compatibilidad con direcciones virtuales de GPU de datos de características, incluidos los bits de dirección máximos por recurso y por proceso.</span><span class="sxs-lookup"><span data-stu-id="414d1-163">Describes feature data GPU virtual address support, including maximum address bits per resource and per process.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-165">Describe si se admite una técnica de generación de perfiles de GPU.</span><span class="sxs-lookup"><span data-stu-id="414d1-165">Describes whether a GPU profiling technique is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-167">Describe el nivel de almacenamiento en caché del sombreador que se admite en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-167">Describes the level of shader caching supported in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-169">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-169">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-170">Describe las opciones de compatibilidad de precisión para los sombreadores en el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-170">Describes precision support options for shaders in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-172">Describe las características de subprocesamiento múltiple admitidas por el controlador de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="414d1-172">Describes the multi-threading features that are supported by the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-174">Descripción de un elemento único para la fase del ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="414d1-174">A description of a single element for the input-assembler stage.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-176">Consulte la información sobre la actividad de la canalización de gráficos entre las llamadas a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> y <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="414d1-176">Query information about graphics-pipeline activity in between calls to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-178">Consulte la información sobre la cantidad de datos que se transmiten a los búferes de salida de flujo entre <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> y <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="414d1-178">Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-180">Consultar información sobre la confiabilidad de una consulta de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="414d1-180">Query information about the reliability of a timestamp query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-182">Describe una consulta.</span><span class="sxs-lookup"><span data-stu-id="414d1-182">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-184">Describe una consulta.</span><span class="sxs-lookup"><span data-stu-id="414d1-184">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-186">Describe el estado de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="414d1-186">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-188">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-188">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-189">Describe el estado de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="414d1-189">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-191">Describe el estado de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="414d1-191">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-193">D3D11_RECT se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="414d1-193">D3D11_RECT is declared as follows:</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-195">Describe el estado de Blend para un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="414d1-195">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="414d1-197">Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="414d1-197">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="414d1-198">Describe el estado de Blend para un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="414d1-198">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-200">Describe un estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="414d1-200">Describes a sampler state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-202">Descripción de un elemento de vértice en un búfer de vértice en una ranura de salida.</span><span class="sxs-lookup"><span data-stu-id="414d1-202">Description of a vertex element in a vertex buffer in an output slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="414d1-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="414d1-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="414d1-204">Define las dimensiones de una ventanilla.</span><span class="sxs-lookup"><span data-stu-id="414d1-204">Defines the dimensions of a viewport.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="414d1-205">Además, hay una estructura de rectángulo 2D definida en D3D11. h.</span><span class="sxs-lookup"><span data-stu-id="414d1-205">In addition, there's a 2D rectangle structure defined in D3D11.h.</span></span>

```cpp
typedef RECT D3D11_RECT;
```

<span data-ttu-id="414d1-206">Para obtener documentación, vea [Rect](/previous-versions/dd162897%28v%3dvs.85%29) en [Windows GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="414d1-206">For documentation, see [RECT](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="414d1-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="414d1-207">Related topics</span></span>

[<span data-ttu-id="414d1-208">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="414d1-208">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)