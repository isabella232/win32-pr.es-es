---
title: callnz bool - vs
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. | callnz bool - vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a6d5a7646670d182b0b685ab742fb5b2094a89a717a31019165054bcbc4816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287263"
---
# <a name="callnz-bool---vs"></a>callnz bool - vs

Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

donde:

-   donde l \# es una [etiqueta: frente](label---vs.md) a marcar el principio de la subrutina a la que se va a llamar.
-   \[!\] es el modificador NOT booleano opcional.
-   b \# identifica un registro [booleano constante.](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz bool            |      | x    | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:


```
if (specified boolean register is not zero)
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

 

 




