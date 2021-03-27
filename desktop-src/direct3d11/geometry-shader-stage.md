---
title: Fase del sombreador de geometría
description: La fase del sombreador de geometría (GS) ejecuta código de sombreador especificado por la aplicación con los vértices como entrada y la capacidad de generar vértices en la salida.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da66b1e3f9abf4e7db8010887f3e78676d02a874
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792441"
---
# <a name="geometry-shader-stage"></a>Fase del sombreador de geometría

La fase del sombreador de geometría (GS) ejecuta código de sombreador especificado por la aplicación con los vértices como entrada y la capacidad de generar vértices en la salida.

## <a name="the-geometry-shader"></a>Sombreador de geometría

A diferencia de los sombreadores de vértices, que operan en un solo vértice, las entradas del sombreador de geometría son los vértices de un primitivo completo (dos vértices para las líneas, tres vértices para triángulos o un solo vértice para el punto). Los sombreadores de geometría también pueden traer los datos de vértices de los primitivos adyacentes perimetrales como entrada (dos vértices adicionales para una línea, tres más para un triángulo). En la ilustración siguiente se muestra un triángulo y una línea con vértices adyacentes.

![Ilustración de un triángulo y una línea con vértices adyacentes](images/d3d10-gs.png)

|     |                 |
|-----|-----------------|
| TV  | Vértice de triángulo |
| AV  | Vértice adyacente |
| LV  | Vértice de línea     |



 

La fase del sombreador de geometría puede consumir el \_ valor de VP PrimitiveID generado por el [sistema](d3d10-graphics-programming-guide-input-assembler-stage-using.md) que genera automáticamente el IA. Esto permite capturar o calcular los datos por primitivos si se desea.

La fase de sombreador de geometría es capaz de generar varios vértices que formen una sola topología seleccionada (las topologías de salida de fase GS disponibles son: tristripe, linestrip y PointList). El número de primitivas emitidas puede variar libremente dentro de cualquier invocación del sombreador de geometría, aunque el número máximo de vértices que podrían emitirse se debe declarar de forma estática. Las longitudes de franjas emitidas desde una invocación del sombreador de geometría pueden ser arbitrarias y se pueden crear nuevas bandas a través de la función HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) .

La salida del sombreador de geometría se puede alimentar a la fase de rasterizador o a un búfer de vértice en la memoria a través de la fase de salida de flujo. La salida introducida en la memoria se expande a listas de puntos, líneas y triángulos individuales (exactamente como se pasarían al rasterizador).

Cuando un sombreador de geometría está activo, se invoca una vez para cada primitiva que se pasa o se genera anteriormente en la canalización. Cada invocación del sombreador de geometría ve como entrada los datos para la invocación de primitivos, ya sea un único punto, una sola línea o un solo triángulo. Una franja de triángulos anterior en la canalización produciría una invocación del sombreador de geometría para cada triángulo individual de la franja (como si la franja estuviera expandida en una lista de triángulos). Todos los datos de entrada para cada vértice de la primitiva individual están disponibles (es decir, 3 vértices para el triángulo), además de los datos de vértice adyacentes, si procede o está disponible.

Un sombreador de geometría genera datos de un vértice a la vez anexando vértices a un objeto de flujo de salida. La topología de las secuencias viene determinada por una declaración fija, eligiendo uno de los siguientes: PointStream, LineStream o TriangleStream como salida de la fase GS. Hay tres tipos de objetos de secuencia disponibles, PointStream, LineStream y TriangleStream, que son todos los objetos con plantilla. La topología de la salida viene determinada por su tipo de objeto respectivo, mientras que el formato de los vértices anexados a la secuencia viene determinado por el tipo de plantilla. La ejecución de una instancia del sombreador de geometría es atómica desde otras invocaciones, salvo que los datos que se agregan a los flujos son serie. Las salidas de una invocación determinada de un sombreador de geometría son independientes de otras invocaciones (aunque se respeta la ordenación). Un sombreador de geometría que genera bandas triángulos iniciará una nueva franja en cada invocación.

Cuando una salida del sombreador de geometría se identifica como un valor interpretado por el sistema (por ejemplo, la \_ posición VP RenderTargetArrayIndex o VP \_ ), el hardware examina estos datos y realiza algún comportamiento dependiente del valor, además de poder pasar los datos en la siguiente fase del sombreador para la entrada. Cuando dicha salida de datos del sombreador de geometría tiene significado para el hardware en función de la primitiva (como la VP \_ RenderTargetArrayIndex o la VP \_ ViewportArrayIndex), en lugar de un carácter por vértice (como la VP \_ ClipDistance \[ n \] o la \_ posición SV), los datos por primitivos se toman del vértice inicial emitido para el primitivo.

El sombreador de geometría puede generar primitivos parcialmente completados si el sombreador de geometría finaliza y el primitivo está incompleto. Los primitivos incompletos se descartan de forma silenciosa. Esto es similar a la forma en que el IA trata los primitivos parcialmente completados.

El sombreador de geometría puede realizar operaciones de muestreo de la carga y la textura en las que no se necesitan los derivados del espacio de pantalla (samplelevel, samplecmplevelzero, samplegrad).

Los algoritmos que se pueden implementar en el sombreador de geometría incluyen:

-   Expansión de Sprite de punto
-   Sistemas de partículas dinámicas
-   Generación de peletería/fin
-   Generación de volúmenes de instantáneas
-   Representación de un solo paso a mapa
-   Intercambio de materiales Per-Primitive
-   Configuración de Per-Primitive material: incluida la generación de coordenadas Barycentric como datos primitivos para que un sombreador de píxeles pueda realizar la interpolación de atributos personalizados (para obtener un ejemplo de interpolación normal de orden superior, vea [ejemplo de CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 