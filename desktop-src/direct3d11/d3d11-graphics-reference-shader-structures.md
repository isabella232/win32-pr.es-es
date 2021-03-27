---
title: Estructuras de sombreador (gráficos de Direct3D 11)
description: Las estructuras se usan para crear y usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estructuras, sombreadores de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800842"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Estructuras de sombreador (gráficos de Direct3D 11)

Las estructuras se usan para crear y usar sombreadores.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Descripción de la \_ instancia de clase D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Describe una instancia de la clase HLSL.<br/>                           |
| [**\_Descripción de \_ seguimiento del sombreador de cálculo de \_ D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Describe una instancia de un sombreador de cálculo que se va a trazar.<br/>         |
| [**\_Descripción de \_ seguimiento del sombreador de dominio de \_ D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Describe una instancia de un sombreador de dominio para realizar el seguimiento.<br/>          |
| [**D3D11 \_ función \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Describe una función.<br/>                                       |
| [**D3D11 \_ \_ DESC del sombreador de geometría \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Describe una instancia de un sombreador de geometría del que se realiza el seguimiento.<br/>        |
| [**DESC. de \_ \_ seguimiento del sombreador de casco D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Describe una instancia de un sombreador de casco para realizar el seguimiento.<br/>            |
| [**Descripción de la \_ biblioteca D3D11 \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Describe una biblioteca de.<br/>                                        |
| [**\_Parámetro D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Describe un parámetro de función. <br/>                            |
| [**DESC. de \_ \_ seguimiento del sombreador de píxeles D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Describe una instancia de un sombreador de píxeles para el seguimiento.<br/>           |
| [**\_Desc. búfer del sombreador de D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Describe un búfer de constantes de sombreador.<br/>                         |
| [**\_Descripción del sombreador D3D11 \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Describe un sombreador.<br/>                                         |
| [**\_DESC de enlace de entrada del sombreador D3D11 \_ \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Describe cómo un recurso de sombreador se enlaza a una entrada de sombreador.<br/> |
| [**\_Descripción del sombreador de D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Describe un objeto de seguimiento de sombreador.<br/>                            |
| [**\_Tipo de sombreador D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Describe un tipo de variable de sombreador.<br/>                           |
| [**D3D11 \_ variable de sombreador \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Describe una variable de sombreador.<br/>                                |
| [**\_Parámetro de firma D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Describe una firma de sombreador.<br/>                               |
| [**\_Registro de seguimiento de D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Describe un registro de seguimiento.<br/>                                 |
| [**\_Estadísticas de seguimiento de D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Especifica las estadísticas de un seguimiento.<br/>                         |
| [**\_Paso de seguimiento de D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Describe un paso de seguimiento, que es una instrucción.<br/>            |
| [**\_Valor de seguimiento D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Describe un valor de seguimiento.<br/>                                    |
| [**\_Descripción de \_ seguimiento del sombreador de VÉRTICEs D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Describe una instancia de un sombreador de vértices para realizar un seguimiento.<br/>          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de los sombreadores](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





