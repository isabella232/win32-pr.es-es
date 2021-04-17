---
description: En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado, lo que reduce en gran medida el costo de los cambios de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705259"
---
# <a name="state-objects-direct3d-10"></a>Objetos de estado (Direct3D 10)

En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado, lo que reduce en gran medida el costo de los cambios de estado. Hay varios objetos de estado y cada uno está diseñado para inicializar un conjunto de estado para una fase de canalización determinada. Puede crear hasta 4096 de cada tipo de objeto de estado.

-   [Estado de diseño de entrada](#input-layout-state)
-   [Estado del rasterizador](#rasterizer-state)
-   [Profundidad: estado de estarcido](#depth-stencil-state)
-   [Estado de Blend](#blend-state)
-   [Estado de muestra](#sampler-state)
-   [Consideraciones de rendimiento](#performance-considerations)
-   [Temas relacionados](#related-topics)

## <a name="input-layout-state"></a>Estado de Input-Layout

Este grupo de estado (vea [**la \_ \_ \_ Descripción del elemento de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina cómo la fase del [ensamblador de entrada](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Lee los datos fuera de los búferes de entrada y los ensambla para que los use el sombreador de vértices. Esto incluye el estado como el número de elementos en el búfer de entrada y la firma de los datos de entrada. La fase de ensamblador de entrada es una nueva fase de la canalización cuyo trabajo es transmitir los primitivos de la memoria a la canalización.

Para crear un objeto de estado de diseño de entrada, vea [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Estado del rasterizador

Este grupo de estado (consulte [**D3D10 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) inicializa la [fase de rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Este objeto incluye el estado, como los modos de relleno o de selección, habilitando un rectángulo de recorte en tijera y estableciendo parámetros de ejemplo múltiples. Esta fase rasteriza los primitivos en píxeles y realiza operaciones como el recorte y la asignación de primitivos a la ventanilla.

Para crear un objeto de estado de rasterizador, vea [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).

## <a name="depth-stencil-state"></a>Estado de Depth-Stencil

Este grupo de estado (consulte [**D3D10 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) inicializa la parte de la galería de símbolos de profundidad de la [fase de combinación de resultados](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md). Más concretamente, este objeto inicializa las pruebas de profundidad y de estarcido.

Para crear un objeto de estado de galería de símbolos de profundidad, vea [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).

## <a name="blend-state"></a>Estado de Blend

Este grupo de estado (vea [**D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) inicializa la parte de mezcla de la [fase de combinación de salida](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).

Para crear un objeto de estado de Blend, vea [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>Estado de muestra

Este grupo de estado (vea [**D3D10 \_ muestra \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) inicializa un objeto de muestra. Las fases del sombreador usan un objeto de muestra para filtrar las texturas en memoria.



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 10, el objeto de muestra ya no está enlazado a una textura específica; simplemente describe cómo realizar el filtrado dado cualquier recurso asociado. |



 

Para crear un objeto de estado de muestra, vea [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).

## <a name="performance-considerations"></a>Consideraciones de rendimiento

El diseño de la API para usar objetos de estado crea varias ventajas de rendimiento. Incluyen la validación del estado en el momento de la creación del objeto, la habilitación del almacenamiento en caché de objetos de estado en hardware y la reducción en gran medida de la cantidad de estado que se pasa durante una llamada de API de configuración de estado (pasando un identificador al objeto de estado en lugar del estado).

Para lograr estas mejoras de rendimiento, debe crear los objetos de estado cuando la aplicación se inicia, bien antes del bucle de representación. Los objetos de estado son inmutables, es decir, una vez que se crean, no se pueden cambiar. En su lugar, debe destruirlos y volver a crearlos. Para hacer frente a esta restricción, puede crear hasta 4096 de cada tipo de objetos de estado. Por ejemplo, podría crear varios objetos de muestra con varias combinaciones de estado de muestra. El cambio del estado de la muestra se realiza mediante una llamada a la API de conjunto adecuada que pasa un identificador al objeto (en contraposición al estado de muestra). Esto reduce considerablemente la cantidad de sobrecarga durante cada fotograma de representación para cambiar el estado, ya que el número de llamadas y la cantidad de datos se reducen considerablemente.

Como alternativa, puede optar por usar el sistema de efectos, que administrará automáticamente la creación y destrucción eficientes de los objetos de estado de la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de la API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
