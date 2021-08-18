---
title: mova- vs
description: Mueva los datos de un registro de punto flotante al registro de direcciones, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dec849009ee47b4aaef1bc3766e2b141a8a6ccf5e17b16a370c6ea8284eaf957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986335"
---
# <a name="mova---vs"></a>mova- vs

Mueva los datos de un registro de punto flotante al registro [de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Syntax



| mova dst, src |
|---------------|



 

where

-   dst debe ser el [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Mova                   |      | x    | x    | x     | x    | x     |



 

Mueve los datos de punto flotante a un registro entero. Los valores se convierten de punto flotante mediante redondeo a más cercano.

El registro de direcciones es el único registro de destino permitido.

El fragmento de código siguiente muestra las operaciones realizadas.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Para las versiones 2 \_ x y posteriores, el registro de direcciones es un vector de componente. Por lo tanto, se permite cualquier máscara de escritura.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




