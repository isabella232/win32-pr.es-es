---
title: m3x3- vs
description: Multiplica un vector de 3 componentes por una matriz de 3x3. | m3x3- vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241437"
---
# <a name="m3x3---vs"></a>m3x3- vs

Multiplica un vector de 3 componentes por una matriz de 3x3.

## <a name="syntax"></a>Sintaxis



| m3x3 dst, src0, src1 |
|----------------------|



 

, donde

-   dst es el registro de destino. El resultado es un vector de 3 componentes.
-   src0 es un registro de origen que representa un vector de 3 componentes.
-   src1 es un registro de origen que representa una matriz 3x3, que corresponde al primero de tres registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

La máscara xyz es necesaria para el registro de destino. Se permiten modificadores negate y swzzle para src0, pero no para src1.

El fragmento de código siguiente muestra las operaciones realizadas.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



El vector de entrada está en el registro src0. La matriz de entrada 3x3 está en el registro src1 y los dos siguientes registros superiores, como se muestra en la expansión siguiente. Se genera un resultado 3D, sin que el otro elemento del registro de destino (dest.w) se ven afectados.

Esta operación se usa normalmente para transformar vectores normales durante los cálculos de iluminación. Esta instrucción se implementa como un par de productos de punto, como se muestra a continuación.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




