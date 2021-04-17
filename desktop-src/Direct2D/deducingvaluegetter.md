---
title: DeducingValueGetter (D2d1effecthelpers. h)
description: Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de valor.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- DeducingValueGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660331"
---
# <a name="deducingvaluegetter"></a><span data-ttu-id="f2482-104">DeducingValueGetter</span><span class="sxs-lookup"><span data-stu-id="f2482-104">DeducingValueGetter</span></span>

<span data-ttu-id="f2482-105">Deduce la clase y los argumentos y, a continuación, llama a una devolución de llamada del captador de propiedad de función miembro para una propiedad de tipo de valor.</span><span class="sxs-lookup"><span data-stu-id="f2482-105">Deduces the class and arguments and then calls a member-function property getter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="f2482-106">No se debe llamar a DeducingValueGetter directamente.</span><span class="sxs-lookup"><span data-stu-id="f2482-106">DeducingValueGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="f2482-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2482-107">Requirements</span></span>



| <span data-ttu-id="f2482-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2482-108">Requirement</span></span> | <span data-ttu-id="f2482-109">Value</span><span class="sxs-lookup"><span data-stu-id="f2482-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2482-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2482-110">Header</span></span><br/> | <dl> <span data-ttu-id="f2482-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2482-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2482-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2482-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2482-113">**Direct2D::D educingValueSetter**</span><span class="sxs-lookup"><span data-stu-id="f2482-113">**Direct2D::DeducingValueSetter**</span></span>](deducingvaluesetter.md)
</dt> </dl>

 

 





