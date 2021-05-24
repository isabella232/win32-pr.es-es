---
description: En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado que reducen considerablemente el costo de los cambios de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335429"
---
# <a name="state-objects-direct3d-10"></a>Objetos de estado (Direct3D 10)

En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado que reducen considerablemente el costo de los cambios de estado. Hay varios objetos de estado y cada uno de ellos está diseñado para inicializar un conjunto de estado para una fase de canalización determinada. Puede crear hasta 4096 de cada tipo de objeto de estado.

-   [Estado de diseño de entrada](#input-layout-state)
-   [Estado del rasterizador](#rasterizer-state)
-   [Estado de galería de símbolos de profundidad](#depth-stencil-state)
-   [Estado de blend](#blend-state)
-   [Estado del muestreador](#sampler-state)
-   [Consideraciones de rendimiento](#performance-considerations)
-   [Temas relacionados](#related-topics)

## <a name="input-layout-state"></a>Input-Layout estado

Este grupo de estado (vea [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)determina cómo la fase del [ensamblador](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) de entrada lee los datos de los búferes de entrada y los ensambla para que los use el sombreador de vértices. Esto incluye el estado, como el número de elementos del búfer de entrada y la firma de los datos de entrada. La fase de ensamblador de entrada es una nueva fase de la canalización cuyo trabajo es transmitir primitivas de la memoria a la canalización.

Para crear un objeto input-layout-state, vea [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Estado del rasterizador

Este grupo de estado (consulte [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)inicializa la fase [del rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Este objeto incluye el estado, como los modos de relleno o cull, la habilitación de un rectángulo de recorte para el recorte y la configuración de parámetros multimuestreo. Esta fase rasteriza las primitivas en píxeles, realizando operaciones como el recorte y la asignación de primitivas a la ventanilla.

Para crear un objeto de estado de rasterizador, vea [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).

## <a name="depth-stencil-state"></a>Depth-Stencil estado

Este grupo de estado (vea [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)inicializa la parte de la galería de símbolos de profundidad de la fase de fusión [de salida.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) Más concretamente, este objeto inicializa las pruebas de profundidad y galería de símbolos.

Para crear un objeto depth-stencil-state, vea [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).

## <a name="blend-state"></a>Estado de blend

Este grupo de estado (vea [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)inicializa la parte de mezcla de la fase [de fusión de salida.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)

Para crear un objeto blend-state, vea [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>Estado del muestreador

Este grupo de estado (vea [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)inicializa un objeto sampler. Las fases del sombreador usan un objeto sampler para filtrar texturas en memoria.



Diferencias entre Direct3D 9 y Direct3D 10:

- En Direct3D 10, el objeto sampler ya no está enlazado a una textura específica, solo describe cómo realizar el filtrado dado cualquier recurso asociado.



 

Para crear un objeto sampler-state, vea [**CreateSamplerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)

## <a name="performance-considerations"></a>Consideraciones de rendimiento

El diseño de la API para usar objetos de estado crea varias ventajas de rendimiento. Esto incluye validar el estado en el momento de la creación del objeto, habilitar el almacenamiento en caché de objetos de estado en hardware y reducir en gran medida la cantidad de estado que se pasa durante una llamada API de configuración de estado (pasando un identificador al objeto de estado en lugar del estado).

Para lograr estas mejoras de rendimiento, debe crear los objetos de estado cuando se inicie la aplicación, justo antes del bucle de representación. Los objetos de estado son inmutables, es decir, una vez creados, no se pueden cambiar. En su lugar, debe destruirlos y volver a crearlos. Para hacer frente a esta restricción, puede crear hasta 4096 de cada tipo de objetos de estado. Por ejemplo, podría crear varios objetos sampler con varias combinaciones de estado de sampler. A continuación, el cambio del estado del muestreador se realiza mediante una llamada a la API Set adecuada que pasa un identificador al objeto (en lugar del estado del muestreador). Esto reduce significativamente la cantidad de sobrecarga durante cada fotograma de representación para cambiar el estado, ya que el número de llamadas y la cantidad de datos se reducen considerablemente.

Como alternativa, puede optar por usar el sistema de efectos que administrará automáticamente la creación eficaz y la destrucción de objetos de estado para la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
