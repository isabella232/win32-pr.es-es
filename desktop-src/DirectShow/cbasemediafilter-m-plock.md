---
description: Puntero a una sección crítica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Miembro CBaseMediaFilter:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660937"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="43e5d-103">Miembro Plock CBaseMediaFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="43e5d-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="43e5d-104">Puntero a una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="43e5d-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e5d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43e5d-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="43e5d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43e5d-106">Remarks</span></span>

<span data-ttu-id="43e5d-107">La sección crítica se mantiene durante las transiciones de estado ([**CBaseMediaFilter:: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter:: Stop**](cbasemediafilter-stop.md)), al tener acceso al reloj de referencia ([**CBaseMediaFilter:: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) y en el método [**CBaseMediaFilter:: IsActive**](cbasemediafilter-isactive.md) .</span><span class="sxs-lookup"><span data-stu-id="43e5d-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e5d-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e5d-108">Requirements</span></span>



| <span data-ttu-id="43e5d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e5d-109">Requirement</span></span> | <span data-ttu-id="43e5d-110">Value</span><span class="sxs-lookup"><span data-stu-id="43e5d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e5d-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43e5d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="43e5d-112"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43e5d-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43e5d-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43e5d-113">Library</span></span><br/> | <dl> <span data-ttu-id="43e5d-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="43e5d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e5d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="43e5d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e5d-116">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="43e5d-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




