---
title: M4x4-vs
description: Multiplica un vector de cuatro componentes por una matriz de 4x4. | M4x4-vs
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279996"
---
# <a name="m4x4---vs"></a>M4x4-vs

Multiplica un vector de cuatro componentes por una matriz de 4x4.

## <a name="syntax"></a>Sintaxis



| M4x4 DST, src0, SRC1 |
|----------------------|



 

, donde

-   DST es el registro de destino. El resultado es un vector de cuatro componentes.
-   src0 es un registro de origen que representa un vector de 4 componentes.
-   SRC1 es un registro de origen que representa una matriz de 4x4, que corresponde al primer de 4 registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m4x4                   | x    | x    | x    | x     | x    | x     |



 

Se necesita la máscara xyzw (valor predeterminado) para el registro de destino. Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.

Los modificadores swizzle y Negate no son válidos para el registro src0. Los registros dest y src0 no pueden ser iguales.

En el siguiente fragmento de código se muestran las operaciones realizadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



El vector de entrada se encuentra en el registro src0. La matriz 4x4 de entrada está en el registro SRC1 y los tres registros superiores siguientes, tal como se muestra en la siguiente expansión.

Esta operación se utiliza normalmente para transformar una posición por una matriz de proyección. Esta instrucción se implementa como una serie de productos de puntos, como se muestra aquí.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




