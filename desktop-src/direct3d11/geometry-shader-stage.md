---
title: Fase del sombreador de geometría
description: La fase geometry-shader (GS) ejecuta código de sombreador especificado por la aplicación con vértices como entrada y la capacidad de generar vértices en la salida.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3099ed5ede8dd89dc607ed838ff6e3fabfb16a69
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335369"
---
# <a name="geometry-shader-stage"></a>Fase del sombreador de geometría

La fase geometry-shader (GS) ejecuta código de sombreador especificado por la aplicación con vértices como entrada y la capacidad de generar vértices en la salida.

## <a name="the-geometry-shader"></a>Sombreador de geometría

A diferencia de los sombreadores de vértices, que funcionan en un solo vértice, las entradas del sombreador de geometría son los vértices de una primitiva completa (dos vértices para líneas, tres vértices para triángulos o un solo vértice para el punto). Los sombreadores de geometría también pueden aportar los datos de vértice para las primitivas adyacentes al borde como entrada (dos vértices adicionales para una línea, tres adicionales para un triángulo). En la ilustración siguiente se muestra un triángulo y una línea con vértices adyacentes.

![ilustración de un triángulo y una línea con vértices adyacentes](images/d3d10-gs.png)

|     | Tipo                |
|-----|-----------------|
| **TV**  | Vértice de triángulo |
| **Av**  | Vértice adyacente |
| **Lv**  | Vértice de línea     |



 

La fase del sombreador de geometría puede consumir el valor generado por el sistema de SV PrimitiveID generado \_ automáticamente por el IA. [](d3d10-graphics-programming-guide-input-assembler-stage-using.md) Esto permite que los datos por primitivos se puedan capturar o calcular si se desea.

La fase del sombreador de geometría es capaz de generar varios vértices que forman una única topología seleccionada (las topologías de salida de la fase GS disponibles son: tristrip, linestrip y pointlist). El número de primitivas emitidas puede variar libremente dentro de cualquier invocación del sombreador de geometría, aunque el número máximo de vértices que se podrían emitir debe declararse estáticamente. Las longitudes de bandas emitidas a partir de una invocación del sombreador de geometría pueden ser arbitrarias y se pueden crear nuevas franjas a través de la [función RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL.

La salida del sombreador de geometría se puede alimentar a la fase del rasterizador o a un búfer de vértices en memoria a través de la fase de salida del flujo. La salida que se introduce en la memoria se expande a listas individuales de punto, línea o triángulo (exactamente como se pasarían al rasterizador).

Cuando un sombreador de geometría está activo, se invoca una vez para cada primitiva pasada o generada anteriormente en la canalización. Cada invocación del sombreador de geometría ve como entrada los datos de la primitiva de invocación, ya sea un único punto, una sola línea o un solo triángulo. Una franja de triángulos anterior en la canalización daría como resultado una invocación del sombreador de geometría para cada triángulo individual de la franja (como si la franja se expande hacia fuera en una lista de triángulos). Todos los datos de entrada de cada vértice de la primitiva individual están disponibles (es decir, 3 vértices para triángulo), además de los datos de vértice adyacentes si procede o están disponibles.

Un sombreador de geometría genera datos de un vértice a la vez anexando vértices a un objeto de flujo de salida. La topología de las secuencias viene determinada por una declaración fija, eligiendo una de las siguientes opciones: PointStream, LineStream o TriangleStream como salida de la fase GS. Hay tres tipos de objetos de secuencia disponibles: PointStream, LineStream y TriangleStream, que son objetos con plantilla. La topología de la salida viene determinada por su tipo de objeto respectivo, mientras que el formato de los vértices anexados a la secuencia viene determinado por el tipo de plantilla. La ejecución de una instancia del sombreador de geometría es atómica a partir de otras invocaciones, salvo que los datos agregados a las secuencias están en serie. Las salidas de una invocación determinada de un sombreador de geometría son independientes de otras invocaciones (aunque se respeta la ordenación). Un sombreador de geometría que genera franjas de triángulo iniciará una nueva franja en cada invocación.

Cuando una salida del sombreador de geometría se identifica como un valor interpretado por el sistema (por ejemplo, SV RenderTargetArrayIndex o SV Position), el hardware examina estos datos y realiza algún comportamiento dependiente del valor, además de poder pasar los propios datos a la siguiente fase del sombreador para la \_ \_ entrada. Cuando la salida de estos datos del sombreador de geometría tiene significado para el hardware por primitiva (como SV RenderTargetArrayIndex o SV ViewportArrayIndex), en lugar de por vértice \_ \_ (como SV ClipDistance n o SV Position), los datos por primitivo se toman del vértice inicial emitido \_ \[ para la \] \_ primitiva.

El sombreador de geometría podría generar primitivas parcialmente completadas si el sombreador de geometría finaliza y la primitiva está incompleta. Las primitivas incompletas se descartan silenciosamente. Esto es similar a la manera en que el IA trata las primitivas parcialmente completadas.

El sombreador de geometría puede realizar operaciones de muestreo de carga y textura donde no se requieren derivados del espacio de pantalla (samplelevel, samplecmplevelzero, samplegrad).

Los algoritmos que se pueden implementar en el sombreador de geometría incluyen:

-   Expansión de sprite de punto
-   Sistemas de partícula dinámica
-   Generación de pectoral/fin
-   Generación de volúmenes de sombra
-   Mapa de representación a cubo de paso único
-   Per-Primitive intercambio de material
-   Per-Primitive configuración de material: incluida la generación de coordenadas baricéntricas como datos primitivos para que un sombreador de píxeles pueda realizar la interpolación de atributos personalizados (para obtener un ejemplo de interpolación normal de orden superior, vea [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 