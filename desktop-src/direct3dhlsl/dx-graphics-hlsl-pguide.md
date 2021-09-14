---
title: Guía de programación para HLSL
description: Los datos entran en la canalización de gráficos como una secuencia de primitivas y se procesan mediante las fases del sombreador.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258447"
---
# <a name="programming-guide-for-hlsl"></a>Guía de programación para HLSL

Los datos entran en la canalización de gráficos como una secuencia de primitivas y se procesan mediante las fases del sombreador. Las fases reales del sombreador dependen de la versión de Direct3D, pero sin duda incluyen las fases de vértice, píxel y geometría. Otras fases incluyen los sombreadores de casco y dominio para teselación y el sombreador de proceso. Estas fases se pueden programar completamente mediante el lenguaje de sombreado de alto nivel[(HLSL).](dx-graphics-hlsl-reference.md)

Los sombreadores HLSL se pueden compilar en tiempo de creación o en tiempo de ejecución, y establecerse en tiempo de ejecución en la fase de canalización adecuada. Los sombreadores de Direct3D 9 se pueden diseñar mediante el modelo de sombreador [1,](dx-graphics-hlsl-sm1.md)el modelo de sombreador [2](dx-graphics-hlsl-sm2.md) y el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md); Los sombreadores de Direct3D 10 solo se pueden diseñar en el [modelo 4 del sombreador.](dx-graphics-hlsl-sm4.md) Los sombreadores de Direct3D 11 se pueden diseñar en el modelo [de sombreador 5.](d3d11-graphics-reference-sm5.md) Direct3D 11.3 y Direct3D 12 se pueden diseñar en el modelo de sombreador [5.1](shader-model-5-1.md)y Direct3D 12 también se puede diseñar en el modelo [de sombreador 6.](shader-model-6-0.md)

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Uso de la vinculación de sombreador](using-shader-linking.md) | Se muestra cómo crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a sombreadores completos en tiempo de ejecución. |
| [Escribir sombreadores HLSL en Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Uso de sombreadores en Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Uso de sombreadores en Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Optimización de sombreadores HLSL](dx-graphics-hlsl-optimize.md) | |
| [Depuración de sombreadores en Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | La herramienta más reciente para depurar sombreadores ahora se incluye como una característica en Microsoft Visual Studio, denominada Visual Studio Depurador de gráficos.  |
| [Compilación de sombreadores](dx-graphics-hlsl-part1.md) | Ahora se verán varias maneras de compilar el código del sombreador y las convenciones de las extensiones de archivo para el código del sombreador. |
| [Especificar destinos del compilador](specifying-compiler-targets.md) | Aquí se enumeran los destinos de varios perfiles que las funciones **D3DCompile \*** y el compilador HLSL admiten. |
| [Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Uso de la precisión mínima hlsl](using-hlsl-minimum-precision.md) | A partir Windows 8, los controladores gráficos pueden implementar tipos de datos escalares [HLSL](dx-graphics-hlsl-scalar.md) de precisión mínima mediante cualquier precisión mayor o igual que su precisión de bits especificada.  |
| [Modelo de sombreador HLSL 5](overviews-direct3d-11-hlsl.md) | |
| [Modelo de sombreador HLSL 5.1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | En esta sección se describen las características del modelo de sombreador 5.1, que se aplican en la práctica a D3D12 y D3D11.3. Todo el hardware de DirectX 12 admite Shader Model 5.1. |
| [Modelo de sombreador HLSL 6.0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Describe los intrínsecos de la operación de onda agregados al modelo de sombreador HLSL 6.0. |
| [Modelo de sombreador HLSL 6.4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Describe los intrínsecos de aprendizaje automático agregados al modelo de sombreador HLSL 6.4. |

## <a name="related-topics"></a>Temas relacionados

* [HLSL](dx-graphics-hlsl.md)
* [Referencia de HLSL](dx-graphics-hlsl-reference.md)
