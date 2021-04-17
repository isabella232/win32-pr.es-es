---
description: El método StartUsingOutputPin obtiene acceso al pin para una operación de streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Método CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661201"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="0ad9b-103">CDynamicOutputPin. StartUsingOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="0ad9b-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="0ad9b-104">El `StartUsingOutputPin` método obtiene acceso al pin para una operación de streaming.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ad9b-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="0ad9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ad9b-106">Parameters</span></span>

<span data-ttu-id="0ad9b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ad9b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ad9b-108">Return value</span></span>

<span data-ttu-id="0ad9b-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ad9b-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0ad9b-110">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0ad9b-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0ad9b-111">Return code</span></span>                                                                                           | <span data-ttu-id="0ad9b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ad9b-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ad9b-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9b-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="0ad9b-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0ad9b-115"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9b-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="0ad9b-116">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ad9b-117"><dt>**Estado de VFW \_ E \_ \_ cambiado**</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9b-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="0ad9b-118">Se detuvo el filtro o el PIN comenzó a vaciarse.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ad9b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ad9b-119">Remarks</span></span>

<span data-ttu-id="0ad9b-120">Llame a este método antes de llamar a cualquier método que entregue datos a la clavija de entrada conectada o que cambie el tipo de medio de la conexión.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="0ad9b-121">Por ejemplo, esta regla se aplica a los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="0ad9b-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="0ad9b-122">**CDynamicOutputPin::ChangeOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="0ad9b-123">**CDynamicOutputPin::ChangeMediaType**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="0ad9b-124">**CDynamicOutputPin::D ynamicReconnect**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="0ad9b-125">**CBaseOutputPin::D Eliver**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="0ad9b-126">**CBaseOutputPin::D eliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="0ad9b-127">**CBaseOutputPin::D eliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="0ad9b-128">**IMemInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="0ad9b-129">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="0ad9b-130">**IPin:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="0ad9b-131">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="0ad9b-132">Después, llame al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) para liberar el acceso al código PIN.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="0ad9b-133">Si el PIN está bloqueado, `StartUsingOutputPin` espera a que el PIN se desbloquee.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="0ad9b-134">Si el filtro se detiene mientras el método está esperando, el método devuelve inmediatamente \_ el \_ Estado VFW E \_ cambiado.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="0ad9b-135">El PIN mantiene un recuento del número de veces que se ha `StartUsingOutputPin` llamado sin una llamada correspondiente a **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="0ad9b-136">Si otro subproceso intenta bloquear el PIN mientras este recuento es distinto de cero, el PIN establece su estado de bloqueo en "pendiente".</span><span class="sxs-lookup"><span data-stu-id="0ad9b-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="0ad9b-137">El PIN se bloquea una vez completadas todas las operaciones de streaming, en la llamada final a **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="0ad9b-138">No conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) cuando llame a este método.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="0ad9b-139">De lo contrario, si el PIN está bloqueado, nunca se puede desbloquear, lo que produce un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="0ad9b-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad9b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad9b-140">Requirements</span></span>



| <span data-ttu-id="0ad9b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad9b-141">Requirement</span></span> | <span data-ttu-id="0ad9b-142">Value</span><span class="sxs-lookup"><span data-stu-id="0ad9b-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad9b-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ad9b-143">Header</span></span><br/>  | <dl> <span data-ttu-id="0ad9b-144"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9b-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ad9b-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ad9b-145">Library</span></span><br/> | <dl> <span data-ttu-id="0ad9b-146"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9b-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ad9b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ad9b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad9b-148">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0ad9b-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




