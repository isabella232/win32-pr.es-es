---
title: callnz bool-PS
description: Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998280"
---
# <a name="callnz-bool---ps"></a>callnz bool-PS

Llame a si no es cero. Realiza una llamada condicional a la instrucción marcada por el índice de la etiqueta.

## <a name="syntax"></a>Sintaxis



| callnz l \# , \[ ! \] b\# |
|----------------------|



 

Donde:

-   l \# es una [etiqueta-PS](label---ps.md) que marca el principio de la subrutina a la que se va a llamar.
-   \[!\] es un modificador opcional Negate.
-   b \# identifica un [registro booleano constante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
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

 

 




