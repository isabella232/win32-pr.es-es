---
title: callnz Pred-vs
description: Llame a si no es cero, con un predicado. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077092"
---
# <a name="callnz-pred---vs"></a>callnz Pred-vs

Llame a si no es cero, con un predicado. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.

## <a name="syntax"></a>Sintaxis



| callnz l \# , \[ ! \] P0. x1|sí|z|con |
|----------------------------------|



 

donde:

-   l \# es una [etiqueta, frente](label---vs.md) al marcado del principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador opcional Negate.
-   P0 es el [registro del predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} es el swizzle de replicación necesario en P0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| callnz Pred            |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Esta instrucción usa una ranura de instrucciones del sombreador de vértices.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




