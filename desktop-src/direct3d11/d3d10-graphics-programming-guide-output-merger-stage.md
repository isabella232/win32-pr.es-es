---
title: Output-Merger fase
description: La fase de combinación de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxeles generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad/estarcido.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- fase de fusión de salida (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec77eaff506a0be87a3f0e98de691b50c27c0c3f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421629"
---
# <a name="output-merger-stage"></a>Output-Merger fase

La fase de combinación de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxeles generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad/estarcido. La fase OM es el último paso para determinar qué píxeles son visibles (con pruebas de la galería de símbolos de profundidad) y mezclar los colores finales de los píxeles.



|                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10: Direct3D 9 implementa las pruebas alfa (mediante [el estado de pruebas alfa](/windows/desktop/direct3d9/alpha-testing-state)) para controlar si un píxel se escribe en un destino de representación de salida.<br/> Direct3D 10 y versiones posteriores no implementan una prueba alfa (o el estado de la prueba alfa). Esto se puede controlar mediante un sombreador de píxeles o con la funcionalidad de profundidad/estarcido.<br/> |



 

## <a name="depth-stencil-testing-overview"></a>Información general sobre pruebas de Depth-Stencil

Un búfer de estarcido de profundidad, que se crea como un recurso de textura, puede contener datos de profundidad y datos de estarcido. Los datos de profundidad se usan para determinar qué píxeles se encuentran más cerca de la cámara, y los datos de la galería de símbolos se usan para enmascarar los píxeles que se pueden actualizar. En última instancia, la fase de combinación de resultados utiliza los datos de los valores Depth y stencil para determinar si se debe dibujar un píxel. En el diagrama siguiente se muestra conceptualmente cómo se realizan las pruebas de profundidad de la galería de símbolos.

![diagrama de cómo funciona la prueba de profundidad-estarcido](images/d3d10-depth-stencil-test.png)

Para configurar las pruebas de profundidad y estarcido, consulte Configuración de la [funcionalidad de Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md). Un objeto de galería de símbolos de profundidad encapsula el estado de la galería de símbolos de profundidad. Una aplicación puede especificar el estado de la galería de símbolos de profundidad o la fase OM usará los valores predeterminados. Las operaciones de combinación se realizan por píxel si el muestreo múltiple está deshabilitado. Si el muestreo múltiple está habilitado, la fusión se produce en cada muestreo.

El proceso de usar el búfer de profundidad para determinar qué píxel se debe dibujar se denomina almacenamiento en búfer de profundidad, también denominado almacenamiento en búfer z.

Una vez que los valores de profundidad llegan a la fase de fusión de salida (ya sea desde la interpolación o desde un sombreador de píxeles), siempre están fijados: z = min (viewport. MaxDepth, Max (viewport. MinDepth, z)) según el formato y la precisión del búfer de profundidad, mediante reglas de punto flotante. Después de la compresión, se compara el valor de profundidad (mediante DepthFunc) con el valor de búfer de profundidad existente. Si no se enlaza ningún búfer de profundidad, la prueba de profundidad siempre se supera.

Si no hay ningún componente de estarcido en el formato de búfer de profundidad o no hay ningún límite de búfer de profundidad, la prueba de estarcido siempre pasa. De lo contrario, la funcionalidad no cambia de Direct3D 9.

Solo un búfer de profundidad/estarcido puede estar activo a la vez; cualquier vista de recursos enlazada debe coincidir con la vista de profundidad/estarcido (el mismo tamaño y dimensiones). Esto no significa que el tamaño del recurso debe coincidir, solo que el tamaño de la vista debe coincidir.

Para obtener más información sobre las pruebas de la galería de símbolos de profundidad, vea el [tutorial 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Información general de blending

La mezcla combina uno o más valores de píxeles para crear un color de píxel final. En el diagrama siguiente se muestra el proceso implicado en la combinación de datos de píxeles.

![diagrama de cómo funciona la fusión de datos](images/d3d10-blend-state.png)

Desde el punto de vista conceptual, puede visualizar este diagrama de flujo implementado dos veces en la fase de combinación de salida: el primero de ellos combina los datos RGB, mientras que en paralelo, un segundo combina los datos alfa. Para ver cómo usar la API para crear y establecer el estado de Blend, consulte Configuración de la [funcionalidad de fusión](d3d10-graphics-programming-guide-blend-state.md).

La mezcla de funciones fijas se puede habilitar de forma independiente para cada destino de representación. Sin embargo, solo hay un conjunto de controles de Blend, de modo que la misma mezcla se aplica a todos los RenderTargets con la fusión mediante combinación habilitada. Los valores de Blend (incluido BlendFactor) siempre se fijan en el intervalo del formato de destino de representación antes de la fusión. La compresión se realiza por destino de representación, respetando el tipo de destino de representación. La única excepción son los formatos float16, float11 o float10 que no están fijados, por lo que las operaciones de mezcla en estos formatos se pueden realizar con al menos la misma precisión/intervalo que el formato de salida. Los NaN y los ceros con signo se propagan para todos los casos (incluidos los pesos de 0,0 Blend).

Cuando se utilizan destinos de representación sRGB, el tiempo de ejecución convierte el color del destino de representación en un espacio lineal antes de realizar la fusión. El tiempo de ejecución convierte de nuevo el valor de fusión final en el espacio sRGB antes de guardar el valor en el destino de representación.



|                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10: en Direct3D 9, la combinación de funciones fijas se puede habilitar de forma independiente para cada destino de representación.<br/> En Direct3D 10 y versiones posteriores, hay una descripción de estado de Blend; por lo tanto, se puede establecer un valor de mezcla para todos los destinos de representación.<br/> |



 

### <a name="dual-source-color-blending"></a>Dual-Source la combinación de colores

Esta característica permite a la fase de combinación de salida usar simultáneamente ambas salidas de sombreador de píxeles (O0 y O1) como entradas para una operación de combinación con el destino de representación único en la ranura 0. Entre las operaciones de mezcla válidas se incluyen: Add, Retract y revsubtract. Entre las opciones de Blend válidas para SrcBlend, DestBlend, SrcBlendAlpha o DestBlendAlpha se incluyen: **D3D11 \_ Blend \_ SRC1 \_ color**, **D3D11 \_ Blend \_ INV \_ SRC1 \_ color**, **D3D11 \_ Blend \_ SRC1 \_ Alpha**, **D3D11 \_ Blend \_ INV \_ SRC1 \_ Alpha**. La ecuación de Blend y la máscara de escritura de salida especifican qué componentes está generando el sombreador de píxeles. Se omiten los componentes adicionales.

La escritura en otras salidas del sombreador de píxeles (O2, O3 etc.) no está definida. no se puede escribir en un destino de representación si no está enlazado a la ranura 0. La escritura de oDepth es válida durante la combinación de colores de origen dual.

Para obtener ejemplos, consulte [blending Pixel Shader Outputs](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Información general sobre varios RenderTargets

Un sombreador de píxeles se puede usar para representar al menos 8 destinos de representación independientes, todos ellos deben ser del mismo tipo (buffer, Texture1D, Texture1DArray, etc.). Además, todos los destinos de representación deben tener el mismo tamaño en todas las dimensiones (ancho, alto, profundidad, tamaño de la matriz, recuentos de muestras). Cada destino de representación puede tener un formato de datos diferente.

Puede usar cualquier combinación de ranuras de destinos de representación (hasta 8). Sin embargo, una vista de recursos no se puede enlazar a varias ranuras de destino de representación simultáneamente. Una vista se puede volver A usar siempre que los recursos no se usen simultáneamente.

## <a name="output-write-mask-overview"></a>Información general de la máscara de Output-Write

Use una máscara de salida-escritura para controlar (por componente) Qué datos se pueden escribir en un destino de representación.

## <a name="sample-mask-overview"></a>Información general de la máscara de ejemplo

Una máscara de ejemplo es una máscara de cobertura Multimuestra de 32 bits que determina qué muestras se actualizan en los destinos de representación activos. Solo se permite una máscara de ejemplo. El usuario define la asignación de bits en una máscara de ejemplo a los ejemplos de un recurso. En la representación de n-Sample, se usan los primeros n bits (del LSB) de la máscara de ejemplo (32 bits es el número máximo de bits).


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                    | Descripción                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuración de la funcionalidad de Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | En esta sección se explican los pasos para configurar el búfer de estarcido de profundidad y el estado de la galería de símbolos de profundidad para la fase de combinación de salida.<br/>                                                                                                                           |
| [Configuración de la funcionalidad de fusión](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Las operaciones de combinación se realizan en cada salida del sombreador de píxeles (valor RGBA) antes de que el valor de salida se escriba en un destino de representación. Si el muestreo múltiple está habilitado, la combinación se realiza en cada muestreo múltiple; de lo contrario, se realiza la combinación en cada píxel.<br/> |
| [Tendencia de profundidad](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando un sesgo z (o una diferencia de profundidad) a cada uno de ellos.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

