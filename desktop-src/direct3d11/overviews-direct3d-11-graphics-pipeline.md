---
title: Canalización de gráficos
description: En esta sección se describe la canalización programable de Direct3D 11.
ms.assetid: 8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3872fbfaf63a53a07c8c06246088a5eec1791f98be867adbe56ae1d9c7724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565575"
---
# <a name="graphics-pipeline"></a>Canalización de gráficos

La canalización programable Direct3D 11 está diseñada para generar gráficos para aplicaciones de juegos en tiempo real. En esta sección se describe la canalización programable de Direct3D 11. En el diagrama siguiente se muestra el flujo de datos de entrada a salida a través de cada una de las fases programables.

![diagrama del flujo de datos en la canalización programable direct3d 11](images/d3d11-pipeline-stages.jpg)

La canalización de gráficos para Microsoft Direct3D 11 admite las mismas fases que la canalización de gráficos [de Direct3D 10,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)con fases adicionales para admitir características avanzadas.

Puede usar direct3D 11API para configurar todas las fases. Las fases que cuentan con núcleos comunes de sombreador (los bloques rectangulares redondeados) se pueden programar mediante el [lenguaje de programación HLSL.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) Como verá, esto hace que la canalización sea extremadamente flexible y adaptable.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)<br/> | La API direct3D 10 y superior separa las áreas funcionales de la canalización en fases. la primera fase de la canalización es la fase de ensamblador de entrada (IA).<br/>                                                                                                                                                                                                                                                                                                                             |
| [Fase del sombreador de vértices](vertex-shader-stage.md)<br/>                                      | La fase sombreador de vértices (VS) procesa los vértices del ensamblador de entrada, realizando operaciones por vértice como transformaciones, descamblación, transformación e iluminación por vértice. Los sombreadores de vértices siempre funcionan en un solo vértice de entrada y generan un solo vértice de salida. La fase del sombreador de vértices siempre debe estar activa para que se ejecute la canalización. Si no se requiere ninguna modificación o transformación de vértices, se debe crear un sombreador de vértices de paso a través y establecerlo en la canalización.<br/> |
| [Fases de teselación](direct3d-11-advanced-stages-tessellation.md)<br/>                 | El entorno de ejecución de Direct3D 11 admite tres nuevas fases que implementan la teselación, que convierte las superficies de subdivisión de bajo detalle en primitivas de mayor detalle en la GPU. Mosaicos de teselación (o divide) superficies de orden superior en estructuras adecuadas para la representación.<br/>                                                                                                                                                                                                                 |
| [Fase del sombreador de geometría](geometry-shader-stage.md)<br/>                                  | La fase geometry-shader (GS) ejecuta código de sombreador especificado por la aplicación con vértices como entrada y la capacidad de generar vértices en la salida.<br/>                                                                                                                                                                                                                                                                                                                                          |
| [Fase stream-output](d3d10-graphics-programming-guide-output-stream-stage.md)<br/>     | El propósito de la fase stream-output es generar continuamente (o transmitir) datos de vértices desde la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) a uno o varios búferes en memoria (vea [Tareas iniciales con](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)la fase Stream-Output ). <br/>                                                                                                                       |
| [Etapa del rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)<br/>           | La fase de rasterización convierte la información vectorial (compuesta de formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real. <br/>                                                                                                                                                                                                                                                                                                 |
| [Fase del sombreador de píxeles](pixel-shader-stage.md)<br/>                                        | La fase de sombreador de píxeles (PS) permite técnicas de sombreado enriquecciones, como la iluminación por píxel y el procesamiento posterior. Un sombreador de píxeles es un programa que combina variables constantes, datos de textura, valores interpolados por vértice y otros datos para generar salidas por píxel. La fase de rasterizador invoca un sombreador de píxeles una vez por cada píxel cubierto por una primitiva; sin embargo, es posible especificar un sombreador **NULL** para evitar ejecutar un sombreador.<br/>                                          |
| [Fase de fusión de salida](d3d10-graphics-programming-guide-output-merger-stage.md)<br/>     | La fase de fusión de salida (OM) genera el color de píxel representado final mediante una combinación de estado de canalización, los datos de píxel generados por los sombreadores de píxeles, el contenido de los destinos de representación y el contenido de los búferes de profundidad o galería de símbolos. La fase OM es el paso final para determinar qué píxeles son visibles (con pruebas de galería de símbolos de profundidad) y combinar los colores de píxeles finales.<br/>                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreador de proceso](direct3d-11-advanced-stages-compute-shader.md)
</dt> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

