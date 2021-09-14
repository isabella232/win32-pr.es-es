---
title: log- vs
description: Registro de precisión completa( x). | log- vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974263"
---
# <a name="log---vs"></a>log- vs

Registro de precisión completa( x).

## <a name="syntax"></a>Sintaxis



| log dst, src |
|--------------|



 

, donde

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| log                    | x    | x    | x    | x     | x    | x     |



 

El fragmento de código siguiente muestra las operaciones realizadas.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Esta instrucción acepta un origen escalar cuyo bit de signo se omite. El resultado se replica en los cuatro canales.

Esta instrucción proporciona 21 bits de precisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




