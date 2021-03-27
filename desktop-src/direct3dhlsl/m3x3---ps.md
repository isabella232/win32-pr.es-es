---
title: M3x3-PS
description: Multiplica un vector de tres componentes por una matriz de 3x3. | M3x3-PS
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ac72acd2133c8b34393bdd1ab7de8aec1df4db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986615"
---
# <a name="m3x3---ps"></a>M3x3-PS

Multiplica un vector de tres componentes por una matriz de 3x3.

## <a name="syntax"></a>Sintaxis



| M3x3 DST, src0, SRC1 |
|----------------------|



 

, donde

-   DST es el registro de destino. El resultado es un vector de tres componentes.
-   src0 es un registro de origen que representa un vector de tres componentes.
-   SRC1 es un registro de origen que representa una matriz de 3x3, que corresponde al primer de 3 registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara XYZ es necesaria para el registro de destino. Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.

En el fragmento de código siguiente se muestran las operaciones realizadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



El vector de entrada se encuentra en el registro src0. La matriz de 3x3 de entrada está en el registro SRC1 y los dos registros más altos siguientes, como se muestra en la siguiente expansión. Se genera un resultado 3D, lo que no afecta al otro elemento del registro de destino (dest. w).

Esta operación se utiliza normalmente para transformar vectores normales durante los cálculos de iluminación. Esta instrucción se implementa como un conjunto de productos de puntos, como se muestra a continuación.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




