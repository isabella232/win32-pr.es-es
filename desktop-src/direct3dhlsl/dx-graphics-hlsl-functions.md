---
title: Funciones (referencia de HLSL)
description: Las funciones encapsulan instrucciones HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104358518"
---
# <a name="functions-hlsl-reference"></a>Funciones (referencia de HLSL)

Las funciones encapsulan instrucciones HLSL. Esto le permite depurar un conjunto de funciones y, a continuación, volver a usarlas en otros sombreadores o efectos. Puede que desee crear una función que encapsule la funcionalidad de un sombreador de vértices, un sombreador de píxeles o un sombreador de textura. Otras veces, es posible que desee escribir una función auxiliar que realice alguna tarea de uso frecuente y, a continuación, llamar a esa función auxiliar desde la función de sombreador. Las reglas para escribir funciones de sombreador para HLSL son muy similares a la escritura de funciones de C.

-   [Sintaxis](dx-graphics-hlsl-function-syntax.md)
-   [Parámetros](dx-graphics-hlsl-function-parameters.md)
-   [Instrucción return](dx-graphics-hlsl-return.md)
-   [Firmas](dx-graphics-hlsl-signatures.md)

HLSL también tiene un número de [**funciones intrínsecas integradas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Dado que todas las funciones intrínsecas se prueban y optimizan el rendimiento, es recomendable usar una función intrínseca siempre que sea posible en lugar de crear su propia función.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis del lenguaje (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




