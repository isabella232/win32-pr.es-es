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
# <a name="direct3d-11-core-structures"></a>Estructuras básicas de Direct3D 11

Esta sección contiene información sobre las estructuras principales.

## <a name="in-this-section"></a>En esta sección

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br/></td>
<td>Describe el estado de Blend que se usa en una llamada a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: CreateBlendState</strong></a> para crear un objeto de estado de mezcla. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe el estado de Blend que se usa en una llamada a <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> para crear un objeto de estado de mezcla. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br/></td>
<td>Define un cuadro 3D.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br/></td>
<td>Describe un contador.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br/></td>
<td>Información acerca de las capacidades del contador de rendimiento de la tarjeta de vídeo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br/></td>
<td>Describe el estado de la galería de símbolos de profundidad.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br/></td>
<td>Las operaciones de estarcido que se pueden realizar en función de los resultados de la prueba de estarcido.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Argumentos para dibujar instancias indizadas indirectas. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Argumentos para la instancia de Draw indirecta. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe información acerca de la arquitectura del adaptador de Direct3D 11,1.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br/></td>
<td>Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe la compatibilidad con las sombras de Direct3D 9 en el controlador de gráficos actual. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br/></td>
<td>Describe si se admite la creación de instancias simples.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br/></td>
<td>Describe el sombreador de cálculo y la compatibilidad con el búfer sin formato y estructurado en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe las opciones de características de Direct3D 11,1 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br/></td>
<td>Describe las opciones de características de Direct3D 11,2 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br/></td>
<td>Describe las opciones de características de Direct3D 11,3 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br/></td>
<td>Describe las opciones de características de Direct3D 11,3 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br/></td>
<td>Describe las opciones de características de Direct3D 11,4 en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br/></td>
<td>Describe el nivel de compatibilidad para los recursos compartidos en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br/></td>
<td>Describe la compatibilidad de tipos de datos Double en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br/></td>
<td>Describe qué recursos son compatibles con el controlador de gráficos actual para un formato determinado.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Describe qué opciones de recursos no ordenados son compatibles con el controlador de gráficos actual para un formato determinado.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br/></td>
<td>Describe la compatibilidad con direcciones virtuales de GPU de datos de características, incluidos los bits de dirección máximos por recurso y por proceso. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br/></td>
<td>Describe si se admite una técnica de generación de perfiles de GPU.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br/></td>
<td>Describe el nivel de almacenamiento en caché del sombreador que se admite en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe las opciones de compatibilidad de precisión para los sombreadores en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br/></td>
<td>Describe las características de subprocesamiento múltiple admitidas por el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br/></td>
<td>Descripción de un elemento único para la fase del ensamblador de entrada.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br/></td>
<td>Consulte la información sobre la actividad de la canalización de gráficos entre las llamadas a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> y <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br/></td>
<td>Consulte la información sobre la cantidad de datos que se transmiten a los búferes de salida de flujo entre <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> y <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: end</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br/></td>
<td>Consultar información sobre la confiabilidad de una consulta de marca de tiempo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br/></td>
<td>Describe una consulta.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br/></td>
<td>Describe una consulta.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br/></td>
<td>Describe el estado de rasterizador.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe el estado de rasterizador.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br/></td>
<td>Describe el estado de rasterizador.<br/></td>
</tr>
<tr>
<td><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br/></td>
<td>D3D11_RECT se declara de la siguiente manera:<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br/></td>
<td>Describe el estado de Blend para un destino de representación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta estructura es compatible con el tiempo de ejecución de Direct3D 11,1, que está disponible en Windows 8 y en los sistemas operativos posteriores.
</blockquote>
<br/> Describe el estado de Blend para un destino de representación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br/></td>
<td>Describe un estado de muestra.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br/></td>
<td>Descripción de un elemento de vértice en un búfer de vértice en una ranura de salida.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br/></td>
<td>Define las dimensiones de una ventanilla.<br/></td>
</tr>
</tbody>
</table>

Además, hay una estructura de rectángulo 2D definida en D3D11. h.

```cpp
typedef RECT D3D11_RECT;
```

Para obtener documentación, vea [Rect](/previous-versions/dd162897%28v%3dvs.85%29) en [Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>Temas relacionados

[Referencia básica](d3d11-graphics-reference-d3d11-core.md)