---
description: El método NotifyEvent envía una notificación de eventos al administrador de gráficos de filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Método CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661170"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="36fc2-103">CBaseFilter. NotifyEvent, método</span><span class="sxs-lookup"><span data-stu-id="36fc2-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="36fc2-104">El `NotifyEvent` método envía una notificación de eventos al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="36fc2-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="36fc2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36fc2-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="36fc2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36fc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36fc2-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="36fc2-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="36fc2-108">Código de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="36fc2-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="36fc2-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="36fc2-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="36fc2-110">Primer parámetro del evento.</span><span class="sxs-lookup"><span data-stu-id="36fc2-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="36fc2-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="36fc2-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="36fc2-112">Segundo parámetro del evento.</span><span class="sxs-lookup"><span data-stu-id="36fc2-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36fc2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36fc2-113">Return value</span></span>

<span data-ttu-id="36fc2-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36fc2-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="36fc2-115">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="36fc2-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="36fc2-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="36fc2-116">Return code</span></span>                                                                               | <span data-ttu-id="36fc2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="36fc2-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36fc2-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="36fc2-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="36fc2-119">El administrador de gráficos de filtro no acepta notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="36fc2-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="36fc2-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="36fc2-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="36fc2-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="36fc2-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="36fc2-122"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="36fc2-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="36fc2-123">Filter no tiene un puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="36fc2-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36fc2-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36fc2-124">Remarks</span></span>

<span data-ttu-id="36fc2-125">Para obtener una lista de códigos de notificación y valores de parámetros, vea [códigos de notificación de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="36fc2-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="36fc2-126">En la clase base, si el código de evento es EC \_ completo, el método establece el parámetro *EventParam2* en un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro.</span><span class="sxs-lookup"><span data-stu-id="36fc2-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fc2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36fc2-127">Requirements</span></span>



| <span data-ttu-id="36fc2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="36fc2-128">Requirement</span></span> | <span data-ttu-id="36fc2-129">Value</span><span class="sxs-lookup"><span data-stu-id="36fc2-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36fc2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36fc2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="36fc2-131"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36fc2-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="36fc2-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36fc2-132">Library</span></span><br/> | <dl> <span data-ttu-id="36fc2-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="36fc2-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36fc2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="36fc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fc2-135">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="36fc2-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




