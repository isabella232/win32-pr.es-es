---
description: El método AsynchronousBlockOutputPin bloquea el código PIN. El método puede devolver antes de que se bloquee el PIN.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Método CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661362"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="2ac3b-104">CDynamicOutputPin. AsynchronousBlockOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="2ac3b-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="2ac3b-105">El `AsynchronousBlockOutputPin` método bloquea el código PIN.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="2ac3b-106">El método puede devolver antes de que se bloquee el PIN.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac3b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ac3b-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="2ac3b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ac3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac3b-109">*hNotifyCallerPinBlockedEvent*</span><span class="sxs-lookup"><span data-stu-id="2ac3b-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac3b-110">Identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-110">Handle to an event.</span></span> <span data-ttu-id="2ac3b-111">El evento se señala cuando el PIN de salida está bloqueado o si el autor de la llamada cancela la operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac3b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ac3b-112">Return value</span></span>

<span data-ttu-id="2ac3b-113">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ac3b-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2ac3b-114">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2ac3b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2ac3b-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="2ac3b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ac3b-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2ac3b-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac3b-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="2ac3b-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2ac3b-119"><dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac3b-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="2ac3b-120">El PIN ya está bloqueado en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="2ac3b-121"><dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac3b-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="2ac3b-122">El PIN ya está bloqueado en el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ac3b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac3b-123">Remarks</span></span>

<span data-ttu-id="2ac3b-124">No llame a este método desde el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="2ac3b-125">Si no hay ningún subproceso de transmisión por secuencias que esté usando el PIN, este método bloqueará inmediatamente el código PIN.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="2ac3b-126">De lo contrario, establece el estado del PIN en "pendiente" y devuelve.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="2ac3b-127">Cuando se completa la operación de streaming, el subproceso de streaming llama al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , que bloquea el PIN e indica el evento **hNotifyCallerPinBlockedEvent** .</span><span class="sxs-lookup"><span data-stu-id="2ac3b-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="2ac3b-128">Para cancelar un bloque pendiente, llame al método [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="2ac3b-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac3b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ac3b-129">Requirements</span></span>



| <span data-ttu-id="2ac3b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac3b-130">Requirement</span></span> | <span data-ttu-id="2ac3b-131">Value</span><span class="sxs-lookup"><span data-stu-id="2ac3b-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac3b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ac3b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2ac3b-133"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac3b-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ac3b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ac3b-134">Library</span></span><br/> | <dl> <span data-ttu-id="2ac3b-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac3b-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac3b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ac3b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac3b-137">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="2ac3b-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




