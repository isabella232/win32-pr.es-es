---
description: Número de bloqueos pendientes en este objeto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Miembro CCritSec:: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671165"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="71625-103">Miembro lockCount CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="71625-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="71625-104">Número de bloqueos pendientes en este objeto.</span><span class="sxs-lookup"><span data-stu-id="71625-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="71625-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71625-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="71625-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71625-106">Remarks</span></span>

<span data-ttu-id="71625-107">Esta variable miembro solo se define en la versión de depuración de la clase base.</span><span class="sxs-lookup"><span data-stu-id="71625-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="71625-108">En la sección crítica, las funciones de [depuración](critical-section-debugging-functions.md) de funciones utilizan este miembro.</span><span class="sxs-lookup"><span data-stu-id="71625-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="71625-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71625-109">Requirements</span></span>



| <span data-ttu-id="71625-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="71625-110">Requirement</span></span> | <span data-ttu-id="71625-111">Value</span><span class="sxs-lookup"><span data-stu-id="71625-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71625-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71625-112">Header</span></span><br/>  | <dl> <span data-ttu-id="71625-113"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71625-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="71625-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71625-114">Library</span></span><br/> | <dl> <span data-ttu-id="71625-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="71625-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71625-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="71625-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71625-117">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="71625-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




