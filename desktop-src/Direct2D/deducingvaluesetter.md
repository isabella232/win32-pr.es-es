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
ms.openlocfilehash: bfba4f6123b9e097d5c9c5fedb2e872974fc3d15a5c54464eca4ae6e27c3048c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108865"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Direct2D::D educingValueGetter**](deducingvaluegetter.md)
</dt> </dl>

 

 





