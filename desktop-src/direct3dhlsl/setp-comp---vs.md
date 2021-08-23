---
title: 'setp_comp : frente a'
description: 'Establezca el registro del predicado. | setp_comp : vs'
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 892acf44000e178e7ed6774a3841760db32e3ced4d8348a7f9e9c22969bf9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671775"
---
# <a name="setp_comp---vs"></a>setp \_ comp - vs

Establezca el registro del predicado.

## <a name="syntax"></a>Syntax



| setp \_ comp dst, src0, src1 |
|----------------------------|



 

Donde:

-   \_comp es una comparación por canal entre los dos registros de origen. Puede tener uno de los valores siguientes: 

    | Syntax | De comparación            |
    |--------|-----------------------|
    | \_Gt   | Mayor que          |
    | \_Lt   | Menor que             |
    | \_Ge   | Mayor o igual que |
    | \_le   | Menor o igual que    |
    | \_Eq   | Igual a              |
    | \_Ne   | No es igual a          |

    

     

-   dst es el [registro de registro de](dx9-graphics-reference-asm-vs-registers-predicate.md) predicado, p0.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| setp \_ comp             |      |      | x    | x     | x    | x     |



 

Esta instrucción funciona como:


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



Para cada canal que se pueda escribir según la máscara de escritura de destino, guarde el resultado booleano de la operación de comparación entre los canales correspondientes de src0 y src1 (después de que se haya resuelto el modificador de origen swlinos).

Los registros de origen permiten especificar componentes arbitrarios.

El registro de destino permite máscaras de escritura arbitrarias.

El registro dest debe ser el registro de predicado.

## <a name="applying-the-predicate-register"></a>Aplicación del registro de predicado

Una vez que el registro de predicado se ha inicializado con setp, se puede usar para controlar una instrucción por componente. Esta es la sintaxis:


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



Donde:

-   \[!\] es un valor booleano opcional NOT
-   p0 es el registro de predicado
-   \[.swzzle es un swlino opcional que se aplica al contenido del registro de predicado antes de usarlo \] para enmascarar la instrucción. Los swiques disponibles son: .xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swzzle de replicación: .x/.r, .y/.g, .z/.b o .a/.w.
-   instruction es cualquier instrucción aritmética o de textura. No puede ser una instrucción de control de flujo estático o dinámico.
-   dest, srcReg, ... son los registros requeridos por la instrucción

Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



para realizar una adición de 2 componentes.


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



Los componentes x e y de r2 no se escribirán porque el registro de predicado contenía false en los componentes z y w.

La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta su recuento de ranuras de instrucciones en 1.

El registro de predicado también se puede aplicar a si [pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) y [breakp - vs](breakp---vs.md) instructions. Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




