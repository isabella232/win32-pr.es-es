---
title: Estructuras básicas de Direct3D 11
description: Esta sección contiene información sobre las estructuras principales.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- estructuras, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf2daccc08066d37c00ed2a4b15a19da35afb8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575293"
---
# <a name="direct3d-11-core-structures"></a>Estructuras básicas de Direct3D 11

Esta sección contiene información sobre las estructuras principales.

## <a name="in-this-section"></a>En esta sección


| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br /> | Describe el estado de mezcla que se usa en una llamada a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> para crear un objeto blend-state. <br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe el estado de mezcla que se usa en una llamada a <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> para crear un objeto blend-state. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br /> | Define un cuadro 3D.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br /> | Describe un contador.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br /> | Información sobre las funcionalidades del contador de rendimiento de la tarjeta de vídeo.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br /> | Describe el estado de la galería de símbolos de profundidad.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br /> | Operaciones de galería de símbolos que se pueden realizar en función de los resultados de la prueba de galería de símbolos.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br /> | Argumentos para draw indexed instanced indirect. <br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br /> | Argumentos para draw instanced indirect. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe información sobre la arquitectura del adaptador de Direct3D 11.1.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br /> | Describe las opciones de características de Direct3D 9 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe la compatibilidad con sombras de Direct3D 9 en el controlador de gráficos actual. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br /> | Describe si se admite la creación de instancias simples.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br /> | Describe el sombreador de proceso y la compatibilidad con búferes sin formato y estructurados en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe las opciones de características de Direct3D 11.1 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br /> | Describe las opciones de características de Direct3D 11.2 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br /> | Describe las opciones de características de Direct3D 11.3 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br /> | Describe las opciones de características de Direct3D 11.3 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br /> | Describe las opciones de características de Direct3D 11.4 en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br /> | Describe el nivel de compatibilidad con los recursos compartidos en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br /> | Describe la compatibilidad con tipos de datos dobles en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br /> | Describe qué recursos son compatibles con el controlador de gráficos actual para un formato determinado.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br /> | Describe qué opciones de recursos no ordenados son compatibles con el controlador de gráficos actual para un formato determinado.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br /> | Describe la compatibilidad con direcciones virtuales de GPU de datos de características, incluidos los bits de dirección máximos por recurso y por proceso. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br /> | Describe si se admite una técnica de generación de perfiles de GPU.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br /> | Describe el nivel de almacenamiento en caché del sombreador admitido en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe las opciones de compatibilidad de precisión para sombreadores en el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br /> | Describe las características multiproceso que admite el controlador de gráficos actual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br /> | Descripción de un único elemento para la fase de ensamblador de entrada.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br /> | Consulte información sobre la actividad de canalización de gráficos entre llamadas a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br /> | Consulte información sobre la cantidad de datos transmitidos a los búferes de salida de flujo entre <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End.</strong></a><br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br /> | Información de consulta sobre la confiabilidad de una consulta de marca de tiempo.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br /> | Describe una consulta.<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br /> | Describe una consulta.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br /> | Describe el estado del rasterizador.<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe el estado del rasterizador.<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br /> | Describe el estado del rasterizador.<br /> | 
| <a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br /> | D3D11_RECT se declara de la siguiente manera:<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br /> | Describe el estado de mezcla de un destino de representación.<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />Esta estructura es compatible con el entorno de ejecución de Direct3D 11.1, que está disponible en Windows 8 sistemas operativos posteriores.</blockquote><br /> Describe el estado de mezcla de un destino de representación.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br /> | Describe un estado de muestreador.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br /> | Descripción de un elemento de vértice en un búfer de vértices en una ranura de salida.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br /> | Define las dimensiones de una ventanilla.<br /> | 


Además, hay una estructura de rectángulo 2D definida en D3D11.h.

```cpp
typedef RECT D3D11_RECT;
```

Para obtener documentación, [vea RECT](/previous-versions/dd162897%28v%3dvs.85%29) en [Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>Temas relacionados

[Referencia principal](d3d11-graphics-reference-d3d11-core.md)
