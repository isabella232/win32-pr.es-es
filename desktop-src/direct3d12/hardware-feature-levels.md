---
title: Niveles de características de hardware
description: Describe la funcionalidad de los \_ niveles de características de hardware 11 0 a 12 \_ 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Nivel de característica de DX
- Nivel de característica de DirectX
- nivel de característica, DX
- nivel de características, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d464f6cc52539e31fee5e234af2c045dfff7e413
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104549069"
---
# <a name="hardware-feature-levels"></a>Niveles de características de hardware

Describe la funcionalidad de los \_ niveles de características de hardware 11 0 a 12 \_ 1.

-   [Sistemas de numeración](#numbering-systems)
-   [Compatibilidad de nivel de características](#feature-level-support)
-   [Compatibilidad de hardware con formatos de DXGI](#hardware-support-for-dxgi-formats)
-   [Temas relacionados](#related-topics)

Para controlar la diversidad de tarjetas de vídeo en máquinas nuevas y existentes, Microsoft Direct3D 11 presentó el concepto de niveles de características. Cada tarjeta de vídeo implementa un cierto nivel de funcionalidad de Microsoft DirectX (DX) en función de las unidades de procesamiento de gráficos (GPU) instaladas. Un nivel de característica es un conjunto bien definido de funcionalidades de GPU. Por ejemplo, el \_ nivel de características 11 0 implementa la funcionalidad que se implementó en Direct3D 11.

Ahora, cuando cree un dispositivo, puede intentar crear un dispositivo para el nivel de característica que desea solicitar. Si la creación del dispositivo funciona, ese nivel de característica existe, de lo contrario, el hardware no admite ese nivel de características. Puede intentar volver a crear un dispositivo en un nivel de características inferior o puede salir de la aplicación.

Las propiedades básicas de los niveles de características son:

-   Todos los controladores de Direct3D 12 tendrán el nivel \_ de características 11 0 o superior.
-   Una GPU que permite crear un dispositivo cumple o supera la funcionalidad de dicho nivel de características.
-   Un nivel de característica siempre incluye la funcionalidad de niveles de características anteriores o inferiores.
-   Un nivel de característica no implica el rendimiento, solo la funcionalidad. El rendimiento depende de la implementación de hardware.
-   Se elige un nivel de característica cuando se llama a [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Para obtener información más detallada sobre las características admitidas (especialmente las marcadas como *opcionales* en la tabla siguiente, lo que significa que el hardware puede admitir la característica, pero no es necesario), llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Para obtener información sobre las limitaciones de la creación de dispositivos de tipo que no son de hardware en determinados niveles de características, vea [limitaciones para crear dispositivos](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations)de hipertexto y de referencia. Para obtener más información sobre la introducción de los niveles de características, consulte la documentación de Direct3D 11 sobre [los niveles de características de Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Sistemas de numeración

Los niveles de características de hardware *no* son los mismos que las versiones de API. Por ejemplo, hay una API D3D 11.3, pero no hay ningún nivel de \_ características de hardware de 11 3. Los niveles de características se definen en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) .

Hay tres sistemas de numeración distintos:

-   Las versiones de Direct3D usan un punto; por ejemplo, Direct3D 12,0.
-   Los modelos de sombreador usan un punto; por ejemplo, el modelo de sombreador 5,1.
-   Los niveles de características usan un carácter de subrayado; por ejemplo, nivel de característica 12 \_ 0.

## <a name="feature-level-support"></a>Compatibilidad de nivel de características

Las siguientes características están disponibles para cada nivel de característica de Direct3D.

Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características.



| Nivel de característica de características \\                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modelo de sombreador                                                                                                             | 5,1                       | 5,1                       | 5,1 ²                     | 5,1 ²                     |
| [Nivel de enlace de recursos](hardware-support.md)                                                                            | Tier2 ³                    | Tier2 ³                    | Tier1 ³                   | Tier1 ³                   |
| [Recursos en mosaico](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Tier2 ³                    | Tier2 ³                    | Opcional                 | Opcional                 |
| [Rasterización conservadora](conservative-rasterization.md)                                                             | Tier1 ³                    | Opcional                  | Opcional                 | No                       |
| [Vistas ordenadas de rasterizador](rasterizer-order-views.md)                                                                   | Sí                       | Opcional                  | Opcional                 | No                       |
| [Filtros mín./máx.](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Sí                       | Sí                       | Opcional                 | No                       |
| Asignar búfer predeterminado                                                                                                       | Opcional                  | Opcional                  | Opcional                 | Opcional                 |
| [Valor de referencia de estarcido del sombreador especificado](shader-specified-stencil-reference-value.md)                                 | Opcional                  | Opcional                  | Opcional                 | No                       |
| [Cargas de vista de acceso no ordenada con tipo](typed-unordered-access-view-loads.md)                                               | 18 formatos, más opcionales | 18 formatos, más opcionales | 3 formatos, más opcionales | 3 formatos, más opcionales |
| [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) | Sí                       | Sí                       | Sí                      | Sí                      |
| [Transmisión por secuencias](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Sí                       | Sí                       | Sí                      | Sí                      |
| [DirectCompute/sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Sí                       | Sí                       | Sí                      | Sí                      |
| [Sombreadores de casco y de dominio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Sí                       | Sí                       | Sí                      | Sí                      |
| [Matrices de recursos de textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| [Matrices de recursos mapa](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| [Compresión de BC1 a BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Sí                       | Sí                       | Sí                      | Sí                      |
| [Alfa a cobertura](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Sí                       | Sí                       | Sí                      | Sí                      |
| [Operaciones lógicas (fusión de salida)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Sí                       | Sí                       | Sí                      | Opcional                 |
| Rasterización independiente del destino                                                                                         | Sí                       | Sí                       | Sí                      | No                       |
| [Destino de representación múltiple (MRT) con ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Sí                       | Sí                       | Sí                      | Opcional                 |
| [Recuento de muestras forzadas máximas para la representación solo UAV](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimensión de textura máxima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Dimensión mapa máxima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Extensión de volumen máxima                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Repetición de textura máxima                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Anisotropía máx.                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Recuento máximo de primitivas                                                                                                      | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Índice de vértice máximo                                                                                                         | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Máximo de ranuras de entrada                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Destinos de representación simultáneos                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Consultas de oclusión                                                                                                        | Sí                       | Sí                       | Sí                      | Sí                      |
| Combinación alfa independiente                                                                                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| Reflejar una vez                                                                                                              | Sí                       | Sí                       | Sí                      | Sí                      |
| Elementos de vértice superpuestos                                                                                              | Sí                       | Sí                       | Sí                      | Sí                      |
| Máscaras de escritura independientes                                                                                                  | Sí                       | Sí                       | Sí                      | Sí                      |
| Instancing                                                                                                               | Sí                       | Sí                       | Sí                      | Sí                      |



 

-   ⁰ requiere el tiempo de ejecución de Direct3D 11,3 o Direct3D 12.
-   ¹ requiere el tiempo de ejecución de Direct3D 11,1.
-   ² el modelo de sombreador 5,0 puede admitir opcionalmente los sombreadores de doble precisión, los sombreadores de precisión doble extendidos, la instrucción del sombreador **SAD4** y los sombreadores de precisión parcial. Para determinar las opciones del modelo de sombreador 5,0 que están disponibles, llame a [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Cierta compatibilidad depende del hardware en el que se ejecuta: el modelo de sombreador 5,1 solo se admite en hardware que admita la API de DirectX 12, independientemente del nivel de característica que se esté usando. El hardware de DirectX 11 solo admite hasta el modelo de sombreador 5,0. La API de DirectX 12 solo deja de funcionar hasta el nivel de características 11 \_ 0.
-   los niveles superiores de ³ son opcionales.
-   Los niveles de características 12 \_ 0 y 12 \_ 1 requieren el tiempo de ejecución de Direct3D 11,3 o Direct3D 12.
-   El nivel de características 11 \_ 1 requiere el tiempo de ejecución de Direct3D 11,1.
-   El nivel de característica 11 \_ 0 requiere el tiempo de ejecución de Direct3D 11,0.

## <a name="hardware-support-for-dxgi-formats"></a>Compatibilidad de hardware con formatos de DXGI

Para ver las tablas de formatos y características de hardware de DXGI, consulte:

-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Compatibilidad con el formato de DXGI para el hardware de nivel de característica de Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Compatibilidad de hardware con formatos 10Level9 de Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta de funcionalidades](capability-querying.md)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
