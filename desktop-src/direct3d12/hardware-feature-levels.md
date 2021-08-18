---
title: Niveles de características de hardware
description: Describe la funcionalidad de los niveles de características de hardware de 11 \_ 0 a \_ 12 1.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Nivel de característica DX
- Nivel de característica de DirectX
- nivel de característica, DX
- nivel de característica, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf069baca3d9ff56c0d3d98e79bb553df7e8acf1fadf7b5888c5b5d211f7a874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124153"
---
# <a name="hardware-feature-levels"></a>Niveles de características de hardware

Describe la funcionalidad de los niveles de características de hardware de 11 \_ 0 a \_ 12 1.

-   [Sistemas de numeración](#numbering-systems)
-   [Compatibilidad con el nivel de características](#feature-level-support)
-   [Compatibilidad de hardware con formatos DXGI](#hardware-support-for-dxgi-formats)
-   [Temas relacionados](#related-topics)

Para controlar la diversidad de tarjetas de vídeo en máquinas nuevas y existentes, Microsoft Direct3D 11 introdujo el concepto de niveles de características. Cada tarjeta de vídeo implementa un cierto nivel de funcionalidad de Microsoft DirectX (DX) en función de las unidades de procesamiento gráfico (GPU) instaladas. Un nivel de característica es un conjunto bien definido de funcionalidad de GPU. Por ejemplo, el nivel de característica 11 0 implementa la funcionalidad que se \_ implementó en Direct3D 11.

Ahora, cuando cree un dispositivo, puede intentar crear un dispositivo para el nivel de característica que desea solicitar. Si la creación del dispositivo funciona, ese nivel de característica existe, si no es así, el hardware no admite ese nivel de característica. Puede intentar volver a crear un dispositivo en un nivel de característica inferior o puede optar por salir de la aplicación.

Las propiedades básicas de los niveles de características son:

-   Todos los controladores de Direct3D 12 tendrán el nivel de característica 11 \_ 0 o superior.
-   Una GPU que permite crear un dispositivo cumple o supera la funcionalidad de ese nivel de característica.
-   Un nivel de característica siempre incluye la funcionalidad de los niveles de características anteriores o inferiores.
-   Un nivel de característica no implica rendimiento, solo funcionalidad. El rendimiento depende de la implementación de hardware.
-   Se elige un nivel de característica cuando se llama a [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Para obtener información más detallada sobre  las características admitidas (especialmente las marcadas como Opcionales en la tabla siguiente, lo que significa que el hardware podría admitir la característica, pero no es necesario) llame a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Para obtener información sobre las limitaciones de creación de dispositivos de tipo que no son de hardware en determinados niveles de características, vea Limitaciones al crear [dispositivos warp y de referencia.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations) Para obtener más información sobre la introducción de los niveles de características, consulte la documentación de Direct3D 11 sobre los niveles de características [de Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Sistemas de numeración

Los niveles de características de hardware *no son* los mismos que las versiones de API. Por ejemplo, hay una API D3D11.3, pero no hay ningún nivel de \_ característica de hardware 11 3. Los niveles de características se definen en la [**enumeración \_ D3D FEATURE \_ LEVEL.**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)

Hay tres sistemas de numeración distintos:

-   Las versiones de Direct3D usan un punto; por ejemplo, Direct3D 12.0.
-   Los modelos de sombreador usan un punto; por ejemplo, el modelo de sombreador 5.1.
-   Los niveles de características usan un carácter de subrayado; por ejemplo, nivel de característica 12 \_ 0.

## <a name="feature-level-support"></a>Compatibilidad con el nivel de características

Las siguientes características están disponibles para cada nivel de característica de Direct3D.

Los encabezados de la fila superior son niveles de características de Direct3D. Los encabezados de la columna izquierda son características.



| Nivel \\ de característica                                                                                                 | 12 \_ 1ción                    | 12 \_ 0-0                    | 11 \_ 1¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modelo de sombreador                                                                                                             | 5,1                       | 5,1                       | 5.1:                     | 5.1:                     |
| [Nivel de enlace de recursos](hardware-support.md)                                                                            | Nivel 2:                    | Nivel 2:                    | Nivel 1:                   | Nivel 1:                   |
| [Recursos en mosaico](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Nivel 2:                    | Nivel 2:                    | Opcional                 | Opcional                 |
| [Rasterización conservadora](conservative-rasterization.md)                                                             | Nivel 1:                    | Opcional                  | Opcional                 | No                       |
| [Vistas ordenadas por el rasterizador](rasterizer-order-views.md)                                                                   | Sí                       | Opcional                  | Opcional                 | No                       |
| [Filtros mínimos y máximos](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Sí                       | Sí                       | Opcional                 | No                       |
| Asignar búfer predeterminado                                                                                                       | Opcional                  | Opcional                  | Opcional                 | Opcional                 |
| [Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)                                 | Opcional                  | Opcional                  | Opcional                 | No                       |
| [Cargas de la vista de acceso sin ordenar con tipo](typed-unordered-access-view-loads.md)                                               | 18 formatos, más opcionales | 18 formatos, más opcionales | 3 formatos, más opcionales | 3 formatos, más opcionales |
| [Sombreador de geometría](/previous-versions//bb205146(v=vs.85)) | Sí                       | Sí                       | Sí                      | Sí                      |
| [Stream Out](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Sí                       | Sí                       | Sí                      | Sí                      |
| [DirectCompute/Sombreador de proceso](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Sí                       | Sí                       | Sí                      | Sí                      |
| [Sombreadores de casco y dominio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Sí                       | Sí                       | Sí                      | Sí                      |
| [Matrices de recursos de textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| [Matrices de recursos de Asignación de cubos](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| [Compresión de BC1 a BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Sí                       | Sí                       | Sí                      | Sí                      |
| [Alfa a cobertura](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Sí                       | Sí                       | Sí                      | Sí                      |
| [Operaciones lógicas (fusión de salida)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Sí                       | Sí                       | Sí                      | Opcional                 |
| Rasterización independiente del destino                                                                                         | Sí                       | Sí                       | Sí                      | No                       |
| [Varios destinos de representación (MRT) con ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Sí                       | Sí                       | Sí                      | Opcional                 |
| [Número máximo de muestras forzadas para la representación solo de UAV](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimensión de textura máxima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Max Cubemap Dimension                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Extensión máxima del volumen                                                                                                        | 2048                      | 2048                      | 2048                     | 2048                     |
| Repetición máxima de textura                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Anisotropía máxima                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Número máximo de primitivas                                                                                                      | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Índice máximo de vértices                                                                                                         | 2^32 – 1                  | 2^32 – 1                  | 2^32 – 1                 | 2^32 – 1                 |
| Número máximo de ranuras de entrada                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Destinos de representación simultáneos                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Consultas de oclusión                                                                                                        | Sí                       | Sí                       | Sí                      | Sí                      |
| Combinación alfa independiente                                                                                                     | Sí                       | Sí                       | Sí                      | Sí                      |
| Reflejo una vez                                                                                                              | Sí                       | Sí                       | Sí                      | Sí                      |
| Elementos de vértice superpuestos                                                                                              | Sí                       | Sí                       | Sí                      | Sí                      |
| Máscaras de escritura independientes                                                                                                  | Sí                       | Sí                       | Sí                      | Sí                      |
| Instancing                                                                                                               | Sí                       | Sí                       | Sí                      | Sí                      |



 

-   3 Requiere el entorno de ejecución de Direct3D 11.3 o Direct3D 12.
-   ¹ Requiere el tiempo de ejecución de Direct3D 11.1.
-   El modelo 5.0 del sombreador puede admitir opcionalmente sombreadores de precisión doble, sombreadores extendidos de precisión doble, la instrucción de **sombreador SAD4** y sombreadores de precisión parcial. Para determinar las opciones del modelo de sombreador 5.0 que están disponibles, llame a [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Cierta compatibilidad depende del hardware en el que se ejecute: el modelo de sombreador 5.1 solo se admite en el hardware que admite la API de DirectX 12, independientemente del nivel de característica que se esté utilizando. El hardware de DirectX 11 solo admite hasta el modelo de sombreador 5.0. La API de DirectX 12 solo baja al nivel de característica 11 \_ 0.
-   Ntes niveles superiores son opcionales.
-   Los niveles de características 12 0 y 12 1 requieren el entorno de ejecución \_ \_ de Direct3D 11.3 o Direct3D 12.
-   El nivel de característica 11 \_ 1 requiere el entorno de ejecución de Direct3D 11.1.
-   El nivel de característica \_ 11 0 requiere el entorno de ejecución de Direct3D 11.0.

## <a name="hardware-support-for-dxgi-formats"></a>Compatibilidad de hardware con formatos DXGI

Para ver tablas de formatos DXGI y características de hardware, consulte:

-   [Compatibilidad con formato DXGI para hardware de nivel 12.1 de características de Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Compatibilidad con formato DXGI para hardware de nivel 12.0 de características de Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Compatibilidad con el formato DXGI para hardware de nivel 11.1 de características de Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Compatibilidad con formato DXGI para hardware de nivel 11.0 de características de Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Compatibilidad de hardware con formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Compatibilidad de hardware con formatos de Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Compatibilidad de hardware con formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta de funcionalidades](capability-querying.md)
</dt> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
