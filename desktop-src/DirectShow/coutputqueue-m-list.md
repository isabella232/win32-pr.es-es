---
description: Cola de ejemplo multimedia.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Miembro COutputQueue:: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680221"
---
# <a name="coutputqueuem_list-member"></a><span data-ttu-id="575a5-103">Miembro de la lista COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="575a5-103">COutputQueue::m\_List member</span></span>

<span data-ttu-id="575a5-104">Cola de ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="575a5-104">Media sample queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="575a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="575a5-105">Syntax</span></span>


```C++
CSampleList *m_List;
```



## <a name="remarks"></a><span data-ttu-id="575a5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="575a5-106">Remarks</span></span>

<span data-ttu-id="575a5-107">Esta variable miembro es un puntero a un objeto [**CGenericList**](cgenericlist.md) que contiene punteros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="575a5-107">This member variable is a pointer to a [**CGenericList**](cgenericlist.md) object that holds [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers.</span></span> <span data-ttu-id="575a5-108">El tipo **CSampleList** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="575a5-108">The **CSampleList** type is defined as follows:</span></span>

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a><span data-ttu-id="575a5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575a5-109">Requirements</span></span>



| <span data-ttu-id="575a5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="575a5-110">Requirement</span></span> | <span data-ttu-id="575a5-111">Value</span><span class="sxs-lookup"><span data-stu-id="575a5-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575a5-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="575a5-112">Header</span></span><br/>  | <dl> <span data-ttu-id="575a5-113"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="575a5-113"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="575a5-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="575a5-114">Library</span></span><br/> | <dl> <span data-ttu-id="575a5-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="575a5-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575a5-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="575a5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575a5-117">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="575a5-117">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




