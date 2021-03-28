---
title: callnz bool-vs
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998275"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.

## <a name="syntax"></a>Sintaxis



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

donde:

-   donde l \# es una [etiqueta,](label---vs.md) que marca el principio de la subrutina a la que se va a llamar.
-   \[!\] es el modificador booleano opcional NOT.
-   b \# identifica un [registro booleano constante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
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



Esta instrucción usa una ranura de instrucciones del sombreador de vértices.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




