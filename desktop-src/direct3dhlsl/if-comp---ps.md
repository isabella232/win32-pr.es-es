---
title: 'if_comp : ps'
description: 'Iniciar un if bool - ps... else: ps... endif: bloque ps, con una condición basada en valores que se podrían calcular en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.'
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568925"
---
# <a name="if_comp---ps"></a>if \_ comp : ps

Iniciar un [if bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif: bloque ps,](endif---ps.md) con una condición basada en valores que se podrían calcular en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.

## <a name="syntax"></a>Sintaxis



| if \_ comp src0, src1 |
|---------------------|



 

Donde:

-   \_comp es una comparación entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Sintaxis | De comparación            |
    |--------|-----------------------|
    | \_Gt   | Mayor que          |
    | \_Lt   | Menor que             |
    | \_Ge   | Mayor o igual que |
    | \_le   | Menor o igual que    |
    | \_Eq   | Igual a              |
    | \_Ne   | No es igual a          |

    

     

-   src0 es un registro de origen. Para seleccionar un componente, es necesario replicar sw swzzle.
-   src1 es un registro de origen. Para seleccionar un componente, es necesario replicar sw swzzle.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if \_ comp              |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de una condición.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Tenga cuidado al usar los modos de comparación iguales y no iguales en números de punto flotante. Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor epsilon (número pequeño distinto de cero) para evitar errores.

Entre las restricciones se incluyen:

-   si \_ comp... [else - ps](else---ps.md)... [endif: los bloques ps](endif---ps.md) (junto con el predicado [if blocks)](if-bool---ps.md) se pueden anidar hasta 24 capas de profundidad.
-   Los registros src0 y src1 requieren un swzzle de replicación.
-   si \_ los bloques comp deben terminar con [una instrucción else - vs](else---vs.md) o [endif - vs.](endif---vs.md)
-   si \_ comp... [else - ps](else---ps.md)... [endif: los bloques ps](endif---ps.md) no pueden bloquear un bloque de bucle. El bloque \_ if comp debe estar completamente dentro o fuera del bloque de bucle.

## <a name="example"></a>Ejemplo

Esta instrucción proporciona control de flujo dinámico condicional.


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




