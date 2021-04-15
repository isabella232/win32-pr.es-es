---
title: mova-vs
description: Mueva los datos desde un registro de punto flotante al registro de direcciones, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983898"
---
# <a name="mova---vs"></a>mova-vs

Mueva los datos desde un registro de punto flotante al [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.

## <a name="syntax"></a>Sintaxis



| mova DST, src |
|---------------|



 

, donde

-   DST debe ser el [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| mova                   |      | x    | x    | x     | x    | x     |



 

Mueve los datos de punto flotante a un registro entero. Los valores se convierten del punto flotante utilizando el redondeo al más próximo.

El registro de direcciones es el único registro de destino permitido.

En el siguiente fragmento de código se muestran las operaciones realizadas.


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



En el caso de las versiones 2 \_ x y posteriores, el registro de direcciones es un vector de componente. Por lo tanto, se permite cualquier máscara de escritura.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




