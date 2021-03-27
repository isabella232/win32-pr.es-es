---
title: DST-vs
description: Calcula un vector de distancia. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914345"
---
# <a name="dst---vs"></a>DST-vs

Calcula un vector de distancia.

## <a name="syntax"></a>Sintaxis



| DST Dest, src0, SRC1 |
|----------------------|



 

, donde

-   dest es el registro de destino.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DST                    | x    | x    | x    | x     | x    | x     |



 

En el siguiente fragmento de código se muestran las operaciones realizadas:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Se supone que el primer operando de origen (src0) es el vector (omitido, d d \* , d d \* , omitido) y el segundo operando de origen (SRC1) es el vector (omitido, 1/d, omitido, 1/d). El destino (DEST) es el vector del resultado (1, d, d \* d, 1/d).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




