---
description: La \_ variable miembro m bModifiesData indica si el filtro modifica los datos de ejemplo que recibe. El valor se establece en el constructor CTransInPlaceFilter, pero su valor predeterminado es TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Miembro CTransInPlaceFilter:: m_bModifiesData (TRANSip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660607"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="b225e-104">Miembro bModifiesData CTransInPlaceFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="b225e-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="b225e-105">La `m_bModifiesData` variable miembro indica si el filtro modifica los datos de ejemplo que recibe.</span><span class="sxs-lookup"><span data-stu-id="b225e-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="b225e-106">El valor se establece en el constructor **CTransInPlaceFilter** , pero su valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="b225e-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b225e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b225e-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="b225e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b225e-108">Remarks</span></span>

<span data-ttu-id="b225e-109">Esta variable afecta a cómo el filtro negocia el asignador.</span><span class="sxs-lookup"><span data-stu-id="b225e-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="b225e-110">Si el valor es **true**, el filtro no puede usar un asignador de solo lectura para ambas conexiones de PIN.</span><span class="sxs-lookup"><span data-stu-id="b225e-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="b225e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b225e-111">Requirements</span></span>



| <span data-ttu-id="b225e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b225e-112">Requirement</span></span> | <span data-ttu-id="b225e-113">Value</span><span class="sxs-lookup"><span data-stu-id="b225e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b225e-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b225e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b225e-115"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b225e-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b225e-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b225e-116">Library</span></span><br/> | <dl> <span data-ttu-id="b225e-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b225e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b225e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b225e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b225e-119">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="b225e-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




