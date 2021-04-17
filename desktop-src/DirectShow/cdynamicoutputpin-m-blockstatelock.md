---
description: Sección crítica que protege el estado de bloqueo.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Miembro CDynamicOutputPin:: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660564"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="8fcf9-103">Miembro BlockStateLock CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="8fcf9-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="8fcf9-104">Sección crítica que protege el estado de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcf9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fcf9-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="8fcf9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fcf9-106">Remarks</span></span>

<span data-ttu-id="8fcf9-107">Mantenga esta sección crítica antes de usar cualquiera de las siguientes variables miembro:</span><span class="sxs-lookup"><span data-stu-id="8fcf9-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="8fcf9-108">**CDynamicOutputPin:: m \_ BlockState**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="8fcf9-109">**CDynamicOutputPin:: m \_ dwBlockCallerThreadID**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="8fcf9-110">**CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="8fcf9-111">**CDynamicOutputPin:: m \_ hNotifyCallerPinBlockedEvent**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="8fcf9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fcf9-112">Requirements</span></span>



| <span data-ttu-id="8fcf9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcf9-113">Requirement</span></span> | <span data-ttu-id="8fcf9-114">Value</span><span class="sxs-lookup"><span data-stu-id="8fcf9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf9-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fcf9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8fcf9-116"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf9-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8fcf9-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fcf9-117">Library</span></span><br/> | <dl> <span data-ttu-id="8fcf9-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcf9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fcf9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf9-120">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




