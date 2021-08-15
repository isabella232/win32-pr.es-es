---
title: Funciones (referencia hlsl)
description: Las funciones encapsulan instrucciones HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37086a030ad902f2bfb5deab52ffba620e97890bd13e7c6957170572087ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514583"
---
# <a name="functions-hlsl-reference"></a>Funciones (referencia hlsl)

Las funciones encapsulan instrucciones HLSL. Esto le permite depurar un conjunto de funciones y volver a usarlas en sombreadores o efectos. Es posible que quiera crear una función que encapsula la funcionalidad de un sombreador de vértices, un sombreador de píxeles o un sombreador de textura. En otras ocasiones, es posible que quiera escribir una función auxiliar que realice alguna tarea de uso frecuente y, a continuación, llamar a esa función auxiliar desde la función de sombreador. Las reglas para escribir funciones de sombreador para HLSL son muy similares a la escritura de funciones de C.

-   [Sintaxis](dx-graphics-hlsl-function-syntax.md)
-   [Parámetros](dx-graphics-hlsl-function-parameters.md)
-   [Return (Instrucción)](dx-graphics-hlsl-return.md)
-   [Firmas](dx-graphics-hlsl-signatures.md)

HLSL también tiene una serie de funciones intrínsecas [**integradas (DirectX HLSL).**](dx-graphics-hlsl-intrinsic-functions.md) Dado que todas las funciones intrínsecas se prueban y se optimiza el rendimiento, es una buena práctica usar una función intrínseca siempre que sea posible en lugar de crear su propia función.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis del lenguaje (HLSL de DirectX)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




