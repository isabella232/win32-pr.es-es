---
title: BlobSetter (D2d1effecthelpers. h)
description: Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo de BLOB.
ms.assetid: 29411D53-1D27-4040-A3C0-B1511E627A32
keywords:
- BlobSetter Direct2D
topic_type:
- apiref
api_name:
- BlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a073db2fb53fa86414ed6081ede0e24c2eb7dcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660211"
---
# <a name="blobsetter"></a><span data-ttu-id="57bb0-104">BlobSetter</span><span class="sxs-lookup"><span data-stu-id="57bb0-104">BlobSetter</span></span>

<span data-ttu-id="57bb0-105">Llama a una devolución de llamada del establecedor de propiedad de función miembro para una propiedad de tipo de BLOB.</span><span class="sxs-lookup"><span data-stu-id="57bb0-105">Calls a member-function property setter callback for a blob-type property.</span></span>

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobSetter(
    _In_ IUnknown *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="57bb0-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57bb0-106">Requirements</span></span>



| <span data-ttu-id="57bb0-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="57bb0-107">Requirement</span></span> | <span data-ttu-id="57bb0-108">Value</span><span class="sxs-lookup"><span data-stu-id="57bb0-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57bb0-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57bb0-109">Header</span></span><br/> | <dl> <span data-ttu-id="57bb0-110"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="57bb0-110"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57bb0-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="57bb0-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bb0-112">**Direct2D:: BlobGetter**</span><span class="sxs-lookup"><span data-stu-id="57bb0-112">**Direct2D::BlobGetter**</span></span>](blobgetter.md)
</dt> </dl>

 

 





