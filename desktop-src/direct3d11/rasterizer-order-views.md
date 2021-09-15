---
title: Vistas de orden de rasterizador
description: Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566208"
---
# <a name="rasterizer-order-views"></a>Vistas de orden de rasterizador

Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV. Esto permite que funcionen los algoritmos de transparencia independiente del orden (RSA), que dan resultados de representación mucho mejores cuando varios objetos transparentes están en línea entre sí en una vista.

-   [Información general](#overview)
-   [Detalles de la implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Las canalizaciones de gráficos estándar pueden tener problemas para componer correctamente varias texturas que contienen transparencia. Los objetos como las barreras de cable, el humo, el incendio, la humedad y el cristal coloreado usan la transparencia para obtener el efecto deseado. Los problemas surgen cuando varias texturas que contienen transparencia están en línea entre sí (por ejemplo, el humo delante de una barrera delante de un edificio de cristal que contiene humedad). Las vistas ordenadas por rasterizador (ROV) permiten que los algoritmos DE LAV subyacentes usen características del hardware para intentar resolver el orden de transparencia correctamente. El sombreador de píxeles controla la transparencia.

Las vistas ordenadas por rasterizador (ROV) permiten que el código del sombreador de píxeles marque los enlaces UAV con una declaración que modifique los requisitos normales para el orden de los resultados de la canalización de gráficos para los UAV.

Los ROV garantizan el orden de los accesos UAV para cualquier par de invocaciones de sombreador de píxeles superpuestas. En este caso, la "superposición" significa que las invocaciones se generan mediante las mismas llamadas a draw y comparten la misma coordenada de píxeles en el modo de ejecución de frecuencia de píxeles, y la misma coordenada de píxel y muestra en el modo de frecuencia de muestreo.

El orden en el que se ejecutan los accesos ROV superpuestos de las invocaciones del sombreador de píxeles es idéntico al orden en que se envía la geometría. Esto significa que, para las invocaciones de sombreador de píxeles superpuestas, las escrituras ROV realizadas por una invocación de sombreador de píxeles deben estar disponibles para que las lea una invocación posterior y no deben afectar a las lecturas de una invocación anterior. Las lecturas de ROV realizadas por una invocación de sombreador de píxeles deben reflejar las escrituras de una invocación anterior y no deben reflejar las escrituras realizadas por una invocación posterior. Esto es importante para los UAV porque se omiten explícitamente de las garantías de invariable de salida establecidas normalmente por el orden fijo de los resultados de la canalización de gráficos.

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

-   [**D3D11 \_ RASTERIZER \_ DESC2:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) estructura que mantiene la descripción del rasterizador, y que tiene en cuenta la clase auxiliar CD3D12 \_ RASTERIZER DESC2 para crear descripciones \_ de rasterizador.
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) estructura que mantiene el valor booleano `ROVsSupported` , que indica la compatibilidad.
-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) método para acceder a las características admitidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11.3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 