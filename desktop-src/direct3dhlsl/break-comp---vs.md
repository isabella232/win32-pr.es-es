---
title: 'break_comp : vs'
description: Interrumpir condicionalmente el bucle actual en el endloop más cercano ( vs o endrep ) frente a
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a02bf34844918255086b318d9a13feeabbd6e75bdecca03684adaba70b420626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626565"
---
# <a name="break_comp---vs"></a>break \_ comp- vs

Interrumpir condicionalmente el bucle actual en el [endloop más](endloop---vs.md) cercano ( frente a [o endrep ) frente a](endrep---vs.md).

## <a name="syntax"></a>Syntax



| break \_ comp src0, src1 |
|------------------------|



 

Donde:

-   \_comp es una comparación entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Syntax | De comparación            |
    |--------|-----------------------|
    | \_Gt   | Mayor que          |
    | \_Lt   | Menor que             |
    | \_Ge   | Mayor o igual que |
    | \_le   | Menor o igual que    |
    | \_Eq   | Igual a              |
    | \_Ne   | No es igual a          |

    

     

-   src0 es un registro de origen. Es necesario replicar swzzle para seleccionar un único componente.
-   src1 es un registro de origen. Es necesario replicar swzzle para seleccionar un único componente.

## <a name="remarks"></a>Comentarios

Esta instrucción se admite en las versiones siguientes.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| break \_ comp            |      |      | x    | x     | x    | x     |



 

Cuando la comparación es verdadera, se interrumpe del bucle actual, como se muestra.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




