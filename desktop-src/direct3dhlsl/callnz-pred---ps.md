---
title: callnz pred - ps
description: Llame a con un predicado, si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. Predication usa un valor booleano para determinar si no se debe realizar la instrucción.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f56699a4853b7012401529ecfad6fbfb0006e21990a99a2fe5631faebd57674d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983295"
---
# <a name="callnz-pred---ps"></a>callnz pred - ps

Llame a con un predicado, si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de etiqueta. Predication usa un valor booleano para determinar si no se debe realizar la instrucción.

## <a name="syntax"></a>Syntax



| callnz l \# , \[ ! \] p0. {x\|y\|z\|w} |
|----------------------------------|



 

Donde:

-   donde l \# es una [etiqueta: ps](label---ps.md) marca el principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador negate opcional.
-   p0 es el registro de predicado. Vea [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} es la réplica necesaria en p0.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz pred           |      |      |      |      |      | x    | x     | x    | x     |



 

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

 

 




