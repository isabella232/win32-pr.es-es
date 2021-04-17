---
title: DeducingBlobSetter (D2d1effecthelpers. h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo BLOB.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680606"
---
# <a name="deducingblobsetter"></a><span data-ttu-id="f5fc3-104">DeducingBlobSetter</span><span class="sxs-lookup"><span data-stu-id="f5fc3-104">DeducingBlobSetter</span></span>

<span data-ttu-id="f5fc3-105">Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5fc3-105">Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="f5fc3-106">No se debe llamar a DeducingBlobSetter directamente.</span><span class="sxs-lookup"><span data-stu-id="f5fc3-106">DeducingBlobSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="f5fc3-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5fc3-107">Requirements</span></span>



| <span data-ttu-id="f5fc3-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5fc3-108">Requirement</span></span> | <span data-ttu-id="f5fc3-109">Value</span><span class="sxs-lookup"><span data-stu-id="f5fc3-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fc3-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5fc3-110">Header</span></span><br/> | <dl> <span data-ttu-id="f5fc3-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5fc3-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5fc3-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5fc3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5fc3-113">**Direct2D::D educingBlobGetter**</span><span class="sxs-lookup"><span data-stu-id="f5fc3-113">**Direct2D::DeducingBlobGetter**</span></span>](deducingblobgetter.md)
</dt> </dl>

 

 





