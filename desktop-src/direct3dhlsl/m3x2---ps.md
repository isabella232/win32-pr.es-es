---
title: m3x2 - ps
description: Multiplica un vector de tres componentes por una matriz de 3x2. | m3x2 - ps
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59bf908a2858e46f9c1e339db32d3e6e57062bc280b8223a9fcb66a527380773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672645"
---
# <a name="m3x2---ps"></a>m3x2 - ps

Multiplica un vector de tres componentes por una matriz de 3x2.

## <a name="syntax"></a>Syntax



| m3x2 dst, src0, src1 |
|----------------------|



 

where

-   dst es el registro de destino. El resultado es un vector de 2 componentes.
-   src0 es un registro de origen que representa un vector de tres componentes.
-   src1 es un registro de origen que representa una matriz 3x2, que corresponde al primero de dos registros consecutivos.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara xy es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

Las ecuaciones siguientes muestran cómo funciona la instrucción:


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



El vector de entrada está en el registro src0. La matriz de entrada 3x2 está en el registro src1 y el siguiente registro superior en el mismo archivo de registro, como se muestra en la expansión siguiente. Se genera un resultado 2D, lo que deja los demás elementos del registro de destino (dest.z y dest.w) no afectados.

Esta operación se usa normalmente para transformaciones 2D. Esta instrucción se implementa como un par de productos de punto, como se muestra aquí.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Los modificadores swzzle y negate no son válidos para el registro src1. El registro dst y src0, o cualquiera de los registros src1+i, no puede ser el mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




