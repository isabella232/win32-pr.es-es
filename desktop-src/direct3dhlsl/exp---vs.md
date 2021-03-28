---
title: EXP-vs
description: Proporciona el doble de precisión exponencial. | EXP-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998221"
---
# <a name="exp---vs"></a>EXP-vs

Proporciona una precisión completa exponencial 2<sup>x</sup>.

## <a name="syntax"></a>Sintaxis



| EXP DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes). Consulte [source Register permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción proporciona al menos 21 bits de precisión.

En el siguiente fragmento de código se muestran las operaciones realizadas:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




