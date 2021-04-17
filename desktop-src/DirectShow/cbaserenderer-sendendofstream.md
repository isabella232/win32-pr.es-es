---
description: Si se ha alcanzado el final de la secuencia, el método SendEndOfStream programa un \_ evento EC complete para el administrador de gráficos de filtro.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Método CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670667"
---
# <a name="cbaserenderersendendofstream-method"></a><span data-ttu-id="f9b19-103">CBaseRenderer. SendEndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="f9b19-103">CBaseRenderer.SendEndOfStream method</span></span>

<span data-ttu-id="f9b19-104">Si se ha alcanzado el final de la secuencia, el `SendEndOfStream` método programa un \_ evento EC complete para el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="f9b19-104">If end-of-stream was reached, the `SendEndOfStream` method schedules an EC\_COMPLETE event for the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9b19-105">Syntax</span></span>


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="f9b19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9b19-106">Parameters</span></span>

<span data-ttu-id="f9b19-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9b19-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9b19-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9b19-108">Return value</span></span>

<span data-ttu-id="f9b19-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9b19-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f9b19-110">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9b19-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="f9b19-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f9b19-111">Return code</span></span>                                                                             | <span data-ttu-id="f9b19-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9b19-112">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9b19-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f9b19-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f9b19-114">El administrador de gráficos de filtro no acepta notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9b19-114">The filter graph manager is not accepting event notifications.</span></span><br/> |
| <dl> <span data-ttu-id="f9b19-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f9b19-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f9b19-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f9b19-116">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f9b19-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9b19-117">Remarks</span></span>

<span data-ttu-id="f9b19-118">El filtro podría recibir una notificación de final de secuencia antes de la hora de detención del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="f9b19-118">The filter might receive an end-of-stream notification before the current sample's stop time.</span></span> <span data-ttu-id="f9b19-119">Si es así, el filtro debe esperar antes de publicar una notificación de [**\_ finalización de EC**](ec-complete.md) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="f9b19-119">If so, the filter should wait before posting an [**EC\_COMPLETE**](ec-complete.md) notification to the filter graph manager.</span></span>

<span data-ttu-id="f9b19-120">Por lo tanto:</span><span class="sxs-lookup"><span data-stu-id="f9b19-120">Therefore:</span></span>

-   <span data-ttu-id="f9b19-121">Si el filtro ha recibido una notificación de final de secuencia (EOS) temprana, este método programa un evento de temporizador.</span><span class="sxs-lookup"><span data-stu-id="f9b19-121">If the filter has received an early end-of-stream (EOS) notification, this method schedules a timer event.</span></span> <span data-ttu-id="f9b19-122">Cuando se activa el evento de temporizador, el filtro envía el \_ evento de finalización de EC.</span><span class="sxs-lookup"><span data-stu-id="f9b19-122">When the timer event is activated, the filter posts the EC\_COMPLETE event.</span></span>
-   <span data-ttu-id="f9b19-123">Si el filtro ha recibido una notificación de EOS que no era temprano, este método publica el \_ evento de finalización de EC inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9b19-123">If the filter has received an EOS notification that was not early, this method posts the EC\_COMPLETE event immediately.</span></span>
-   <span data-ttu-id="f9b19-124">Si el filtro no tiene ninguna notificación de EOS pendiente, el método devuelve sin hacer nada.</span><span class="sxs-lookup"><span data-stu-id="f9b19-124">If the filter does not have any pending EOS notification, the method returns without doing anything.</span></span>

<span data-ttu-id="f9b19-125">El método de devolución de llamada del temporizador es [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md).</span><span class="sxs-lookup"><span data-stu-id="f9b19-125">The timer callback method is [**CBaseRenderer::TimerCallback**](cbaserenderer-timercallback.md).</span></span> <span data-ttu-id="f9b19-126">Para enviar el \_ evento de finalización de EC, el filtro llama al método [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b19-126">To deliver the EC\_COMPLETE event, the filter calls the [**CBaseRenderer::NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b19-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b19-127">Requirements</span></span>



| <span data-ttu-id="f9b19-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b19-128">Requirement</span></span> | <span data-ttu-id="f9b19-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9b19-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b19-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9b19-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b19-131"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b19-131"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9b19-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9b19-132">Library</span></span><br/> | <dl> <span data-ttu-id="f9b19-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b19-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b19-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9b19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b19-135">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f9b19-135">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




