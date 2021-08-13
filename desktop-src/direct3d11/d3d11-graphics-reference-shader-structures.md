---
title: Estructuras de sombreador (gráficos de Direct3D 11)
description: Las estructuras se usan para crear y usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estructuras, sombreadores de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5f5c346e4f46b1ca108200a88ae8b2ad3540585fd1a4bfc73b1dafe2b2b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408195"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Estructuras de sombreador (gráficos de Direct3D 11)

Las estructuras se usan para crear y usar sombreadores.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**D3D11 \_ CLASS \_ INSTANCE \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Describe una instancia de clase HLSL.<br/>                           |
| [**D3D11 \_ COMPUTE \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Describe una instancia de un sombreador de proceso para el seguimiento.<br/>         |
| [**D3D11 \_ DOMAIN \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Describe una instancia de un sombreador de dominio del que se debe hacer un seguimiento.<br/>          |
| [**D3D11 \_ FUNCTION \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Describe una función.<br/>                                       |
| [**D3D11 \_ GEOMETRY \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Describe una instancia de un sombreador de geometría que se debe seguir.<br/>        |
| [**D3D11 \_ TRACE \_ \_ \_ DESC DEL SOMBREADOR DE CASCO**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Describe una instancia de un sombreador de casco para el seguimiento.<br/>            |
| [**BIBLIOTECA D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Describe una biblioteca.<br/>                                        |
| [**D3D11 \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Describe un parámetro de función. <br/>                            |
| [**D3D11 \_ PIXEL \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Describe una instancia de un sombreador de píxeles para el seguimiento.<br/>           |
| [**D3D11 \_ SHADER \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Describe un búfer constante del sombreador.<br/>                         |
| [**D3D11 \_ SHADER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Describe un sombreador.<br/>                                         |
| [**D3D11 \_ SHADER \_ INPUT \_ BIND \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Describe cómo se enlaza un recurso de sombreador a una entrada del sombreador.<br/> |
| [**D3D11 \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Describe un objeto shader-trace.<br/>                            |
| [**D3D11 \_ SHADER \_ TYPE \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Describe un tipo de variable de sombreador.<br/>                           |
| [**D3D11 \_ SHADER \_ VARIABLE \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Describe una variable de sombreador.<br/>                                |
| [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Describe una firma de sombreador.<br/>                               |
| [**D3D11 \_ TRACE \_ REGISTER**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Describe un registro de seguimiento.<br/>                                 |
| [**ESTADÍSTICAS DE SEGUIMIENTO DE D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Especifica estadísticas sobre un seguimiento.<br/>                         |
| [**PASO DE SEGUIMIENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Describe un paso de seguimiento, que es una instrucción.<br/>            |
| [**VALOR DE SEGUIMIENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Describe un valor de seguimiento.<br/>                                    |
| [**D3D11 \_ VERTEX \_ SHADER \_ TRACE \_ DESC**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Describe una instancia de un sombreador de vértices para el seguimiento.<br/>          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de los sombreadores](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





