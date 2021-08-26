---
title: dst - vs
description: Calcula un vector de distancia. | dst - vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d75eb61dd498d7a2f1d6bd9c5bd0dd9c52f3fd56625cb41b0026e9acce431ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068355"
---
# <a name="dst---vs"></a>dst - vs

Calcula un vector de distancia.

## <a name="syntax"></a>Syntax



| dst dest, src0, src1 |
|----------------------|



 

where

-   dest es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dst                    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Se supone que el primer operando de origen (src0) es el vector (omitido, d d, d d, omitido) y que el segundo operando de origen \* \* (src1) es el vector (omitido, 1/d, omitido, 1/d). El destino (dest) es el vector de resultado (1, d, \* d, 1/d).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




