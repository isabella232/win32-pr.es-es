---
title: break_comp-PS
description: Salga del bucle actual en el ENDLOOP-PS o endrep-PS más cercano, en función de una comparación por componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148995"
---
# <a name="break_comp---ps"></a>Break \_ COMP-PS

Salga del bucle actual en el [ENDLOOP-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)más cercano, en función de una comparación por componente.

## <a name="syntax"></a>Sintaxis



| Break \_ COMP src0, SRC1 |
|------------------------|



 

Donde:

-   \_Comp es una comparación escalar (o única) entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Sintaxis | De comparación            |
    |--------|-----------------------|
    | \_bruto   | Mayor que          |
    | \_plazo   | Menor que             |
    | \_GE   | Mayor o igual que |
    | \_cuarto   | Menor o igual que    |
    | \_ajustes   | Igual a              |
    | \_&   | No es igual a          |

    

     

-   src0 es un registro de origen. La replicación de swizzle es necesaria si se selecciona un único componente.
-   SRC1 es un registro de origen. La replicación de swizzle es necesaria si se selecciona un único componente.

## <a name="remarks"></a>Observaciones

Esta instrucción es compatible con las siguientes versiones.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| romper \_ COMP           |      |      |      |      |      | x    | x     | x    | x     |



 

Cuando la comparación es true, se interrumpe el bucle actual, como se muestra.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




