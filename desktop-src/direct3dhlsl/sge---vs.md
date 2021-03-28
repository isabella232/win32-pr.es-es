---
title: SGE-vs
description: Calcula el signo si el primer origen es mayor o igual que el segundo origen.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419937"
---
# <a name="sge---vs"></a>SGE-vs

Calcula el signo si el primer origen es mayor o igual que el segundo origen.

## <a name="syntax"></a>Sintaxis



| SGE DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| sge                    | x    | x    | x    | x     | x    | x     |



 

En el siguiente fragmento de código se muestran las operaciones realizadas.


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




