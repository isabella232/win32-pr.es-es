---
title: ps_2_0
description: Obtenga información ps_2_0, un sombreador de píxeles programable, que se forma de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010988"
---
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

-   [ps \_ 2 \_ 0 Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) una lista de las instrucciones disponibles.
-   [ps \_ 2 \_ 0 Registros enumera](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) los diferentes tipos de registros usados por el sombreador de vértices ALU.
-   [Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.
-   [La máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina qué componentes del registro de destino se escriben.
-   [Los modificadores de registro de origen del sombreador de](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) píxeles modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [Source Register Swling proporciona](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.

## <a name="instruction-count"></a>Recuento de instrucciones

Los sombreadores tienen restricciones para el número máximo de instrucciones. Total de ranuras de instrucción: 96 (64 aritméticas y 32 texturas).

## <a name="sampler-count"></a>Sampler Count

El número de muestreadores de textura disponibles es 16.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




