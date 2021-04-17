---
description: El método GetEvent recupera un identificador de evento, que se usa para indicar un cambio en la hora del siguiente aviso.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Método CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660631"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="e860f-103">CAMSchedule. GetEvent, método</span><span class="sxs-lookup"><span data-stu-id="e860f-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="e860f-104">El `GetEvent` método recupera un identificador de evento, que se usa para indicar un cambio en la hora del siguiente aviso.</span><span class="sxs-lookup"><span data-stu-id="e860f-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e860f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e860f-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="e860f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e860f-106">Parameters</span></span>

<span data-ttu-id="e860f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e860f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e860f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e860f-108">Return value</span></span>

<span data-ttu-id="e860f-109">Devuelve un identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="e860f-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="e860f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e860f-110">Remarks</span></span>

<span data-ttu-id="e860f-111">Si la hora del siguiente aviso cambia en otras palabras, si se agrega una nueva solicitud de notificación al principio de la lista, el programador indica este evento.</span><span class="sxs-lookup"><span data-stu-id="e860f-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="e860f-112">El reloj debe llamar al método [**CAMSchedule:: Advise**](camschedule-advise.md) para determinar la hora del siguiente aviso.</span><span class="sxs-lookup"><span data-stu-id="e860f-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="e860f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e860f-113">Requirements</span></span>



| <span data-ttu-id="e860f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e860f-114">Requirement</span></span> | <span data-ttu-id="e860f-115">Value</span><span class="sxs-lookup"><span data-stu-id="e860f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e860f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e860f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e860f-117"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e860f-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="e860f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e860f-118">Library</span></span><br/> | <dl> <span data-ttu-id="e860f-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e860f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e860f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e860f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e860f-121">**Clase CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="e860f-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




