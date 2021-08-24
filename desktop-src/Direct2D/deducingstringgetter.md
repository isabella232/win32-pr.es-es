---
title: DeducingStringGetter (D2d1effecthelpers.h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del getter de la propiedad member-function para una propiedad de tipo cadena.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- DeducingStringGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99e23a2f79f38527dfae76c74e5e2ad8b828dce1a0ff984f622bd95fd287c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342965"
---
# <a name="deducingstringgetter"></a>DeducingStringGetter

Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del getter de la propiedad member-function para una propiedad de tipo cadena.

> [!Note]  
> No se debe llamar directamente a DeducingStringGetter.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Direct2D::D educingStringSetter**](deducingstringsetter.md)
</dt> </dl>

 

 





