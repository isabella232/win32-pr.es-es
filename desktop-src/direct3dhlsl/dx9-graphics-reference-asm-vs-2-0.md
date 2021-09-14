---
title: vs_2_0
description: Obtenga información vs_2_0, un sombreador de vértices programable, que se conste de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974690"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [Instrucciones: frente \_ a \_ 2 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene una lista de las instrucciones disponibles.
-   [Registros: frente \_ a 2 \_ 0,](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) se enumeran los distintos tipos de registros que usa el sombreador de vértices ALU.
-   [Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.
-   [Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [El swling del registro de origen](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, copian o escriben.
-   [El enmascaramiento del registro de](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) destino determina qué componentes del registro de destino se escriben.

## <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas. El número de instrucciones que se ejecutan puede ser mucho mayor (debido a la compatibilidad con bucles o representantes) y está limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que debe ser al menos 0xFFFF.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




