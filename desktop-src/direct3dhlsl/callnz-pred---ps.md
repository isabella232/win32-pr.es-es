---
title: callnz Pred-PS
description: Llame a con un predicado, si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994829"
---
# <a name="callnz-pred---ps"></a>callnz Pred-PS

Llame a con un predicado, si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. Predication usa un valor booleano para determinar si no se va a realizar la instrucción.

## <a name="syntax"></a>Sintaxis



| callnz l \# , \[ ! \] P0. x1|sí|z|con |
|----------------------------------|



 

Donde:

-   donde l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador opcional Negate.
-   P0 es el registro del predicado. Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} es el swizzle de replicación necesario en P0.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz Pred           |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción hace lo siguiente:


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




