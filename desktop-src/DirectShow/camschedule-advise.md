---
description: El método Advise envía todas las solicitudes que están programadas para una hora especificada o anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule. Advise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671116"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="e4ec8-103">CAMSchedule. Advise (método)</span><span class="sxs-lookup"><span data-stu-id="e4ec8-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="e4ec8-104">El `Advise` método envía todas las solicitudes que están programadas para una hora especificada o anterior.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ec8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4ec8-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="e4ec8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4ec8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ec8-107">*rtTime* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="e4ec8-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ec8-108">Valor que especifica el tiempo de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ec8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4ec8-109">Return value</span></span>

<span data-ttu-id="e4ec8-110">Devuelve la hora de referencia de la siguiente solicitud de notificación programada o el \_ tiempo máximo si no hay ninguna.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ec8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4ec8-111">Remarks</span></span>

<span data-ttu-id="e4ec8-112">Cuando el reloj llama a este método, especifica el tiempo de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="e4ec8-113">Scheduler determina qué solicitudes de notificaciones han expirado, si hay alguna, y las envía.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="e4ec8-114">Si expira una solicitud de una captura, el programador la elimina.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="e4ec8-115">Si una solicitud periódica expira, Scheduler la vuelve a programar para el siguiente tiempo de notificación.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="e4ec8-116">El método devuelve la hora de la siguiente solicitud pendiente.</span><span class="sxs-lookup"><span data-stu-id="e4ec8-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="e4ec8-117">Para enviar una solicitud de notificación, el programador indica el evento o semáforo proporcionado en el parámetro *hNotify* del método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="e4ec8-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ec8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ec8-118">Requirements</span></span>



| <span data-ttu-id="e4ec8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ec8-119">Requirement</span></span> | <span data-ttu-id="e4ec8-120">Value</span><span class="sxs-lookup"><span data-stu-id="e4ec8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ec8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4ec8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ec8-122"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ec8-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="e4ec8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4ec8-123">Library</span></span><br/> | <dl> <span data-ttu-id="e4ec8-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ec8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ec8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4ec8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ec8-126">**Clase CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="e4ec8-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




