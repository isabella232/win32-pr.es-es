---
title: lrp- vs
description: Interpola linealmente entre el segundo y el tercer registro de origen en una proporción especificada en el primer registro de origen. | lrp- vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d154f78b3e8ae5d3b7b8e553435d962ad3dbea9fe86f8dd772bf165c5eb542be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119189"
---
# <a name="lrp---vs"></a>lrp- vs

Interpola linealmente entre el segundo y el tercer registro de origen en una proporción especificada en el primer registro de origen.

## <a name="syntax"></a>Syntax



| lrp dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Lrp                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción realiza la interpolación lineal en función de la fórmula siguiente.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




