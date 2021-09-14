---
title: DeducingBlobSetter (D2d1effecthelpers.h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del setter de la propiedad member-function para una propiedad de tipo blob.
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- DeducingBlobSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d3bbfcc0a48d722bd98456821d7f7df5e8780a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163434"
---
# <a name="deducingblobsetter"></a>DeducingBlobSetter

Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del setter de la propiedad member-function para una propiedad de tipo blob.

> [!Note]  
> No se debe llamar directamente a DeducingBlobSetter.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Direct2D::D educingBlobGetter**](deducingblobgetter.md)
</dt> </dl>

 

 





