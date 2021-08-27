---
description: La canalización programable direct3D 10 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En el diagrama siguiente se muestra el flujo de datos de entrada a salida a través de cada una de las fases programables.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Fases de canalización (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942e2594f1f2eeb83f92b3ee517804a68b6074d85bf5c9205828a08e024112df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119985"
---
# <a name="pipeline-stages-direct3d-10"></a>Fases de canalización (Direct3D 10)

La canalización programable direct3D 10 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En el diagrama siguiente se muestra el flujo de datos de entrada a salida a través de cada una de las fases programables.

![diagrama del flujo de datos en la canalización programable direct3d 10](images/d3d10-pipeline-stages.png)

Todas las fases se pueden configurar mediante la API. Las fases que presentan núcleos comunes de sombreador (los bloques rectangulares redondeados) se pueden programar mediante el lenguaje de programación HLSL. Como verá, esto hace que la canalización sea extremadamente flexible y adaptable. A continuación se muestra el propósito de cada una de las fases.

-   [Fase de ensamblador de entrada:](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) la fase de ensamblador de entrada es responsable de proporcionar datos (triángulos, líneas y puntos) a la canalización.
-   [Fase del sombreador de vértices](https://www.bing.com/search?q=Vertex-Shader+Stage). Esta fase procesa vértices, normalmente realizando ciertas operaciones, como transformar, enmascarar e iluminar. Un sombreador de vértices siempre toma un solo vértice de entrada y produce un solo vértice de salida.
-   [Fase de sombreador de geometría:](https://www.bing.com/search?q=Geometry-Shader+Stage) la fase del sombreador de geometría procesa primitivas enteras. Su entrada es una primitiva completa (que es tres vértices para un triángulo, dos vértices para una línea o un solo vértice para un punto). Además, cada primitiva también puede incluir los datos de vértices de cualquier primitiva adyacente al borde. Esto podría incluir como máximo tres vértices adicionales para un triángulo o dos vértices adicionales para una línea. El sombreador de geometría también admite la amplificación y desamplificación de geometría limitadas. Dado un primitivo de entrada, el sombreador de geometría puede descartar la primitiva o emitir una o varias primitivas nuevas.
-   [Fase stream-output:](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) la fase stream-output está diseñada para transmitir datos primitivos de la canalización a la memoria en su camino al rasterizador. Los datos pueden transmitirse o pasarse al rasterizador. Los datos trasmitidos a la memoria pueden regresar a la canalización como datos de entrada o volver a leerse en la CPU.
-   [Fase de rasterizador:](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) el rasterizador es responsable de recortar primitivas, preparar primitivas para el sombreador de píxeles y determinar cómo invocar sombreadores de píxeles.
-   [Fase del sombreador de píxeles](https://www.bing.com/search?q=Pixel-Shader+Stage): La fase del sombreador de píxeles recibe datos interpolados para un primitivo y genera datos por píxel, como el color.
-   [Fase de](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) fusión de salida: la fase de fusión de salida es responsable de combinar varios tipos de datos de salida (valores de sombreador de píxeles, información de profundidad y galería de símbolos) con el contenido del destino de representación y los búferes de profundidad/galería de símbolos para generar el resultado final de la canalización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
