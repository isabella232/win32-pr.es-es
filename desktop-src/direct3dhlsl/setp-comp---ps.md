---
title: setp_comp-PS
description: Establezca el registro del predicado. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280128"
---
# <a name="setp_comp---ps"></a>SETP \_ COMP-PS

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

    

     

-   DST es el registro de [predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) Register, P0.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| comp. SETP \_            |      |      |      |      |      | x    | x     | x    | x     |



 

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

El registro de DST debe ser el registro del predicado.

## <a name="applying-the-predicate-register"></a>Aplicar el registro de predicado

Una vez que se ha inicializado el registro de predicado con SETP \_ COMP, se puede usar para controlar una instrucción por componente. Esta es la sintaxis:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Donde:

-   \[!\] es un booleano opcional que no es
-   P0 es el registro del predicado
-   \[. swizzle \] es un swizzle opcional que se aplica al contenido del predicado Register antes de usarlo para enmascarar la instrucción. Los swizzles disponibles son:. xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swizzle de replicación:. x/. r,. y/. g,. z/. b o. a/. w.
-   Instruction es cualquier Aritmetic o instrucción de textura. No puede ser una instrucción de control de flujo estático o dinámico.
-   Dest, src0,... son los registros requeridos por la instrucción

Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:


```
(p0) add r1, r2, r3
```



para realizar una adición de dos componentes.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Los componentes z y w de R1 no se escribirán, ya que el registro de predicado contenía false en los componentes z y w.

La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta el número de ranuras de la instrucción en 1.

También se puede aplicar el registro de predicado a las instrucciones de [callnz Pred](callnz-pred---ps.md) - [PS](if-pred---ps.md)y [breakp-](break-p---ps.md) PS. Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




