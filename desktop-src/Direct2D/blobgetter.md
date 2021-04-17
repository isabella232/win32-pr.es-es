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
# <a name="blobgetter"></a><span data-ttu-id="5eb37-104">BlobGetter</span><span class="sxs-lookup"><span data-stu-id="5eb37-104">BlobGetter</span></span>

<span data-ttu-id="5eb37-105">Llama a una devolución de llamada de captador de propiedad de función miembro para una propiedad de tipo de BLOB.</span><span class="sxs-lookup"><span data-stu-id="5eb37-105">Calls a member-function property getter callback for a blob-type property.</span></span>

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobGetter(
    _In_ const IUnknown *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="5eb37-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eb37-106">Requirements</span></span>



| <span data-ttu-id="5eb37-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb37-107">Requirement</span></span> | <span data-ttu-id="5eb37-108">Value</span><span class="sxs-lookup"><span data-stu-id="5eb37-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb37-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5eb37-109">Header</span></span><br/> | <dl> <span data-ttu-id="5eb37-110"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eb37-110"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb37-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="5eb37-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb37-112">**Direct2D:: BlobSetter**</span><span class="sxs-lookup"><span data-stu-id="5eb37-112">**Direct2D::BlobSetter**</span></span>](blobsetter.md)
</dt> </dl>

 

 





