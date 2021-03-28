---
title: Guía de programación para HLSL
description: Los datos entran en la canalización de gráficos como un flujo de primitivas y se procesan mediante las etapas del sombreador.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "104986147"
---
# <a name="programming-guide-for-hlsl"></a>Guía de programación para HLSL

Los datos entran en la canalización de gráficos como un flujo de primitivas y se procesan mediante las etapas del sombreador. Las fases del sombreador reales dependen de la versión de Direct3D, pero en realidad incluyen las fases de vértice, píxel y geometría. Otras fases incluyen los sombreadores de casco y de dominio para la teselación y el sombreador de cálculo. Estas fases son completamente programables mediante el lenguaje de sombreado de alto nivel ([HLSL](dx-graphics-hlsl-reference.md)).

Los sombreadores HLSL se pueden compilar en tiempo de autor o en tiempo de ejecución y establecer en el tiempo de ejecución en la fase de canalización adecuada. Los sombreadores de Direct3D 9 se pueden diseñar con el modelo de [sombreador 1](dx-graphics-hlsl-sm1.md), el modelo de sombreador [2](dx-graphics-hlsl-sm2.md) y el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md); Los sombreadores de Direct3D 10 solo se pueden diseñar en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md). Los sombreadores de Direct3D 11 se pueden diseñar en el [modelo de sombreador 5](d3d11-graphics-reference-sm5.md). Direct3D 11,3 y Direct3D 12 se pueden diseñar en el [modelo de sombreador 5,1](shader-model-5-1.md)y Direct3D 12 también se puede diseñar en el [modelo de sombreador 6](shader-model-6-0.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Usar la vinculación del sombreador](using-shader-linking.md) | Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución. |
| [Escribir sombreadores HLSL en Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Usar sombreadores en Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Usar sombreadores en Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Optimizar los sombreadores HLSL](dx-graphics-hlsl-optimize.md) | |
| [Depurar sombreadores en Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | La herramienta más reciente para la depuración de sombreadores ahora se incluye como una característica de Microsoft Visual Studio, denominada depurador de gráficos de Visual Studio.  |
| [Compilación de sombreadores](dx-graphics-hlsl-part1.md) | Echemos un vistazo a las distintas formas de compilar el código del sombreador y las convenciones para las extensiones de archivo para el código del sombreador. |
| [Especificar destinos del compilador](specifying-compiler-targets.md) | Aquí se enumeran los destinos para varios perfiles que admiten las funciones **D3DCompile \** _ y el compilador de HLSL. |
| [Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Usar precisión mínima de HLSL](using-hlsl-minimum-precision.md) | A partir de Windows 8, los controladores de gráficos pueden implementar [tipos de datos escalares HLSL](dx-graphics-hlsl-scalar.md) de precisión mínima con cualquier precisión mayor o igual que la precisión de bits especificada.  |
| [Modelo 5 del sombreador HLSL](overviews-direct3d-11-hlsl.md) | |
| [Modelo de sombreador HLSL 5,1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | En esta sección se describen las características del modelo de sombreador 5,1 como se aplican en la práctica de D3D12 y D3D 11.3. Todo el hardware de DirectX 12 admite el modelo de sombreador 5,1. |
| [Modelo de sombreador HLSL 6,0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Describe los intrínsecos de operación de onda agregados al modelo de sombreador de HLSL 6,0. |
| [Modelo de sombreador HLSL 6,4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Describe los intrínsecos de machine learning agregados al modelo de sombreador de HLSL 6,4. |

## <a name="related-topics"></a>Temas relacionados

_ [HLSL](dx-graphics-hlsl.md)
* [Referencia de HLSL](dx-graphics-hlsl-reference.md)
