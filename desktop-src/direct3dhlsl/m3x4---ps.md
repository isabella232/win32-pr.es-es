---
title: M3x4-PS
description: Multiplica un vector de tres componentes por una matriz de 3x4. | M3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986639"
---
# <a name="m3x4---ps"></a>M3x4-PS

Multiplica un vector de tres componentes por una matriz de 3x4.

## <a name="syntax"></a>Sintaxis



| M3x4 DST, src0, SRC1 |
|----------------------|



 

, donde

-   DST es el registro de destino. El resultado es un vector de cuatro componentes.
-   src0 es un registro de origen que representa un vector de tres componentes.
-   SRC1 es un registro de origen que representa una matriz de 3x4, que se corresponde con el primero de 4 registros consecutivos.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Se necesita la máscara xyzw (valor predeterminado) para el registro de destino. Los modificadores Negate y swizzle se permiten para src0, pero no para SRC1.

En el fragmento de código siguiente se muestran las operaciones realizadas.


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



El vector de entrada se encuentra en el registro src0. La matriz de 3x4 de entrada se encuentra en el registro SRC1 y en los dos registros posteriores siguientes, tal como se muestra en la siguiente expansión.

Esta operación se utiliza normalmente para transformar un vector de posición por una matriz que tiene un efecto proyectado pero no aplica ninguna traducción. Esta instrucción se implementa como un par de productos DOT como se muestra aquí.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




