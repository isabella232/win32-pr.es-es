---
title: if_comp-vs
description: 'Iniciar una expresión if bool-vs... Else-vs... endif: bloque de vs, con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.'
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996848"
---
# <a name="if_comp---vs"></a>If \_ COMP-vs

Iniciar una expresión [If bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif:](endif---vs.md) bloque de vs, con una condición basada en valores que podrían calcularse en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.

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



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| If \_ COMP               |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de una condición.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Tenga cuidado al usar los modos de comparación es igual a y no es igual a los números de punto flotante. Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor de épsilon (número pequeño distinto de cero) para evitar errores.

Entre las restricciones se incluyen:

-   If \_ comp... [else-vs](else---vs.md)... [endif:](endif---vs.md) los bloques vs (junto con los bloques if de predicado) se pueden anidar hasta 24 capas de profundidad.
-   los registros de src0 y SRC1 requieren un swizzle de replicación.
-   Si los \_ bloques de COMP deben terminar con una instrucción [else-vs](else---vs.md) o [endif-vs](endif---vs.md) .
-   If \_ comp... [else-vs](else---vs.md)... [endif: los bloques de vs](endif---vs.md) no pueden ocupar un bloque de bucle. El \_ bloque if COMP debe estar completamente dentro o fuera del bloque [Loop-vs](loop---vs.md) .

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

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




