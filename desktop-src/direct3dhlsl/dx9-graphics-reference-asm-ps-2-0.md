---
title: ps_2_0
description: Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983614"
---
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [las \_ instrucciones de PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contienen una lista de las instrucciones disponibles.
-   en los [registros de PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) se enumeran los distintos tipos de registros utilizados por el sombreador de vértices Alu.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se utilizan para modificar la forma en que funciona una instrucción.
-   La [máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina los componentes del registro de destino que se van a escribir.
-   Los [modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.

## <a name="instruction-count"></a>Recuento de instrucciones

Los sombreadores tienen restricciones para el número máximo de instrucciones. Total de ranuras de instrucciones: 96 (64 aritméticos y texturas de 32).

## <a name="sampler-count"></a>Recuento de muestras

El número de muestras de textura disponibles es 16.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




