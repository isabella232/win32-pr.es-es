---
title: callnz pred - vs
description: Llame a si no es cero, con un predicado. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. Predication usa un valor booleano para determinar si no se debe realizar la instrucción.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287029"
---
# <a name="callnz-pred---vs"></a>callnz pred - vs

Llame a si no es cero, con un predicado. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. Predication usa un valor booleano para determinar si no se debe realizar la instrucción.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

donde:

-   l \# es una [etiqueta, frente](label---vs.md) a marcar el principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador negate opcional.
-   p0 es el [registro de predicado.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   {x \| y \| z \| w} es la réplica necesaria en p0.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz pred            |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Esta instrucción consume un espacio de instrucciones del sombreador de vértices.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




