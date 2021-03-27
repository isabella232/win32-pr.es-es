---
title: Agregar vs
description: Agrega dos vectores. | Agregar vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914314"
---
# <a name="add---vs"></a>Agregar vs

Agrega dos vectores.

## <a name="syntax"></a>Sintaxis



| Agregar DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| add                    | x    | x    | x    | x     | x    | x     |



 

En el siguiente fragmento de código se muestran las operaciones realizadas.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




