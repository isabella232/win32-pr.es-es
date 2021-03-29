---
title: Canalización de gráficos
description: En esta sección se describe la canalización programable de Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8e6b0b4d249c46dafe960f4f25a9a7598d6e2c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421633"
---
# <a name="graphics-pipeline"></a>Canalización de gráficos

La canalización programable de Direct3D 11 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En esta sección se describe la canalización programable de Direct3D 11. En el diagrama siguiente se muestra el flujo de datos de la entrada a la salida a través de cada una de las fases programables.

![diagrama del flujo de datos en la canalización programable de Direct3D 11](images/d3d11-pipeline-stages.jpg)

La canalización de gráficos para Microsoft Direct3D 11 admite las mismas fases que la [canalización de gráficos de Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), con fases adicionales para admitir características avanzadas.

Puede usar el 11API de Direct3D para configurar todas las fases. Las fases que incluyen núcleos de sombreador comunes (los bloques rectangulares redondeados) se pueden programar mediante el lenguaje de programación [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) . Como verá, esto hace que la canalización sea extremadamente flexible y adaptable.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | La API de Direct3D 10 y versiones posteriores separa las áreas funcionales de la canalización en fases; la primera fase de la canalización es la fase del ensamblador de entrada (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Fase del sombreador de vértices](vertex-shader-stage.md)<br/>                                      | La fase del sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice, como transformaciones, máscaras, transformación y iluminación por vértice. Los sombreadores de vértices siempre operan en un solo vértice de entrada y producen un único vértice de salida. La fase del sombreador de vértices siempre debe estar activa para que se ejecute la canalización. Si no se requiere ninguna modificación o transformación de vértices, debe crearse un sombreador de vértices de paso a través y establecerse en la canalización.<br/> |
| [Fases de teselación](direct3d-11-advanced-stages-tessellation.md)<br/>                 | El tiempo de ejecución de Direct3D 11 admite tres nuevas fases que implementan Teselación, que convierte las superficies de subdivisiones de bajo detalle en primitivas más detalladas en la GPU. Mosaicos de teselación (o rotura) de superficies de orden superior en estructuras adecuadas para la representación.<br/>                                                                                                                                                                                                                 |
| [Fase del sombreador de geometría](geometry-shader-stage.md)<br/>                                  | La fase del sombreador de geometría (GS) ejecuta código de sombreador especificado por la aplicación con los vértices como entrada y la capacidad de generar vértices en la salida.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Secuencia: fase de salida](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | El propósito de la fase de salida de flujo es la salida continua (o secuencia) de datos de vértices de la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) en uno o varios búferes de la memoria (vea [Introducción con la fase Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)). <br/>                                                                                                                       |
| [Etapa del rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | La fase de rasterización convierte información de vectores (formada por formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real. <br/>                                                                                                                                                                                                                                                                                                 |
| [Fase del sombreador de píxeles](pixel-shader-stage.md)<br/>                                        | La fase del sombreador de píxeles (PS) permite técnicas de sombreado enriquecidas, como la iluminación por píxel y el procesamiento posterior. Un sombreador de píxeles es un programa que combina variables constantes, datos de textura, valores interpolados por vértice y otros datos para generar salidas por píxel. La fase de rasterizador invoca un sombreador de píxeles una vez para cada píxel incluido en una primitiva; sin embargo, es posible especificar un sombreador **nulo** para evitar la ejecución de un sombreador.<br/>                                          |
| [Fase de combinación de salida](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | La fase de combinación de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxeles generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad/estarcido. La fase OM es el último paso para determinar qué píxeles son visibles (con pruebas de la galería de símbolos de profundidad) y mezclar los colores finales de los píxeles.<br/>                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreador de cálculo](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

