---
title: dp2add-PS
description: Realiza un producto de punto 2D y una suma escalar.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148987"
---
# <a name="dp2add---ps"></a>dp2add-PS

Realiza un producto de punto 2D y una suma escalar.

## <a name="syntax"></a>Sintaxis


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Donde:

-   DST es un registro de destino.
-   src0, SRC1 y src2 son tres registros de origen.
-   {x \| y \| z \| w} es el swizzle de replicación necesario en src2.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

El valor escalar para Add lo elige replicate swizzle en src2.

En el fragmento de código siguiente se muestran las operaciones realizadas.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




