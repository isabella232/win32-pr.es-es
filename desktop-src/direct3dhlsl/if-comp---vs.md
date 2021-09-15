---
title: if_comp - vs
description: 'Iniciar un if bool - vs... else - vs... endif: frente a block, con una condición basada en valores que se podrían calcular en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.'
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567793"
---
# <a name="if_comp---vs"></a>if \_ comp - vs

Iniciar un [if bool - vs](if-bool---vs.md)... [else : frente a](else---vs.md)... [endif: frente](endif---vs.md) a block, con una condición basada en valores que se podrían calcular en un sombreador. Esta instrucción se usa para omitir un bloque de código, en función de una condición.

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

    

     

-   src0 es un registro de origen. Se requiere la replicación de swzzle para seleccionar un componente.
-   src1 es un registro de origen. Se requiere la replicación de swzzle para seleccionar un componente.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if \_ comp               |      |      | x    | x     | x    | x     |



 

Esta instrucción se usa para omitir un bloque de código, en función de una condición.


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



Tenga cuidado al usar los modos de comparación iguales y no iguales en números de punto flotante. Dado que el redondeo se produce durante los cálculos de punto flotante, la comparación se puede realizar con un valor epsilon (número pequeño distinto de cero) para evitar errores.

Entre las restricciones se incluyen:

-   si \_ comp... [else : frente a](else---vs.md)... [endif: frente a](endif---vs.md) los bloques (junto con los bloques de predicado if) se pueden anidar hasta 24 capas de profundidad.
-   Los registros src0 y src1 requieren un swzzle de replicación.
-   si \_ los bloques comp deben terminar con [una instrucción else - vs](else---vs.md) o [endif - vs.](endif---vs.md)
-   si \_ comp... [else : frente a](else---vs.md)... [endif: frente a](endif---vs.md) los bloques no se puede bloquear un bloque de bucle. Si el \_ bloque comp debe estar completamente dentro o fuera del bucle : [vs](loop---vs.md) block.

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

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




