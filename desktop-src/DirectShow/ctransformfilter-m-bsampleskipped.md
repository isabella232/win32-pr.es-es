---
description: Marca que indica si se ha quitado la muestra más reciente. Si el método Receive quita un ejemplo, establece el valor en TRUE.
ms.assetid: 6143f948-75b0-47c6-9951-4c18c0773857
title: 'Miembro CTransformFilter:: m_bSampleSkipped (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSampleSkipped
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61d8ceda20fed4c8ec89538cbe9675ad1f3e4549
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661031"
---
# <a name="ctransformfilterm_bsampleskipped-member"></a><span data-ttu-id="e3f44-104">Miembro bSampleSkipped CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="e3f44-104">CTransformFilter::m\_bSampleSkipped member</span></span>

<span data-ttu-id="e3f44-105">Marca que indica si se ha quitado la muestra más reciente.</span><span class="sxs-lookup"><span data-stu-id="e3f44-105">Flag that indicates whether the most recent sample was dropped.</span></span> <span data-ttu-id="e3f44-106">Si el método [**Receive**](ctransformfilter-receive.md) quita un ejemplo, establece el valor en **true**.</span><span class="sxs-lookup"><span data-stu-id="e3f44-106">If the [**Receive**](ctransformfilter-receive.md) method drops a sample, it sets the value to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f44-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3f44-107">Syntax</span></span>


```C++
BOOL m_bSampleSkipped;
```



## <a name="requirements"></a><span data-ttu-id="e3f44-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f44-108">Requirements</span></span>



| <span data-ttu-id="e3f44-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f44-109">Requirement</span></span> | <span data-ttu-id="e3f44-110">Value</span><span class="sxs-lookup"><span data-stu-id="e3f44-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f44-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3f44-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e3f44-112"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3f44-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e3f44-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3f44-113">Library</span></span><br/> | <dl> <span data-ttu-id="e3f44-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e3f44-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f44-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3f44-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f44-116">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e3f44-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




