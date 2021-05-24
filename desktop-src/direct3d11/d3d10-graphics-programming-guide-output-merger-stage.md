---
title: Output-Merger fase
description: La fase de fusión de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxel generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad o galería de símbolos.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- fase de fusión de salida (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8de2851fdea3a22cc42033d2c13454be72ba8ab
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335219"
---
# <a name="output-merger-stage"></a>Output-Merger fase

La fase de fusión de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxel generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad o galería de símbolos. La fase OM es el paso final para determinar qué píxeles son visibles (con pruebas de galería de símbolos de profundidad) y combinar los colores de píxeles finales.



Diferencias entre Direct3D 9 y Direct3D 10:

- Direct3D 9 implementa pruebas alfa (mediante el estado de prueba [alfa)](/windows/desktop/direct3d9/alpha-testing-state)para controlar si un píxel se escribe en un destino de representación de salida.
- Direct3D 10 y superior no implementa una prueba alfa (o estado de prueba alfa). Esto se puede controlar mediante un sombreador de píxeles o con la funcionalidad de profundidad o galería de símbolos.



 

## <a name="depth-stencil-testing-overview"></a>Depth-Stencil de pruebas

Un búfer de galería de símbolos de profundidad, que se crea como un recurso de textura, puede contener datos de profundidad y datos de galería de símbolos. Los datos de profundidad se usan para determinar qué píxeles se encuentran más cerca de la cámara y los datos de galería de símbolos se usan para enmascarar los píxeles que se pueden actualizar. En última instancia, la fase de fusión de salida usa los datos de los valores de profundidad y galería de símbolos para determinar si se debe dibujar o no un píxel. En el diagrama siguiente se muestra conceptualmente cómo se realizan las pruebas de galería de símbolos de profundidad.

![diagrama de cómo funcionan las pruebas de galería de símbolos de profundidad](images/d3d10-depth-stencil-test.png)

Para configurar las pruebas de galería de símbolos de profundidad, vea [Configuring Depth-Stencil Functionality](d3d10-graphics-programming-guide-depth-stencil.md). Un objeto depth-stencil encapsula el estado de la galería de símbolos de profundidad. Una aplicación puede especificar el estado de galería de símbolos de profundidad o la fase OM usará valores predeterminados. Las operaciones de combinación se realizan por píxel si el multimuestreo está deshabilitado. Si el multimuestreo está habilitado, la combinación se produce por muestreo múltiple.

El proceso de usar el búfer de profundidad para determinar qué píxel se debe dibujar se denomina almacenamiento en búfer de profundidad, también denominado búfer z.

Una vez que los valores de profundidad alcanzan la fase de fusión de salida (ya sea procedente de la interpolación o de un sombreador de píxeles), siempre se fijan: z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z)) según el formato o la precisión del búfer de profundidad, mediante reglas de punto flotante. Después de la fijación, el valor de profundidad se compara (mediante DepthFunc) con el valor de búfer de profundidad existente. Si no hay ningún búfer de profundidad enlazado, siempre se supera la prueba de profundidad.

Si no hay ningún componente de galería de símbolos en el formato de búfer de profundidad o no hay ningún búfer de profundidad enlazado, siempre se supera la prueba de galería de símbolos. De lo contrario, la funcionalidad no se modifica desde Direct3D 9.

Solo un búfer de profundidad o galería de símbolos puede estar activo a la vez; cualquier vista de recursos enlazado debe coincidir (con el mismo tamaño y dimensiones) con la vista de profundidad o galería de símbolos. Esto no significa que el tamaño del recurso debe coincidir, solo que el tamaño de la vista debe coincidir.

Para obtener más información sobre las pruebas de galería de símbolos de profundidad, [vea el tutorial 14.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)

## <a name="blending-overview"></a>Información general sobre la combinación

La combinación combina uno o varios valores de píxel para crear un color de píxel final. En el diagrama siguiente se muestra el proceso implicado en la combinación de datos de píxeles.

![diagrama de cómo funciona la combinación de datos](images/d3d10-blend-state.png)

Conceptualmente, puede visualizar este gráfico de flujo implementado dos veces en la fase de fusión de salida: el primero combina datos RGB, mientras que en paralelo, otro mezcla datos alfa. Para ver cómo usar la API para crear y establecer el estado de blend, consulte [Configuring Blending Functionality](d3d10-graphics-programming-guide-blend-state.md).

La combinación de función fija se puede habilitar de forma independiente para cada destino de representación. Sin embargo, solo hay un conjunto de controles blend, por lo que la misma combinación se aplica a todos los RenderTargets con la combinación habilitada. Los valores de Blend (incluido BlendFactor) siempre se fijan al intervalo del formato de destino de representación antes de la combinación. La fijación se realiza por destino de representación, respetando el tipo de destino de representación. La única excepción es para los formatos float16, float11 o float10 que no están fijas para que las operaciones de combinación en estos formatos se puedan realizar con al menos la misma precisión o intervalo que el formato de salida. Los naN y los ceros con firma se propagan para todos los casos (incluidos 0,0 pesos de mezcla).

Cuando se usan destinos de representación sRGB, el tiempo de ejecución convierte el color del destino de representación en espacio lineal antes de realizar la mezcla. El tiempo de ejecución vuelve a convertir el valor combinado final en espacio sRGB antes de volver a guardar el valor en el destino de representación.

Diferencias entre Direct3D 9 y Direct3D 10:

- En Direct3D 9, la combinación de funciones fijas se puede habilitar de forma independiente para cada destino de representación.
- En Direct3D 10 y posteriores, hay una descripción de estado de mezcla; por lo tanto, se puede establecer un valor de combinación para todos los destinos de representación.



 

### <a name="dual-source-color-blending"></a>Dual-Source combinación de colores

Esta característica permite que la fase de fusión de salida use simultáneamente ambas salidas del sombreador de píxeles (o0 y o1) como entradas para una operación de mezcla con el destino de representación única en la ranura 0. Las operaciones de blend válidas incluyen: sumar, restar y revsubtract. Las opciones de mezcla válidas para SrcBlend, DestBlend, SrcBlendAlpha o DestBlendAlpha incluyen: **D3D11 \_ BLEND \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ INV \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ SRC1 \_ ALPHA**, **D3D11 \_ BLEND \_ INV \_ SRC1 \_ ALPHA**. La ecuación de mezcla y la máscara de escritura de salida especifican qué componentes genera el sombreador de píxeles. Se omiten los componentes adicionales.

Escribir en otras salidas del sombreador de píxeles (o2, o3, etc.) no está definida; No puede escribir en un destino de representación si no está enlazado a la ranura 0. Escribir oDepth es válido durante la combinación de colores de origen dual.

Para obtener ejemplos, vea [Combinar salidas de sombreador de píxeles.](d3d10-graphics-programming-guide-blend-state.md)

## <a name="multiple-rendertargets-overview"></a>Información general sobre varios elementos RenderTargets

Un sombreador de píxeles se puede usar para representar al menos 8 destinos de representación independientes, todos los cuales deben ser del mismo tipo (buffer, Texture1D, Texture1DArray, y así sucesivamente). Además, todos los destinos de representación deben tener el mismo tamaño en todas las dimensiones (ancho, alto, profundidad, tamaño de matriz, recuentos de muestras). Cada destino de representación puede tener un formato de datos diferente.

Puede usar cualquier combinación de ranuras de destinos de representación (hasta 8). Sin embargo, una vista de recursos no se puede enlazar a varias ranuras de destino de representación simultáneamente. Una vista se puede reutilizar siempre que los recursos no se utilicen simultáneamente.

## <a name="output-write-mask-overview"></a>Output-Write información general sobre la máscara de máscara

Use una máscara de salida y escritura para controlar (por componente) qué datos se pueden escribir en un destino de representación.

## <a name="sample-mask-overview"></a>Información general sobre máscaras de ejemplo

Una máscara de ejemplo es una máscara de cobertura de varios ejemplos de 32 bits que determina qué muestras se actualizan en destinos de representación activos. Solo se permite una máscara de ejemplo. Un usuario define la asignación de bits de una máscara de ejemplo a los ejemplos de un recurso. Para la representación de n muestras, se usan los primeros n bits (del LSB) de la máscara de muestra (32 bits es el número máximo de bits).


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                    | Descripción                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración de Depth-Stencil funcionalidad](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | En esta sección se tratan los pasos para configurar el búfer de galería de símbolos de profundidad y el estado de la galería de símbolos de profundidad para la fase de fusión de salida.<br/>                                                                                                                           |
| [Configuración de la funcionalidad de mezcla](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación. Si se habilita el multimuestreo, la combinación se realiza en cada multimuestreo. De lo contrario, la combinación se realiza en cada píxel.<br/> |
| [Sesgo de profundidad](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Los polígonos que son coplanares en el espacio 3D pueden aparecer como si no fuera coplanar agregando un sesgo z (o sesgo de profundidad) a cada uno de ellos.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

