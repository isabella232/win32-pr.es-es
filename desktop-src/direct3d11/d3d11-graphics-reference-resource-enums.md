---
title: Enumeraciones de recursos (gráficos de Direct3D 11)
description: Las enumeraciones se usan para especificar información sobre cómo se crean y se accede a los recursos durante la representación.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumeraciones, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966908"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumeraciones de recursos (gráficos de Direct3D 11)

Las enumeraciones se usan para especificar información sobre cómo se crean y se accede a los recursos durante la representación.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                               | Descripción                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ BIND \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica cómo enlazar un recurso a la canalización.<br/>                                                                                                                                 |
| [**D3D11 \_ BUFFEREX \_ SRV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica cómo ver un recurso de búfer.<br/>                                                                                                                                          |
| [**D3D11 \_ BUFFER \_ UAV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica las opciones de vista de acceso desordenado para un recurso de búfer.<br/>                                                                                                                    |
| [**D3D11 \_ CHECK \_ MULTISAMPLE \_ QUALITY \_ LEVELS \_ FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifica cómo comprobar los niveles de calidad de varios muestreos.<br/>                                                                                                                                |
| [**MARCA DE ACCESO DE CPU D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Especifica los tipos de acceso de CPU permitidos para un recurso.<br/>                                                                                                                          |
| [**D3D11 \_ DIMENSIÓN DSV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Especifica cómo acceder a un recurso usado en una vista de galería de símbolos de profundidad.<br/>                                                                                                                   |
| [**D3D11 \_ DSV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opciones de vista de galería de símbolos de profundidad.<br/>                                                                                                                                                        |
| [**MAPA D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica un recurso al que se va a acceder para leer y escribir por parte de la CPU. Las aplicaciones pueden combinar una o varias de estas marcas.<br/>                                                      |
| [**MARCA DE MAPA D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Especifica cómo debe responder la CPU cuando una aplicación llama al método [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) en un recurso que usa la GPU.<br/> |
| [**DIMENSIÓN DE RECURSOS D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica el tipo de recurso que se usa.<br/>                                                                                                                                        |
| [**MARCA MISC DEL RECURSO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica las opciones de los recursos.<br/>                                                                                                                                                  |
| [**DIMENSIÓN RTV D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Estas marcas identifican el tipo de recurso que se verá como un destino de representación.<br/>                                                                                                  |
| [**D3D11 \_ SRV \_ DIMENSION**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Estas marcas identifican el tipo de recurso que se verá como un recurso de sombreador.<br/>                                                                                                |
| [**NIVELES DE CALIDAD ESTÁNDAR DE MÚLTIPLES MUESTRAS D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Especifica un tipo de patrón de varios ejemplos.<br/>                                                                                                                                             |
| [**DISEÑO DE TEXTURA D3D11 \_ \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Especifica las opciones de diseño de textura.<br/>                                                                                                                                                  |
| [**MARCA DE COPIA DE ICONO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica cómo copiar un icono.<br/>                                                                                                                                                     |
| [**MARCA DE ASIGNACIÓN DE MOSAICOS D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica cómo realizar una operación de asignación de mosaicos.<br/>                                                                                                                                |
| [**MARCA DE INTERVALO \_ DE MOSAICOS D3D11 \_ \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Especifica un intervalo de asignaciones de mosaico que se van a usar [**con ID3D11DeviceContext2::UpdateTiles.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)<br/>                                                      |
| [**D3D11 \_ UAV \_ DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Opciones de vista de acceso desordenado.<br/>                                                                                                                                                     |
| [**USO DE D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica el uso esperado de recursos durante la representación. El uso refleja directamente si la CPU o la unidad de procesamiento gráfico (GPU) pueden acceder a un recurso.<br/>              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

