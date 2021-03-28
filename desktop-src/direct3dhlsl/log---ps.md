---
title: 'registro: PS'
description: '₂ de registro de precisión completa (x). | registro: PS'
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986689"
---
# <a name="log---ps"></a>registro: PS

₂ de registro de precisión completa (x).

## <a name="syntax"></a>Sintaxis



| DST de registro, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swizzle; es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

En el fragmento de código siguiente se muestran las operaciones realizadas.


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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




