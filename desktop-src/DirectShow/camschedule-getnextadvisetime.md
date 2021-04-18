---
description: El método GetNextAdviseTime recupera la hora de la solicitud de notificación siguiente.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Método CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671112"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="7fde1-103">CAMSchedule. GetNextAdviseTime, método</span><span class="sxs-lookup"><span data-stu-id="7fde1-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="7fde1-104">El `GetNextAdviseTime` método recupera la hora de la solicitud de notificación siguiente.</span><span class="sxs-lookup"><span data-stu-id="7fde1-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fde1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fde1-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="7fde1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fde1-106">Parameters</span></span>

<span data-ttu-id="7fde1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7fde1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fde1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fde1-108">Return value</span></span>

<span data-ttu-id="7fde1-109">Devuelve la hora de referencia de la solicitud de notificación siguiente o el tiempo máximo que \_ no hay solicitudes programadas.</span><span class="sxs-lookup"><span data-stu-id="7fde1-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fde1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fde1-110">Requirements</span></span>



| <span data-ttu-id="7fde1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fde1-111">Requirement</span></span> | <span data-ttu-id="7fde1-112">Value</span><span class="sxs-lookup"><span data-stu-id="7fde1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fde1-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fde1-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7fde1-114"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fde1-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="7fde1-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fde1-115">Library</span></span><br/> | <dl> <span data-ttu-id="7fde1-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7fde1-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fde1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fde1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fde1-118">**Clase CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="7fde1-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




