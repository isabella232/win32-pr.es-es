---
title: if_comp-PS
description: Iniciar un IF bool-PS... Else-PS... bloque endif-PS, con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784888"
---
# <a name="if_comp---ps"></a>Si \_ COMP-PS

Iniciar un [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... bloque [endif-PS](endif---ps.md) , con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.

## <a name="syntax"></a>Sintaxis



| If \_ COMP src0, SRC1 |
|---------------------|



 

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

    

     

-   src0 es un registro de origen. La replicación de swizzle es necesaria para seleccionar un componente.
-   SRC1 es un registro de origen. La replicación de swizzle es necesaria para seleccionar un componente.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| If \_ COMP              |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de una condición.


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



Tenga cuidado al usar los modos de comparación es igual a y no es igual a los números de punto flotante. Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor de épsilon (número pequeño distinto de cero) para evitar errores.

Entre las restricciones se incluyen:

-   If \_ comp... [else-PS](else---ps.md)... los bloques [endif-PS](endif---ps.md) (junto con los bloques [If](if-bool---ps.md) de predicado) se pueden anidar hasta 24 capas de profundidad.
-   los registros de src0 y SRC1 requieren un swizzle de replicación.
-   Si los \_ bloques de COMP deben terminar con una instrucción [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .
-   If \_ comp... [else-PS](else---ps.md)... los bloques [endif-PS](endif---ps.md) no pueden ocupar un bloque de bucle. El \_ bloque if COMP debe estar completamente dentro o fuera del bloque de bucle.

## <a name="example"></a>Ejemplo

Esta instrucción proporciona el control de flujo dinámico condicional.


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

 

 




