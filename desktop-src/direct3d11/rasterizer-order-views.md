---
title: Vistas de orden de rasterizador
description: Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149494"
---
# <a name="rasterizer-order-views"></a>Vistas de orden de rasterizador

Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs. Esto permite que funcionen los algoritmos de transparencia independiente de orden (OIT), que proporcionan resultados de representación mucho mejores cuando varios objetos transparentes están alineados entre sí en una vista.

-   [Información general](#overview)
-   [Detalles de implementación](#implementation-details)
-   [Resumen de API](#api-summary)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Las canalizaciones de gráficos estándar pueden tener problemas al componer varias texturas que contienen transparencias correctamente. Los objetos como las barreras de alambres, humos, incendios, vegetación y vidrio en color usan transparencia para obtener el efecto deseado. Surgen problemas cuando varias texturas que contienen transparencias están alineadas entre sí (humo delante de una barrera delante de un edificio de vidrio que contiene vegetación, por ejemplo). Las vistas ordenadas de rasterizador (ROVs) permiten que los algoritmos OIT subyacentes usen características del hardware para intentar resolver el orden de transparencia correctamente. El sombreador de píxeles controla la transparencia.

Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.

ROVs garantiza el orden de los accesos a UAV para cualquier par de invocaciones del sombreador de píxeles superpuestos. En este caso "superpuesta" significa que las invocaciones se generan mediante las mismas llamadas a Draw y comparten la misma coordenada de píxeles en el modo de ejecución de frecuencia de píxeles y el mismo píxel y la coordenada de ejemplo en el modo de frecuencia de muestreo.

El orden en que se ejecutan los accesos ROV superpuestos de las invocaciones del sombreador de píxeles es idéntico al orden en el que se envía la geometría. Esto significa que, para las invocaciones del sombreador de píxeles superpuestos, las escrituras de ROV realizadas por una invocación del sombreador de píxeles deben estar disponibles para ser leídas por una invocación posterior y no deben afectar a las lecturas realizadas por una invocación anterior. Las lecturas de ROV realizadas por una invocación del sombreador de píxeles deben reflejar las escrituras realizadas por una invocación anterior y no deben reflejar las escrituras en una invocación posterior. Esto es importante para UAVs porque se omiten explícitamente en las garantías de invarianza de salida establecidas normalmente por el orden fijo de los resultados de la canalización de gráficos.

## <a name="implementation-details"></a>Detalles de la implementación

Las vistas ordenadas de rasterizador (ROVs) se declaran con los siguientes objetos del lenguaje HLSL (High Level Shader Language) y solo están disponibles para el sombreador de píxeles:

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

Utilice estos objetos de la misma manera que otros objetos UAV (como, por ejemplo, `RWBuffer` etc.).

## <a name="api-summary"></a>API summary

ROVs son una construcción solo HLSL que aplica una semántica de comportamiento diferente a UAVs. Todas las API relevantes para UAVs también son relevantes para ROVs. Tenga en cuenta que el siguiente método, las estructuras y la clase auxiliar hacen referencia al rasterizador:

-   [**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estructura que contiene la descripción del rasterizador, anotando la \_ \_ clase auxiliar CD3D12 de rasterizador DESC2 para crear descripciones de rasterizador.
-   [**D3D11 \_ \_Data Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estructura que contiene el valor booleano `ROVsSupported` , que indica la compatibilidad.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para tener acceso a las características admitidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 