---
title: MOV-vs
description: Mueve los datos de punto flotante entre los registros.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784990"
---
# <a name="mov---vs"></a>MOV-vs

Mueve los datos de punto flotante entre los registros.

## <a name="syntax"></a>Sintaxis



| MOV. DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| MOV                    | x    | x    | x    | x     | x    | x     |



 

Se puede usar para datos de punto flotante. En el caso de la versión frente \_ \_ a 1 1, también se puede utilizar para escribir el registro de direcciones. Cuando se utiliza para actualizar los registros de direcciones, los valores se convierten del punto flotante mediante el redondeo al más próximo.

En el siguiente fragmento de código se muestran las operaciones realizadas.


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

 

 




