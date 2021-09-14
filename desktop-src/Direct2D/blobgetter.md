---
title: BlobGetter (D2d1effecthelpers.h)
description: Llama a una devolución de llamada del obtienedor de propiedad de función miembro para una propiedad de tipo blob.
ms.assetid: 55A41BE4-2AAE-480B-A143-86E8E7533210
keywords:
- BlobGetter Direct2D
topic_type:
- apiref
api_name:
- BlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c638501c9c15abc2f895003fd79c481fd0e05b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164238"
---
# <a name="blobgetter"></a>BlobGetter

Llama a una devolución de llamada del obtienedor de propiedad de función miembro para una propiedad de tipo blob.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobGetter(
    _In_ const IUnknown *effect,
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

[**Direct2D::BlobSetter**](blobsetter.md)
</dt> </dl>

 

 





