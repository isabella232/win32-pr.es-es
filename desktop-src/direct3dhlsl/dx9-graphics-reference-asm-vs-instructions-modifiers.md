---
title: Modificadores de instrucciones (HLSL VS Reference)
description: Modificadores de instrucciones
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104487199"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificadores de instrucciones (HLSL VS Reference)

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.

## <a name="_sat"></a>\_sábado

Satura (o fija) el resultado de la instrucción en \[ 0, 1 \] intervalo antes de escribir en el registro de destino.

Por ejemplo:


```
add_sat dst, src0, src1
```



Donde:

DST = abrazadera \_ entre \_ 0 \_ y \_ 1 (src0 + SRC1)

El \_ modificador de instrucciones SAT no cuesta ninguna ranura de instrucciones adicional.

Si se admite, el \_ modificador de instrucciones de SAT se puede usar con cualquier instrucción excepto: [FRC-vs](frc---vs.md), [sincos (-vs](sincos---vs.md)y [texldl-vs](texldl---vs.md).



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_sábado                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




