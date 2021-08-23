---
title: 'logp: vs'
description: Logpción de precisión parcial(x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c33242ec23070a78e8adee159d35c19121dcc7c3dfe2c013c3d00adceb16477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043783"
---
# <a name="logp---vs"></a>logp: vs

Logpción de precisión parcial(x).

## <a name="syntax"></a>Syntax



| logp dst, src |
|---------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Logp                   | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas.


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



Esta instrucción proporciona una precisión parcial de logaritmo base 2, hasta 10 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




