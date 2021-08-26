---
title: dp2add - ps
description: Realiza un producto de punto 2D y una adición escalar.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39a7cd640de57f2f69c8ee3b46ee6be6e52cbb16f9db39ef902725241d77b9c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068365"
---
# <a name="dp2add---ps"></a>dp2add - ps

Realiza un producto de punto 2D y una adición escalar.

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Donde:

-   dst es un registro de destino.
-   src0, src1 y src2 son tres registros de origen.
-   {x y z w} es la réplica \| necesaria de \| \| swzzle en src2.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

El valor escalar de add lo elige el swzzle de replicación en src2.

El siguiente fragmento de código muestra las operaciones realizadas.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




