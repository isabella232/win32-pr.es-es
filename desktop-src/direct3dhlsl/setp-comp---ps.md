---
title: 'setp_comp: ps'
description: 'Establezca el registro del predicado. | setp_comp: ps'
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d278a6104a6c47d84623b185f78b921d61899f296eeaa557a6c6c6d5344097b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119487085"
---
# <a name="setp_comp---ps"></a>setp \_ comp - ps

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

    

     

-   dst es el [registro de registro de](dx9-graphics-reference-asm-ps-registers-predicate.md) predicado, p0.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| setp \_ comp            |      |      |      |      |      | x    | x     | x    | x     |



 

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

El registro dst debe ser el registro de predicado.

## <a name="applying-the-predicate-register"></a>Aplicación del registro de predicado

Una vez que el registro de predicado se ha inicializado con setp comp, se puede usar \_ para controlar una instrucción por componente. Esta es la sintaxis:


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



Donde:

-   \[!\] es un valor booleano opcional NOT
-   p0 es el registro de predicado
-   \[.swzzle es un swlino opcional que se aplica al contenido del registro de predicado antes de usarlo \] para enmascarar la instrucción. Los swiques disponibles son: .xyzw (valor predeterminado cuando no se especifica ninguno) o cualquier swzzle de replicación: .x/.r, .y/.g, .z/.b o .a/.w.
-   instruction es cualquier instrucción aritmética o de textura. No puede ser una instrucción de control de flujo estático o dinámico.
-   dest, src0, ... son los registros requeridos por la instrucción

Suponiendo que el registro de predicado se ha configurado con valores de componente (true, true, false, false), se puede aplicar a esta instrucción:


```
(p0) add r1, r2, r3
```



para realizar una adición de 2 componentes.


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



Los componentes z y w de r1 no se escribirán porque el registro de predicado contenía false en los componentes z y w.

La aplicación del registro de predicado a una instrucción aritmética o de textura aumenta su recuento de ranuras de instrucciones en 1.

El registro de predicado también se puede aplicar a si [pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) y [breakp - ps](break-p---ps.md) instructions. Estas instrucciones de control de flujo no tienen ningún aumento en el recuento de ranuras de instrucciones cuando se usa el registro de predicado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




