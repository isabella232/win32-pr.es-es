---
title: CMP-PS
description: Elija SRC1 si src0 0. De lo contrario, elija src2. La comparación se realiza por canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077089"
---
# <a name="cmp---ps"></a>CMP-PS

Elija SRC1 si src0 >= 0. De lo contrario, elija src2. La comparación se realiza por canal.

## <a name="syntax"></a>Sintaxis



| CMP DST, src0, SRC1, src2 |
|---------------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CMP                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Existen algunas limitaciones adicionales para las versiones 1 \_ 2 y 1 \_ 3:

-   Cada sombreador puede utilizar hasta tres instrucciones de CMP como máximo.
-   El registro de destino no puede ser el mismo que ninguno de los registros de origen.

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

 

 




