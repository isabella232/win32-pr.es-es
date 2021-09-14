---
title: ps_2_0
description: Obtenga información ps_2_0, un sombreador de píxeles programable, que se conste de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360806"
---
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [ps \_ 2 \_ 0 Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) una lista de las instrucciones disponibles.
-   [ps \_ 2 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) enumera los distintos tipos de registros usados por el sombreador de vértices ALU.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.
-   [Destination Register Write Mask determina](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) qué componentes del registro de destino se escriben.
-   [Los modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [El swling del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, copian o escriben.

## <a name="instruction-count"></a>Recuento de instrucciones

Los sombreadores tienen restricciones para el número máximo de instrucciones. Espacios de instrucción totales: 96 (64 aritméticas y 32 texturas).

## <a name="sampler-count"></a>Recuento de muestreador

El número de muestreadores de textura disponibles es 16.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




