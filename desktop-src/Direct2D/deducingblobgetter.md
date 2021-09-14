---
title: DeducingBlobGetter (D2d1effecthelpers.h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del getter de propiedad de función miembro para una propiedad de tipo blob.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- DeducingBlobGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ca5cc37a9fbd79807e258a87a199be7319ce3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163438"
---
# <a name="deducingblobgetter"></a>DeducingBlobGetter

Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del getter de propiedad de función miembro para una propiedad de tipo blob.

> [!Note]  
> No se debe llamar directamente a DeducingBlobGetter.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Direct2D::D educingBlobSetter**](deducingblobsetter.md)
</dt> </dl>

 

 





