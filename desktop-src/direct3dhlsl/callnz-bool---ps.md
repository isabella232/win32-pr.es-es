---
title: callnz bool - ps
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. | callnz bool - ps
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516635"
---
# <a name="callnz-bool---ps"></a>callnz bool - ps

Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] B\# |
|----------------------|



 

Donde:

-   l \# es una [etiqueta: ps](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador negate opcional.
-   b \# identifica un registro [booleano constante.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




