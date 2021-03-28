---
title: Lenguaje de sombreador de alto nivel (HLSL)
description: HLSL es el lenguaje de sombreador de alto nivel de C que se usa con los sombreadores programables en DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104986182"
---
# <a name="high-level-shader-language-hlsl"></a>Lenguaje de sombreador de alto nivel (HLSL)

HLSL es el lenguaje de sombreador de alto nivel de C que se usa con los sombreadores programables en DirectX.

Por ejemplo, puede usar HLSL para escribir un [sombreador de vértices](../direct3d11/vertex-shader-stage.md), un [sombreador de píxeles](../direct3d11/pixel-shader-stage.md)y usar esos sombreadores en la implementación del representador en la aplicación [Direct3D](../direct3d12/directx-12-programming-guide.md) .

O bien, puede usar HLSL para escribir un sombreador de cálculo, quizás para implementar una simulación física. Sin embargo, si, por ejemplo, está inclinado por escribir su propio operador de circunvolución (para el procesamiento de imágenes) como HLSL en un sombreador de cálculo, obtendrá un mejor rendimiento en ese escenario si usa [machine learning directo (DirectML)](../direct3d12/dml.md) en su lugar.

Se creó HLSL (a partir de DirectX 9) para configurar la [canalización](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programable. Puede programar toda la canalización con instrucciones de HLSL.

## <a name="where-to-go-next"></a>Dónde ir siguiente

* [Guía de programación para HLSL](./dx-graphics-hlsl-pguide.md)
* [Referencia de HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guía de programación para HLSL

Para obtener una introducción conceptual a HLSL, consulte la [Guía de programación para HLSL](./dx-graphics-hlsl-pguide.md).

En la guía de programación se describen los diferentes tipos de fases del sombreador y cómo crear, compilar, optimizar, enlazar y vincular sombreadores.

Allí también encontrará información general y notas de la versión sobre las generaciones sucesivas de la versión del modelo de sombreador que se han lanzado, volviendo al modelo de sombreador de HLSL 5.

### <a name="reference-for-hlsl"></a>Referencia de HLSL

Para obtener documentación de referencia de HLSL, consulte la [referencia de HLSL](./dx-graphics-hlsl-reference.md).

La sección de referencia contiene una lista completa de la sintaxis del lenguaje y de las funciones intrínsecas integradas en HLSL para simplificar los requisitos de codificación.

También encontrará una descripción de los modelos de sombreador frente a los perfiles y el contenido de referencia del modelo de sombreador que vuelve a pasar hasta el modelo de sombreador de HLSL 1. También hay contenido que abarca las instrucciones de ensamblado, la herramienta D3DCompiler y la información sobre los errores y advertencias que puede devolver un sombreador.