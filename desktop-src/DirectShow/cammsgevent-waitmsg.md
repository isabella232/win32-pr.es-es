---
description: El método WaitMsg espera a que se señale el evento y envía los mensajes enviados.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Método CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660438"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="60489-103">CAMMsgEvent. WaitMsg, método</span><span class="sxs-lookup"><span data-stu-id="60489-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="60489-104">El `WaitMsg` método espera a que se señale el evento y envía los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="60489-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="60489-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60489-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="60489-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60489-107">*dwTimeOut*</span><span class="sxs-lookup"><span data-stu-id="60489-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="60489-108">Valor opcional de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="60489-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60489-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60489-109">Return value</span></span>

<span data-ttu-id="60489-110">Devuelve **true** si el evento está señalado, o **false** si se ha producido el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="60489-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="60489-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60489-111">Remarks</span></span>

<span data-ttu-id="60489-112">Este método llama a la función PeekMessage para procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="60489-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="60489-113">Llame a este método en lugar de [**CAMEvent:: wait**](camevent-wait.md) si el subproceso necesita procesar mensajes mientras espera un evento.</span><span class="sxs-lookup"><span data-stu-id="60489-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="60489-114">Si el subproceso no procesa los mensajes y otro subproceso envía un mensaje, podría producirse un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="60489-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="60489-115">Por ejemplo, suponga que crea un subproceso y, a continuación, se bloquea hasta que se inicializa el subproceso.</span><span class="sxs-lookup"><span data-stu-id="60489-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="60489-116">Si el subproceso envía un mensaje a la ventana mediante una llamada a la función SendMessage, se producirá un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="60489-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="60489-117">Esto se debe a que SendMessage no devuelve ningún resultado hasta que se haya procesado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="60489-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="60489-118">La llamada a WaitMsg permite que la llamada SendMessage devuelva, lo que impide el interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="60489-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="60489-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60489-119">Requirements</span></span>



| <span data-ttu-id="60489-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="60489-120">Requirement</span></span> | <span data-ttu-id="60489-121">Value</span><span class="sxs-lookup"><span data-stu-id="60489-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60489-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60489-122">Header</span></span><br/>  | <dl> <span data-ttu-id="60489-123"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60489-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60489-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60489-124">Library</span></span><br/> | <dl> <span data-ttu-id="60489-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="60489-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60489-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="60489-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60489-127">**Clase CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="60489-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




