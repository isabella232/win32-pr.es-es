---
title: DeducingStringSetter (D2d1effecthelpers. h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo cadena.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- DeducingStringSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680356"
---
# <a name="deducingstringsetter"></a>DeducingStringSetter

Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo cadena.

> [!Note]  
> No se debe llamar a DeducingStringSetter directamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Direct2D::D educingStringGetter**](deducingstringgetter.md)
</dt> </dl>

 

 





