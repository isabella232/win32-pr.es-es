---
title: Enumeraciones de recursos (gráficos de Direct3D 11)
description: Las enumeraciones se utilizan para especificar información sobre cómo se crean y se obtiene acceso a los recursos durante la representación.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumeraciones, recurso de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104984135"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumeraciones de recursos (gráficos de Direct3D 11)

Las enumeraciones se utilizan para especificar información sobre cómo se crean y se obtiene acceso a los recursos durante la representación.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                               | Descripción                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ marca de enlace \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica cómo enlazar un recurso a la canalización.<br/>                                                                                                                                 |
| [**D3D11 \_ BUFFEREX \_ SRV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica cómo ver un recurso de búfer.<br/>                                                                                                                                          |
| [**\_Marca de \_ UAV de búfer de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica las opciones de vista de acceso desordenado para un recurso de búfer.<br/>                                                                                                                    |
| [**D3D11 \_ \_ marca de nivel de calidad de muestreo Multimuestra \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifica cómo comprobar los niveles de calidad Multimuestra.<br/>                                                                                                                                |
| [**\_Marca de \_ acceso de CPU de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Especifica los tipos de acceso de CPU permitidos para un recurso.<br/>                                                                                                                          |
| [**D3D11 \_ \_ dimensión DSV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Especifica cómo obtener acceso a un recurso usado en una vista de galería de símbolos de profundidad.<br/>                                                                                                                   |
| [**\_Marca de DSV de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opciones de vista de galería de símbolos de profundidad.<br/>                                                                                                                                                        |
| [**\_Mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica un recurso al que se va a obtener acceso para lectura y escritura de la CPU. Las aplicaciones pueden combinar una o varias de estas marcas.<br/>                                                      |
| [**D3D11 \_ marca de mapa \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Especifica cómo debe responder la CPU cuando una aplicación llama al método [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) en un recurso que la GPU está usando.<br/> |
| [**\_Dimensión de recursos D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica el tipo de recurso que se está usando.<br/>                                                                                                                                        |
| [**\_Marca de recursos \_ varios \_ de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica las opciones de los recursos.<br/>                                                                                                                                                  |
| [**D3D11 \_ dimensión de RTV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Estas marcas identifican el tipo de recurso que se va a ver como destino de representación.<br/>                                                                                                  |
| [**Dimensión de D3D11 \_ SRV \_**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Estas marcas identifican el tipo de recurso que se va a ver como un recurso de sombreador.<br/>                                                                                                |
| [**\_Niveles de \_ calidad Multimuestra estándar \_ de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Especifica un tipo de patrón de ejemplo múltiple.<br/>                                                                                                                                             |
| [**D3D11 \_ diseño de textura \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Especifica las opciones de diseño de textura.<br/>                                                                                                                                                  |
| [**\_Marca de \_ copia del icono de D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica cómo copiar un icono.<br/>                                                                                                                                                     |
| [**\_Marca de \_ asignación de iconos de D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica cómo realizar una operación de asignación de mosaicos.<br/>                                                                                                                                |
| [**D3D11 \_ \_ marcador de intervalo de mosaico \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Especifica un intervalo de asignaciones de mosaico que se usará con [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles).<br/>                                                      |
| [**D3D11 \_ \_ dimensión UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Desordenado: opciones de vista de acceso.<br/>                                                                                                                                                     |
| [**Uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica el uso esperado de recursos durante la representación. El uso refleja directamente si un recurso es accesible por la CPU o la unidad de procesamiento de gráficos (GPU).<br/>              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

