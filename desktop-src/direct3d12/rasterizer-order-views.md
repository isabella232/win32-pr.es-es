---
title: Vistas ordenadas por rasterizador
description: Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque enlaces de vista de acceso no ordenados con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para uavs.
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214098f70608d5f20d24edb1312593c6215abea12efecfc6eea97148e8855cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300986"
---
# <a name="rasterizer-ordered-views"></a>Vistas ordenadas por rasterizador

Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque enlaces de vista de acceso desordenado (UAV) con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV. Esto permite que funcionen los algoritmos de transparencia independiente del orden (RSA), que dan resultados de representación mucho mejores cuando varios objetos transparentes se alinean entre sí en una vista.

-   [Información general](#overview)
-   [Detalles de la implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Las canalizaciones de gráficos estándar pueden tener problemas para componer correctamente varias texturas que contienen transparencia. Los objetos como las barreras de cable, el humo, el incendio, la humedad y el cristal coloreado usan la transparencia para obtener el efecto deseado. Los problemas surgen cuando varias texturas que contienen transparencia se alinean entre sí (por ejemplo, el humo delante de una barrera delante de un edificio de cristal que contiene humedad). Las vistas ordenadas por rasterizadores (ROV) permiten a los algoritmos de LAV subyacentes usar las características del hardware para intentar resolver el orden de transparencia correctamente. El sombreador de píxeles controla la transparencia.

Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV.

Las ROV garantizan el orden de los accesos UAV para cualquier par de invocaciones de sombreador de píxeles superpuestas. En este caso, "superposición" significa que las invocaciones se generan mediante las mismas llamadas a draw y comparten la misma coordenada de píxeles cuando están en modo de ejecución de frecuencia de píxeles, y la misma coordenada de píxel y muestra en modo de frecuencia de muestreo.

El orden en el que se ejecutan los accesos ROV superpuestos de las invocaciones del sombreador de píxeles es idéntico al orden en que se envía la geometría. Esto significa que, para las invocaciones de sombreador de píxeles superpuestas, las escrituras de ROV realizadas por una invocación de sombreador de píxeles deben estar disponibles para que las lea una invocación posterior y no deben afectar a las lecturas de una invocación anterior. Las lecturas de ROV realizadas por una invocación de sombreador de píxeles deben reflejar las escrituras de una invocación anterior y no deben reflejar las escrituras realizadas por una invocación posterior. Esto es importante para los UAV porque se omiten explícitamente de las garantías de invariancia de salida establecidas normalmente por el orden fijo de los resultados de la canalización de gráficos.

## <a name="implementation-details"></a>Detalles de la implementación

Las vistas ordenadas por rasterizador (ROV) se declaran con los siguientes nuevos objetos de Lenguaje de sombreador de alto nivel (HLSL) y solo están disponibles para el sombreador de píxeles:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Use estos objetos de la misma manera que otros objetos UAV (por `RWBuffer` ejemplo, etc.).

## <a name="api-summary"></a>API summary

Los ROV son una construcción solo HLSL que aplica semántica de comportamiento diferente a los UAV. Todas las API relevantes para los UAV también son relevantes para los ROV. Tenga en cuenta que el método, las estructuras y la clase auxiliar siguientes hacen referencia al rasterizador:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) estructura que mantiene la descripción del rasterizador.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) estructura que mantiene un valor booleano, que indica la compatibilidad.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) método para acceder a las características admitidas.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) clase auxiliar para crear descripciones de rasterizador.
-   [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) estructura que mantiene el estado de canalización.

## <a name="related-topics"></a>Temas relacionados

* [Rasterización conservadora](conservative-rasterization.md)
* [Representación](rendering.md)
* [Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
* [Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)