---
description: Puntero a un objeto de sección crítica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Miembro CSourceSeeking:: m_pLock (Ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690549"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="b262c-103">Miembro Plock CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="b262c-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="b262c-104">Puntero a un objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="b262c-104">Pointer to a critical section object.</span></span> <span data-ttu-id="b262c-105">La `CSourceSeeking` clase utiliza esta sección crítica para sincronizar el acceso a las horas de inicio y detención, la duración y las variables de velocidad.</span><span class="sxs-lookup"><span data-stu-id="b262c-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="b262c-106">Esta variable se inicializa en el método de constructor; vea [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="b262c-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b262c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b262c-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="b262c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b262c-108">Requirements</span></span>



| <span data-ttu-id="b262c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="b262c-109">Requirement</span></span> | <span data-ttu-id="b262c-110">Value</span><span class="sxs-lookup"><span data-stu-id="b262c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b262c-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b262c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b262c-112"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b262c-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b262c-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b262c-113">Library</span></span><br/> | <dl> <span data-ttu-id="b262c-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b262c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b262c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b262c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b262c-116">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b262c-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




