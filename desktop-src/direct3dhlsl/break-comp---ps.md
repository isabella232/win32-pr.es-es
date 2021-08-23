---
title: break_comp- ps
description: 'Salga del bucle actual en el endloop más cercano: ps o endrep - ps, en función de una comparación por componente.'
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794470"
---
# <a name="break_comp---ps"></a>break \_ comp - ps

Salga del bucle actual en el [endloop](endloop---ps.md) más cercano: ps o [endrep - ps](endrep---ps.md), en función de una comparación por componente.

## <a name="syntax"></a>Syntax



| break \_ comp src0, src1 |
|------------------------|



 

Donde:

-   \_comp es una comparación escalar (o única) entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Syntax | De comparación            |
    |--------|-----------------------|
    | \_Gt   | Mayor que          |
    | \_Lt   | Menor que             |
    | \_Ge   | Mayor o igual que |
    | \_le   | Menor o igual que    |
    | \_Eq   | Igual a              |
    | \_Ne   | No es igual a          |

    

     

-   src0 es un registro de origen. Es necesario replicar swzzle si se selecciona un único componente.
-   src1 es un registro de origen. Es necesario replicar swzzle si se selecciona un único componente.

## <a name="remarks"></a>Comentarios

Esta instrucción se admite en las versiones siguientes.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| break \_ comp           |      |      |      |      |      | x    | x     | x    | x     |



 

Cuando la comparación es verdadera, se interrumpe del bucle actual, como se muestra.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




