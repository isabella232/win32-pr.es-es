---
title: 'mov : frente a'
description: Mover datos de punto flotante entre registros.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dd3e476c871bf2c8d1e48075a3f43576283efff1df285f900c6d0194cf4bbbfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906736"
---
# <a name="mov---vs"></a>mov : frente a

Mover datos de punto flotante entre registros.

## <a name="syntax"></a>Syntax



| mov dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Mov                    | x    | x    | x    | x     | x    | x     |



 

Se puede usar para datos de punto flotante. Para la versión \_ 1 \_ frente a la 1, también se puede usar para escribir el registro de direcciones. Cuando se usan para actualizar los registros de direcciones, los valores se convierten de punto flotante mediante redondeo a más cercano.

El fragmento de código siguiente muestra las operaciones realizadas.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




