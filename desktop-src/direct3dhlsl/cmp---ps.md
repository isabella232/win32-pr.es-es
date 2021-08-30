---
title: cmp - ps
description: Elija src1 si src0 0. De lo contrario, elija src2. La comparación se realiza por canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7cafc386d56995eafee5541a02a6ec2d22201b7689a83f79a4e818b1741ed17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983285"
---
# <a name="cmp---ps"></a>cmp - ps

Elija src1 si src0 >= 0. De lo contrario, elija src2. La comparación se realiza por canal.

## <a name="syntax"></a>Syntax



| cmp dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Cmp                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Existen algunas limitaciones adicionales para las versiones 1 \_ 2 y 1 \_ 3:

-   Cada sombreador puede usar hasta un máximo de tres instrucciones de cmp.
-   El registro de destino no puede ser el mismo que cualquiera de los registros de origen.

En este ejemplo se realiza una comparación de cuatro canales.


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




