---
title: vs_2_0
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983734"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [Instrucciones: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene una lista de las instrucciones disponibles.
-   [Registros: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) muestra los distintos tipos de registros utilizados por el sombreador de vértices Alu.
-   Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.
-   Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.
-   [El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.

## <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas. El número de instrucciones que se ejecutan puede ser mucho mayor (debido al soporte de bucle/REP) y está limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que debe ser al menos 0xFFFF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




