---
title: BlobGetter (D2d1effecthelpers. h)
description: Llama a una devolución de llamada de captador de propiedad de función miembro para una propiedad de tipo de BLOB.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660213"
---
# <a name="blobgetter"></a>BlobGetter

Llama a una devolución de llamada de captador de propiedad de función miembro para una propiedad de tipo de BLOB.

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
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Direct2D:: BlobSetter**](blobsetter.md)
</dt> </dl>

 

 





