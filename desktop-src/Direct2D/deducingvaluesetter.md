---
title: DeducingValueSetter (D2d1effecthelpers.h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del setter de propiedad de función miembro para una propiedad de tipo de valor.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- DeducingValueSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163421"
---
# <a name="deducingvaluesetter"></a>DeducingValueSetter

Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del setter de propiedad de función miembro para una propiedad de tipo de valor.

> [!Note]  
> No se debe llamar directamente a DeducingValueSetter.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Direct2D::D educingValueGetter**](deducingvaluegetter.md)
</dt> </dl>

 

 





