---
description: El método AddAdvisePacket agrega una solicitud de notificación a la lista de solicitudes pendientes.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Método CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671117"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="9151f-103">CAMSchedule. AddAdvisePacket, método</span><span class="sxs-lookup"><span data-stu-id="9151f-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="9151f-104">El `AddAdvisePacket` método agrega una solicitud de notificación a la lista de solicitudes pendientes.</span><span class="sxs-lookup"><span data-stu-id="9151f-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="9151f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9151f-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="9151f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9151f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9151f-107">*tiempo1* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="9151f-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9151f-108">Hora solicitada para el aviso.</span><span class="sxs-lookup"><span data-stu-id="9151f-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="9151f-109">*al tiempo2?* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="9151f-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9151f-110">Para solicitudes de notificación periódicas, el tiempo entre notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9151f-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="9151f-111">Este parámetro se omite si *bPeriodic* es **false**.</span><span class="sxs-lookup"><span data-stu-id="9151f-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9151f-112">*hNotify*</span><span class="sxs-lookup"><span data-stu-id="9151f-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="9151f-113">Identificador de un semáforo si *bPeriodic* es **true** o identificador de un evento si *bPeriodic* es **false**.</span><span class="sxs-lookup"><span data-stu-id="9151f-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9151f-114">*bPeriodic*</span><span class="sxs-lookup"><span data-stu-id="9151f-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="9151f-115">Valor booleano que especifica si se debe agregar una notificación periódica o una notificación de una captura.</span><span class="sxs-lookup"><span data-stu-id="9151f-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="9151f-116">Si es **true**, la notificación es periódica; el parámetro *al tiempo2?* especifica el tiempo entre notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9151f-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="9151f-117">Si **es false**, la notificación se produce una sola vez.</span><span class="sxs-lookup"><span data-stu-id="9151f-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9151f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9151f-118">Return value</span></span>

<span data-ttu-id="9151f-119">Devuelve un identificador para la solicitud de notificación (la "cookie").</span><span class="sxs-lookup"><span data-stu-id="9151f-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="9151f-120">Si se produce un error en el método, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9151f-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9151f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9151f-121">Requirements</span></span>



| <span data-ttu-id="9151f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9151f-122">Requirement</span></span> | <span data-ttu-id="9151f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9151f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9151f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9151f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9151f-125"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9151f-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="9151f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9151f-126">Library</span></span><br/> | <dl> <span data-ttu-id="9151f-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9151f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9151f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9151f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9151f-129">**Clase CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="9151f-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




