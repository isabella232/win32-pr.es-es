---
title: m4x3 - ps
description: Multiplica un vector de 4 componentes por una matriz de 4x3. | m4x3 - ps
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e291c268aae4173cb3ace4fc00beb5f1a3aa9f0b3d335f80891a851bcab41b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982035"
---
# <a name="m4x3---ps"></a>m4x3 - ps

Multiplica un vector de 4 componentes por una matriz de 4x3.

## <a name="syntax"></a>Syntax



| m4x3 dst, src0, src1 |
|----------------------|



 

where

-   dst es el registro de destino. El resultado es un vector de 3 componentes.
-   src0 es un registro de origen que representa un vector de 4 componentes.
-   src1 es un registro de origen que representa una matriz 4x3, que corresponde al primero de tres registros consecutivos.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara xyz es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

El fragmento de código siguiente muestra las operaciones realizadas.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



El vector de entrada está en el registro src0. La matriz de entrada 4x3 está en el registro src1 y los dos siguientes registros superiores, como se muestra en la expansión siguiente. Se genera un resultado 3D, sin que el otro elemento del registro de destino (dest.w) se ven afectados.

Esta operación se usa normalmente para transformar un vector de posición mediante una matriz que no tiene ningún efecto projective, como ocurre en transformaciones de espacio de modelo. Esta instrucción se implementa como un conjunto de productos de punto, como se muestra a continuación.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Los modificadores swzzle y negate no son válidos para el registro src1. El registro dst y src0 no puede ser el mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




