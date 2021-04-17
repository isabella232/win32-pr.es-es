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
# <a name="deducingstringsetter"></a><span data-ttu-id="d65f9-104">DeducingStringSetter</span><span class="sxs-lookup"><span data-stu-id="d65f9-104">DeducingStringSetter</span></span>

<span data-ttu-id="d65f9-105">Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del establecedor de la propiedad de función miembro para una propiedad de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="d65f9-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="d65f9-106">No se debe llamar a DeducingStringSetter directamente.</span><span class="sxs-lookup"><span data-stu-id="d65f9-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="d65f9-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d65f9-107">Requirements</span></span>



| <span data-ttu-id="d65f9-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d65f9-108">Requirement</span></span> | <span data-ttu-id="d65f9-109">Value</span><span class="sxs-lookup"><span data-stu-id="d65f9-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d65f9-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d65f9-110">Header</span></span><br/> | <dl> <span data-ttu-id="d65f9-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="d65f9-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d65f9-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="d65f9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d65f9-113">**Direct2D::D educingStringGetter**</span><span class="sxs-lookup"><span data-stu-id="d65f9-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





