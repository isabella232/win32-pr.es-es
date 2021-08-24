---
title: cnd - ps
description: Elige condicionalmente entre src1 y src2, en función de la comparación src0 0.5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726965"
---
# <a name="cnd---ps"></a>cnd - ps

Elige condicionalmente entre src1 y src2, en función de la comparación src0 > 0.5.

## <a name="syntax"></a>Syntax



| cnd dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

Para las versiones \_ 1 1 a 1 \_ 3, src0 debe ser r0.a.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



La versión 1 \_ 4 compara cada canal por separado.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



Estos ejemplos muestran una comparación de cuatro canales realizada en un sombreador de la versión 1 4, así como una comparación de un solo canal posible en un sombreador de la versión \_ \_ 1 1.


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



La versión 1 1 a 1 3 solo se compara con el canal alfa replicado \_ \_ de r0.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



En este ejemplo se comparan dos valores, A y B. En el ejemplo se supone que A se carga en v0 y B se carga en v1. Tanto A como B deben estar en el intervalo de -1 a +1 y, dado que los registros de color (vn) se definen para estar entre 0 y 1, la restricción se cumple en este ejemplo.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




