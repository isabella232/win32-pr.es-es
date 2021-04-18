---
description: Puntero a un objeto de sección crítica que protege el estado del filtro.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Miembro CBasePin:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671442"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="dc295-103">Miembro Plock CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="dc295-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="dc295-104">Puntero a un objeto de sección crítica que protege el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="dc295-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc295-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc295-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="dc295-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc295-106">Requirements</span></span>



| <span data-ttu-id="dc295-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc295-107">Requirement</span></span> | <span data-ttu-id="dc295-108">Value</span><span class="sxs-lookup"><span data-stu-id="dc295-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc295-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc295-109">Header</span></span><br/>  | <dl> <span data-ttu-id="dc295-110"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc295-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dc295-111">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc295-111">Library</span></span><br/> | <dl> <span data-ttu-id="dc295-112"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dc295-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc295-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc295-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc295-114">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="dc295-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="dc295-115">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="dc295-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




