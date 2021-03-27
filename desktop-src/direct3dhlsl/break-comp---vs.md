---
title: break_comp-vs
description: Divida condicionalmente el bucle actual en el ENDLOOP-vs o endrep-vs más cercano.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904290"
---
# <a name="break_comp---vs"></a>Break \_ COMP-vs

Divida condicionalmente el bucle actual en el [ENDLOOP-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)más cercano.

## <a name="syntax"></a>Sintaxis



| Break \_ COMP src0, SRC1 |
|------------------------|



 

Donde:

-   \_Comp es una comparación entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Sintaxis | De comparación            |
    |--------|-----------------------|
    | \_bruto   | Mayor que          |
    | \_plazo   | Menor que             |
    | \_GE   | Mayor o igual que |
    | \_cuarto   | Menor o igual que    |
    | \_ajustes   | Igual a              |
    | \_&   | No es igual a          |

    

     

-   src0 es un registro de origen. Replicate swizzle es necesario para seleccionar un componente único.
-   SRC1 es un registro de origen. Replicate swizzle es necesario para seleccionar un componente único.

## <a name="remarks"></a>Observaciones

Esta instrucción es compatible con las siguientes versiones.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| romper \_ COMP            |      |      | x    | x     | x    | x     |



 

Cuando la comparación es true, se interrumpe el bucle actual, como se muestra.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




