---
description: La canalización programable de Direct3D 10 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En el diagrama siguiente se muestra el flujo de datos de la entrada a la salida a través de cada una de las fases programables.
ms.assetid: 3ead6c7c-c7cc-48f1-81d5-b4b67326d610
title: Fases de canalización (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bf6e904051fcac255a5bf1b99ca0f7d43ca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153015"
---
# <a name="pipeline-stages-direct3d-10"></a>Fases de canalización (Direct3D 10)

La canalización programable de Direct3D 10 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En el diagrama siguiente se muestra el flujo de datos de la entrada a la salida a través de cada una de las fases programables.

![diagrama del flujo de datos en la canalización programable de Direct3D 10](images/d3d10-pipeline-stages.png)

Todas las fases se pueden configurar mediante la API. Las fases que incluyen núcleos de sombreador comunes (los bloques rectangulares redondeados) se pueden programar mediante el lenguaje de programación HLSL. Como verá, esto hace que la canalización sea extremadamente flexible y adaptable. A continuación se muestra el propósito de cada una de las fases.

-   [Fase de ensamblado de entrada](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) : la etapa del ensamblador de entrada es responsable de proporcionar datos (triángulos, líneas y puntos) a la canalización.
-   [Fase del sombreador de vértices](https://www.bing.com/search?q=Vertex-Shader+Stage). Esta fase procesa vértices, normalmente realizando ciertas operaciones, como transformar, enmascarar e iluminar. Un sombreador de vértices siempre toma un solo vértice de entrada y produce un solo vértice de salida.
-   [Fase de sombreador de geometría](https://www.bing.com/search?q=Geometry-Shader+Stage) : la fase de sombreador de geometría procesa los primitivos completos. Su entrada es un primitivo completo (que es tres vértices para un triángulo, dos vértices para una línea o un solo vértice para un punto). Además, cada primitiva también puede incluir los datos de vértices para cualquier primitivo adyacente perimetral. Esto podría incluir como máximo tres vértices adicionales para un triángulo o dos vértices adicionales para una línea. El sombreador de geometría también admite amplificación y desamplificación de geometría limitada. Dado un primitivo de entrada, el sombreador de geometría puede descartar la primitiva o emitir una o más primitivas nuevas.
-   [Fase de flujo de salida](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md) : la fase de salida de flujo está diseñada para el streaming de datos primitivos de la canalización a la memoria en su camino al rasterizador. Los datos pueden transmitirse o pasarse al rasterizador. Los datos trasmitidos a la memoria pueden regresar a la canalización como datos de entrada o volver a leerse en la CPU.
-   [Fase de rasterización](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md) : el rasterizador es responsable de recortar los primitivos, preparar los primitivos para el sombreador de píxeles y determinar cómo invocar los sombreadores de píxeles.
-   [Fase del sombreador de píxeles](https://www.bing.com/search?q=Pixel-Shader+Stage): La fase del sombreador de píxeles recibe datos interpolados para un primitivo y genera datos por píxel, como el color.
-   [Fase de combinación de salida](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) : la fase de combinación de salida es responsable de combinar varios tipos de datos de salida (valores del sombreador de píxeles, información de profundidad y de estarcido) con el contenido de los búferes de destino de representación y de profundidad y estarcido para generar el resultado final de la canalización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
