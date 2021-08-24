---
title: 'm3x4: vs'
description: 'Multiplica un vector de 3 componentes por una matriz de 3x4. | m3x4: vs'
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54137f2081a48158d306e882eab0dc912a8e50332b7d66cfb137c3c10b669570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457435"
---
# <a name="m3x4---vs"></a>m3x4: vs

Multiplica un vector de 3 componentes por una matriz de 3x4.

## <a name="syntax"></a>Syntax



| m3x4 dst, src0, src1 |
|----------------------|



 

where

-   dst es el registro de destino. El resultado es un vector de 4 componentes.
-   src0 es un registro de origen que representa un vector de 3 componentes.
-   src1 es un registro de origen que representa una matriz 3x4, que corresponde al primero de cuatro registros consecutivos.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

La máscara xyzw (valor predeterminado) es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

El fragmento de código siguiente muestra las operaciones realizadas.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



El vector de entrada está en el registro src0. La matriz de entrada 3x4 está en el registro src1 y los tres registros siguientes superiores, como se muestra en la expansión siguiente.

Esta operación se usa normalmente para transformar un vector de posición mediante una matriz que tiene un efecto projective pero no aplica ninguna traducción. Esta instrucción se implementa como un par de productos de punto, como se muestra aquí.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




