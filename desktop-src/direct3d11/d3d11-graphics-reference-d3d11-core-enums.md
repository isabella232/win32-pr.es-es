---
title: Enumeraciones básicas de Direct3D 11
description: Esta sección contiene información sobre las enumeraciones principales.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- enumeraciones, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0daf03ca2114f67935e1eb89f34b31306e31fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575301"
---
# <a name="direct3d-11-core-enumerations"></a>Enumeraciones básicas de Direct3D 11

Esta sección contiene información sobre las enumeraciones principales.

## <a name="in-this-section"></a>En esta sección

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a><br/></td>
<td>Marcas opcionales que controlan el comportamiento de <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ID3D11DeviceContext::GetData</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a><br/></td>
<td>Factores de blend, que modularán los valores para el sombreador de píxeles y el destino de representación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a><br/></td>
<td>Operación de combinación RGB o alfa.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a><br/></td>
<td>Especifica las partes de la galería de símbolos de profundidad que se va a borrar. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a><br/></td>
<td>Identifique qué componentes de cada píxel de un destino de representación se pueden escribir durante la mezcla.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a><br/></td>
<td>Opciones de comparación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a><br/></td>
<td>Identifica si la rasterización conservadora está desactivada o no.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a><br/></td>
<td>Especifica si el hardware y el controlador admiten la rasterización conservadora y en qué nivel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a><br/></td>
<td>Especifica el contexto en el que se produce una consulta.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta enumeración es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 y sistemas operativos posteriores.
</blockquote>
<br/> Especifica cómo controlar el contenido existente de un recurso durante una operación de copia o actualización de una región dentro de ese recurso.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a><br/></td>
<td>Opciones para contadores de rendimiento.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a><br/></td>
<td>Tipo de datos de un contador de rendimiento.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a><br/></td>
<td>Describe los parámetros que se usan para crear un dispositivo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a><br/></td>
<td>Describe las marcas que se usan para crear un objeto de estado de contexto de dispositivo (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) con el <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>método ID3D11Device1::CreateDeviceContextState.</strong></a><br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a><br/></td>
<td>Indica que los triángulos orientados a una dirección determinada no se dibujan.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a><br/></td>
<td>Identifique la parte de un búfer de galería de símbolos de profundidad para escribir datos de profundidad.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a><br/></td>
<td>Opciones de contexto de dispositivo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a><br/></td>
<td>Opciones de características de Direct3D 11.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a><br/></td>
<td>Especifica las opciones de barrera. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a><br/></td>
<td>Determina el modo de relleno que se usará al representar triángulos.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a><br/></td>
<td>Opciones de filtrado durante el muestreo de textura.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a><br/></td>
<td>Tipos de filtros de sampler de ampliación o minificación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a><br/></td>
<td>Especifica el tipo de reducción del filtro del muestreador. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a><br/></td>
<td>Qué recursos se admiten para un determinado formato y dispositivo determinado (vea <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device::CheckFormatSupport</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport).</strong></a><br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Opciones de compatibilidad de recursos no ordenados para un recurso de sombreador de proceso <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>(vea ID3D11Device::CheckFeatureSupport</strong></a>). <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a><br/></td>
<td>Tipo de datos contenidos en una ranura de entrada.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta enumeración es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 y sistemas operativos posteriores.
</blockquote>
<br/> Especifica las operaciones lógicas que se configurarán para un destino de representación.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a><br/></td>
<td>Indica cómo la canalización interpreta las primitivas de entrada de geometría o sombreador de casco. <br/></td>
</tr>
<tr>
<td><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a><br/></td>
<td>Cómo interpreta la canalización los datos de vértice enlazados a la fase de ensamblador de entrada. Estos valores de topología primitivos determinan cómo se representan los datos del vértice en la pantalla.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a><br/></td>
<td>Tipos de consulta.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a><br/></td>
<td>Marcas que describen el comportamiento de consulta varios.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a><br/></td>
<td>Opciones para generar un error en una excepción no continuable.<br/></td>
</tr>
<tr>
<td><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a><br/></td>
<td>Describe el nivel de compatibilidad con el almacenamiento en caché del sombreador en el controlador de gráficos actual.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta enumeración es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 y sistemas operativos posteriores.
</blockquote>
<br/> Valores que especifican niveles de precisión mínimos en las fases del sombreador.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a><br/></td>
<td>Define constantes que especifican un nivel para la compatibilidad con recursos compartidos.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a><br/></td>
<td>Operaciones de galería de símbolos que se pueden realizar durante las pruebas de galería de símbolos de profundidad.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a><br/></td>
<td>Identifique una técnica para resolver las coordenadas de textura que están fuera de los límites de una textura.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a><br/></td>
<td>Las distintas caras de una textura de cubo.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a><br/></td>
<td>Indica el nivel en el que se admiten los recursos en mosaico.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Temas relacionados

[Referencia principal](d3d11-graphics-reference-d3d11-core.md)
