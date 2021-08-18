---
title: Modificadores de instrucción (referencia de HLSL VS)
description: Modificadores de instrucción
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119699"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificadores de instrucción (referencia de HLSL VS)

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.

## <a name="_sat"></a>\_Sentado

Satura (o fija) el resultado de la instrucción en \[ un intervalo de 0,1 antes \] de escribir en el registro de destino.

Por ejemplo:


```
add_sat dst, src0, src1
```



Donde:

dst = \_ fijación \_ entre 0 y \_ \_ 1(src0 + src1)

El \_ modificador de instrucción sat no cuesta espacios de instrucciones adicionales.

Si se admite, el modificador de instrucción sat se puede usar con cualquier instrucción \_ excepto: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md)y [texldl - frente a](texldl---vs.md).



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \_Sentado                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




