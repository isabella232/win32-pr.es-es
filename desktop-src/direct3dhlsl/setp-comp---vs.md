---
title: setp_comp-vs
description: Establezca el registro del predicado. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424247"
---
# <a name="setp_comp---vs"></a>\_COMP SETP-vs

Establezca el registro del predicado.

## <a name="syntax"></a>Sintaxis



| SETP \_ COMP DST, src0, SRC1 |
|----------------------------|



 

Donde:

-   \_Comp es una comparación por canal entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Sintaxis | De comparación            |
    |--------|-----------------------|
    | \_bruto   | Mayor que          |
    | \_plazo   | Menor que             |
    | \_GE   | Mayor o igual que |
    | \_cuarto   | Menor o igual que    |
    | \_ajustes   | Igual a              |
    | \_&   | No es igual a          |

    

     

-   DST es el registro de [predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) Register, P0.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| comp. SETP \_             |      |      | x    | x     | x    | x     |



 

Esta instrucción funciona como:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Para cada canal que se puede escribir en función de la máscara de escritura de destino, guarde el resultado booleano de la operación de comparación entre los canales correspondientes de src0 y SRC1 (después de que se haya resuelto el modificador de origen swizzles).

Los registros de origen permiten especificar swizzles de componentes arbitrarios.

El registro de destino permite máscaras de escritura arbitrarias.

El registro de destino debe ser el registro de predicado.

## <a name="applying-the-predicate-register"></a>Aplicar el registro de predicado

Una vez que se ha inicializado el registro de predicado con SETP, se puede usar para controlar una instrucción por componente. Esta es la sintaxis:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Donde:

-   \[!\] es un booleano opcional que no es
-   P0 es el registro del predicado
-   \[. swizzle \] es un swizzle opcional que se aplica al contenido del predicado Register antes de usarlo para enmascarar la instrucción. Los swizzles disponibles son:. xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swizzle de replicación:. x/. r,. y/. g,. z/. b o. a/. w.
-   Instruction es cualquier Aritmetic o instrucción de textura. No puede ser una instrucción de control de flujo estático o dinámico.
-   Dest, srcReg,... son los registros requeridos por la instrucción

Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



para realizar una adición de dos componentes.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



Los componentes x e y de R2 no se escribirán, ya que el registro de predicado contenía false en los componentes z y w.

La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta el número de ranuras de la instrucción en 1.

El registro de predicado también se puede aplicar a si se preparan las instrucciones [Pred-vs](if-pred---vs.md), [callnz Pred-vs](callnz-pred---vs.md) y [breakp-vs](breakp---vs.md) . Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




