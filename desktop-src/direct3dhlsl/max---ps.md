---
title: max - ps
description: Calcula el máximo de los orígenes. | max - ps
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241413"
---
# <a name="max---ps"></a>max - ps

Calcula el máximo de los orígenes.

## <a name="syntax"></a>Sintaxis



| max dst, src0, src1 |
|---------------------|



 

, donde

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| max                   |      |      |      |      | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas.


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




