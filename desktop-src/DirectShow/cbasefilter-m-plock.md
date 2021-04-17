---
description: Puntero a una sección crítica que se usa para serializar los cambios de estado.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Miembro CBaseFilter:: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660461"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="36f58-103">Miembro Plock CBaseFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="36f58-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="36f58-104">Puntero a una sección crítica que se usa para serializar los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="36f58-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f58-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36f58-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="36f58-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36f58-106">Remarks</span></span>

<span data-ttu-id="36f58-107">Esta variable se inicializa en el constructor de clase; vea [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="36f58-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="36f58-108">Mantenga esta sección crítica durante las transiciones de estado o cuando un método tiene acceso al estado en varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="36f58-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="36f58-109">La clase base contiene la sección crítica en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="36f58-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="36f58-110">**CBaseFilter::FindPin**</span><span class="sxs-lookup"><span data-stu-id="36f58-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="36f58-111">**CBaseFilter::GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="36f58-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="36f58-112">**CBaseFilter::JoinFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="36f58-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="36f58-113">**CBaseFilter:: IsActive**</span><span class="sxs-lookup"><span data-stu-id="36f58-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="36f58-114">**CBaseFilter::SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="36f58-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="36f58-115">**CBaseFilter::P ause**</span><span class="sxs-lookup"><span data-stu-id="36f58-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="36f58-116">**CBaseFilter:: Run**</span><span class="sxs-lookup"><span data-stu-id="36f58-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="36f58-117">**CBaseFilter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="36f58-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="36f58-118">No conserve esta sección crítica durante las operaciones de streaming (es decir, al entregar muestras a un filtro de nivel inferior).</span><span class="sxs-lookup"><span data-stu-id="36f58-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="36f58-119">Serialice las operaciones de streaming con una sección crítica diferente.</span><span class="sxs-lookup"><span data-stu-id="36f58-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="36f58-120">De lo contrario, puede producir un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="36f58-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f58-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f58-121">Requirements</span></span>



| <span data-ttu-id="36f58-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f58-122">Requirement</span></span> | <span data-ttu-id="36f58-123">Value</span><span class="sxs-lookup"><span data-stu-id="36f58-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f58-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36f58-124">Header</span></span><br/>  | <dl> <span data-ttu-id="36f58-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36f58-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="36f58-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36f58-126">Library</span></span><br/> | <dl> <span data-ttu-id="36f58-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="36f58-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f58-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="36f58-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f58-129">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="36f58-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="36f58-130">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="36f58-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




