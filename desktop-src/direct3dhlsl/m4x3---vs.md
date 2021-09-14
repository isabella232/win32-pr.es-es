---
title: 'm4x3: vs'
description: 'Multiplica un vector de 4 componentes por una matriz de 4x3. | m4x3: vs'
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241419"
---
# <a name="m4x3---vs"></a>m4x3: vs

Multiplica un vector de 4 componentes por una matriz de 4x3.

## <a name="syntax"></a>Sintaxis



| m4x3 dst, src0, src1 |
|----------------------|



 

, donde

-   dst es el registro de destino. El resultado es un vector de 3 componentes.
-   src0 es un registro de origen que representa un vector de 4 componentes.
-   src1 es un registro de origen que representa una matriz 4x3, que corresponde al primero de tres registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

La máscara xyz es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

El fragmento de código siguiente muestra las operaciones realizadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



El vector de entrada está en el registro src0. La matriz de entrada 4x3 está en el registro src1 y los dos registros siguientes superiores, como se muestra en la expansión siguiente. Se genera un resultado 3D, sin que el otro elemento del registro de destino (dest.w) se ven afectados.

Esta operación se usa normalmente para transformar un vector de posición mediante una matriz que no tiene ningún efecto projective, como ocurre en transformaciones de espacio de modelo. Esta instrucción se implementa como un par de productos de punto, como se muestra a continuación.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Los modificadores swzzle y negate no son válidos para el registro src1. El registro dst y src0 no puede ser el mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




