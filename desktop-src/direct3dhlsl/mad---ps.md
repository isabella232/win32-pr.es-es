---
title: mad - ps
description: Multiplicar y agregar instrucciones. Establece el registro de destino en (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241425"
---
# <a name="mad---ps"></a>mad - ps

Multiplicar y agregar instrucciones. Establece el registro de destino en (src0 \* src1) + src2.

## <a name="syntax"></a>Sintaxis



| mad dst, src0, src1, src2 |
|---------------------------|



 

, donde

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.
-   src2 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Enojado                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

El siguiente fragmento de código muestra las operaciones realizadas.


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




