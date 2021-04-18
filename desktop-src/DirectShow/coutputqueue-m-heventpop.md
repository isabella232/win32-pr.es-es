---
description: 'Evento opcional que se señala cada vez que el objeto quita un ejemplo de la cola. El valor es inicialmente NULL. Llame al método COutputQueue:: SetPopEvent para especificar un identificador de evento.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Miembro COutputQueue:: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679464"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="a0bf0-105">Miembro hEventPop COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="a0bf0-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="a0bf0-106">Evento opcional que se señala cada vez que el objeto quita un ejemplo de la cola.</span><span class="sxs-lookup"><span data-stu-id="a0bf0-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="a0bf0-107">El valor es inicialmente **null**.</span><span class="sxs-lookup"><span data-stu-id="a0bf0-107">The value is initially **NULL**.</span></span> <span data-ttu-id="a0bf0-108">Llame al método [**COutputQueue:: SetPopEvent**](coutputqueue-setpopevent.md) para especificar un identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a0bf0-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bf0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0bf0-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="a0bf0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0bf0-110">Requirements</span></span>



| <span data-ttu-id="a0bf0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bf0-111">Requirement</span></span> | <span data-ttu-id="a0bf0-112">Value</span><span class="sxs-lookup"><span data-stu-id="a0bf0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bf0-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0bf0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a0bf0-114"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bf0-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0bf0-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0bf0-115">Library</span></span><br/> | <dl> <span data-ttu-id="a0bf0-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bf0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bf0-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0bf0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bf0-118">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="a0bf0-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




