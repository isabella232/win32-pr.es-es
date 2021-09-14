---
title: Lenguaje de sombreador de alto nivel (HLSL)
description: HLSL es el lenguaje de sombreador de alto nivel de tipo C que se usa con sombreadores programables en DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: 9f518102b7b3305103ed85231a791c542418a04c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264108"
---
# <a name="high-level-shader-language-hlsl"></a>Lenguaje de sombreador de alto nivel (HLSL)

HLSL es el lenguaje de sombreador de alto nivel de tipo C que se usa con sombreadores programables en DirectX.

Por ejemplo, puede usar HLSL para escribir un sombreador de vértices [o](../direct3d11/vertex-shader-stage.md)un sombreador de [píxeles](../direct3d11/pixel-shader-stage.md)y usarlos en la implementación del representador en la [aplicación de Direct3D.](../direct3d12/directx-12-programming-guide.md)

O bien, podría usar HLSL para escribir un sombreador de proceso, quizás para implementar una simulación física. Sin embargo, si por ejemplo está dispuesto a escribir su propio operador de convolución (para el procesamiento de imágenes) como HLSL en un sombreador de proceso, tendrá un mejor rendimiento en ese escenario si usa [Direct Machine Learning (DirectML)](/windows/ai/directml/dml) en su lugar.

HLSL se creó (a partir de DirectX 9) para configurar la canalización 3D [programable.](../direct3d11/overviews-direct3d-11-graphics-pipeline.md) Puede programar toda la canalización con instrucciones HLSL.

## <a name="where-to-go-next"></a>Dónde ir a continuación

* [Guía de programación para HLSL](./dx-graphics-hlsl-pguide.md)
* [Referencia de HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guía de programación para HLSL

Para obtener una introducción conceptual a HLSL, consulte la [Guía de programación de HLSL.](./dx-graphics-hlsl-pguide.md)

La guía de programación describe los diferentes tipos de fases del sombreador y cómo crear, compilar, optimizar, enlazar y vincular sombreadores.

Allí también encontrará información general y notas de la versión sobre las sucesivas generaciones de la versión del modelo de sombreador que se han publicado, hasta el modelo de sombreador HLSL 5.

### <a name="reference-for-hlsl"></a>Referencia de HLSL

Para obtener documentación de referencia de HLSL, consulte [la Referencia de HLSL.](./dx-graphics-hlsl-reference.md)

La sección de referencia tiene una lista completa de la sintaxis del lenguaje y de las funciones intrínsecas que están integradas en HLSL con el fin de simplificar los requisitos de codificación.

También encontrará una explicación de los modelos de sombreador frente a los perfiles y el contenido de referencia del modelo de sombreador hasta el modelo de sombreador HLSL 1. También hay contenido que abarca instrucciones de ensamblado, la herramienta D3DCompiler e información sobre los errores y advertencias que puede devolver un sombreador.