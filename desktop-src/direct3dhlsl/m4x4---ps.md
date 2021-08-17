---
title: m4x4 - ps
description: Multiplica un vector de 4 componentes por una matriz de 4x4. | m4x4 - ps
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7dfba3713bcd376c369a17d4856b64965e2e83c22ff03b282d4c9880d6c8700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906865"
---
# <a name="m4x4---ps"></a>m4x4 - ps

Multiplica un vector de 4 componentes por una matriz de 4x4.

## <a name="syntax"></a>Syntax



| m4x4 dst, src0, src1 |
|----------------------|



 

where

-   dst es el registro de destino. El resultado es un vector de 4 componentes.
-   src0 es un registro de origen que representa un vector de 4 componentes.
-   src1 es un registro de origen que representa una matriz 4x4, que corresponde al primero de cuatro registros consecutivos.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

La máscara xyzw (valor predeterminado) es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

Los modificadores swzzle y negate no son válidos para el registro src0. Los registros dst y src0 no pueden ser los mismos.

El siguiente fragmento de código muestra las operaciones realizadas.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



El vector de entrada está en el registro src0. La matriz 4x4 de entrada se encuentra en el registro src1 y los tres registros superiores siguientes, como se muestra en la expansión siguiente.

Esta operación se usa normalmente para transformar una posición mediante una matriz de proyección. Esta instrucción se implementa como un conjunto de productos de punto, como se muestra aquí.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




