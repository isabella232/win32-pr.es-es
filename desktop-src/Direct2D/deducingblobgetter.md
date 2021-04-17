---
title: DeducingBlobGetter (D2d1effecthelpers. h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de BLOB.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680607"
---
# <a name="deducingblobgetter"></a><span data-ttu-id="0faa0-104">DeducingBlobGetter</span><span class="sxs-lookup"><span data-stu-id="0faa0-104">DeducingBlobGetter</span></span>

<span data-ttu-id="0faa0-105">Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0faa0-105">Deduces the class and arguments and then calls a member-function property getter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="0faa0-106">No se debe llamar a DeducingBlobGetter directamente.</span><span class="sxs-lookup"><span data-stu-id="0faa0-106">DeducingBlobGetter should not be called directly.</span></span>

 

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

## <a name="requirements"></a><span data-ttu-id="0faa0-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0faa0-107">Requirements</span></span>



| <span data-ttu-id="0faa0-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="0faa0-108">Requirement</span></span> | <span data-ttu-id="0faa0-109">Value</span><span class="sxs-lookup"><span data-stu-id="0faa0-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0faa0-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0faa0-110">Header</span></span><br/> | <dl> <span data-ttu-id="0faa0-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="0faa0-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0faa0-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="0faa0-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faa0-113">**Direct2D::D educingBlobSetter**</span><span class="sxs-lookup"><span data-stu-id="0faa0-113">**Direct2D::DeducingBlobSetter**</span></span>](deducingblobsetter.md)
</dt> </dl>

 

 





