---
title: m3x2-PS
description: Multiplica un vector de tres componentes por una matriz de 3x2. | m3x2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986688"
---
# <a name="m3x2---ps"></a>m3x2-PS

Multiplica un vector de tres componentes por una matriz de 3x2.

## <a name="syntax"></a>Sintaxis



| m3x2 DST, src0, SRC1 |
|----------------------|



 

, donde

-   DST es el registro de destino. El resultado es un vector de dos componentes.
-   src0 es un registro de origen que representa un vector de tres componentes.
-   SRC1 es un registro de origen que representa una matriz de 3x2, que corresponde al primer de 2 registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara XY es necesaria para el registro de destino. Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.

Las ecuaciones siguientes muestran cómo funciona la instrucción:


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



El vector de entrada se encuentra en el registro src0. La matriz de 3x2 de entrada se encuentra en el registro SRC1 y en el siguiente registro superior en el mismo archivo de registro, tal como se muestra en la siguiente expansión. Se genera un resultado 2D, lo que no afecta a los demás elementos del registro de destino (dest. z y dest. w).

Esta operación se utiliza normalmente para las transformaciones 2D. Esta instrucción se implementa como un par de productos DOT como se muestra aquí.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Los modificadores swizzle y Negate no son válidos para el registro SRC1. El registro de DST y src0, o cualquiera de los registros de SRC1 + i, no puede ser el mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




