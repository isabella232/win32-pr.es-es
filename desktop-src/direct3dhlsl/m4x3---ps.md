---
title: m4x3-PS
description: Multiplica un vector de cuatro componentes por una matriz de 4x3. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986627"
---
# <a name="m4x3---ps"></a>m4x3-PS

Multiplica un vector de cuatro componentes por una matriz de 4x3.

## <a name="syntax"></a>Sintaxis



| m4x3 DST, src0, SRC1 |
|----------------------|



 

, donde

-   DST es el registro de destino. El resultado es un vector de tres componentes.
-   src0 es un registro de origen que representa un vector de 4 componentes.
-   SRC1 es un registro de origen que representa una matriz de 4x3, que corresponde al primer de 3 registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara XYZ es necesaria para el registro de destino. Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.

En el fragmento de código siguiente se muestran las operaciones realizadas.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



El vector de entrada se encuentra en el registro src0. La matriz de 4x3 de entrada se encuentra en el registro SRC1 y en los dos registros posteriores siguientes, tal como se muestra en la siguiente expansión. Se genera un resultado 3D, lo que no afecta al otro elemento del registro de destino (dest. w).

Esta operación se utiliza normalmente para transformar un vector de posición por una matriz que no tiene ningún efecto proyectado, como ocurre en las transformaciones de espacio de modelo. Esta instrucción se implementa como un conjunto de productos de puntos, como se muestra a continuación.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Los modificadores swizzle y Negate no son válidos para el registro SRC1. El registro de DST y src0 no puede ser el mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




