---
description: Procesa las solicitudes. Se trata de una función miembro virtual pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Método CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671221"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="2be59-104">CMsgThread. ThreadMessageProc, método</span><span class="sxs-lookup"><span data-stu-id="2be59-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="2be59-105">Procesa las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be59-105">Processes requests.</span></span> <span data-ttu-id="2be59-106">Se trata de una función miembro virtual pura.</span><span class="sxs-lookup"><span data-stu-id="2be59-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be59-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be59-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="2be59-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2be59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be59-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="2be59-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2be59-110">Código de solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be59-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="2be59-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2be59-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2be59-112">Parámetro opcional de la marca que se va a solicitar.</span><span class="sxs-lookup"><span data-stu-id="2be59-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="2be59-113">*lpParam*</span><span class="sxs-lookup"><span data-stu-id="2be59-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2be59-114">Puntero opcional a datos adicionales o un bloque de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="2be59-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="2be59-115">*As*</span><span class="sxs-lookup"><span data-stu-id="2be59-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="2be59-116">Puntero opcional a un objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="2be59-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be59-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2be59-117">Return value</span></span>

<span data-ttu-id="2be59-118">Cualquier devolución distinto de cero hace que el subproceso se cierre.</span><span class="sxs-lookup"><span data-stu-id="2be59-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="2be59-119">Devuelve cero a menos que se haya procesado recientemente una solicitud de salida.</span><span class="sxs-lookup"><span data-stu-id="2be59-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="2be59-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2be59-120">Remarks</span></span>

<span data-ttu-id="2be59-121">Esta función virtual pura se debe invalidar en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="2be59-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="2be59-122">Se llamará una vez para cada solicitud puesta en cola mediante una llamada a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="2be59-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="2be59-123">La función miembro define los cuatro parámetros.</span><span class="sxs-lookup"><span data-stu-id="2be59-123">The member function defines the four parameters.</span></span> <span data-ttu-id="2be59-124">Normalmente, use el parámetro *uMsg* para indicar la solicitud y los otros tres parámetros serán parámetros adicionales opcionales.</span><span class="sxs-lookup"><span data-stu-id="2be59-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="2be59-125">La aplicación que realiza la llamada puede proporcionar un puntero a un objeto [**CAMEvent**](camevent.md) en el parámetro *pevent* si la aplicación lo requiere.</span><span class="sxs-lookup"><span data-stu-id="2be59-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="2be59-126">Debe establecer este evento después de procesar el evento mediante una expresión como:</span><span class="sxs-lookup"><span data-stu-id="2be59-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="2be59-127">Se debe reservar un código de solicitud para indicar al subproceso de trabajo que se cierre.</span><span class="sxs-lookup"><span data-stu-id="2be59-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="2be59-128">Al recibir esta solicitud, devuelve 1 de esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="2be59-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="2be59-129">Devuelve 0 si no desea que el subproceso de trabajo salga.</span><span class="sxs-lookup"><span data-stu-id="2be59-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be59-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be59-130">Requirements</span></span>



| <span data-ttu-id="2be59-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be59-131">Requirement</span></span> | <span data-ttu-id="2be59-132">Value</span><span class="sxs-lookup"><span data-stu-id="2be59-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be59-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2be59-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2be59-134"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2be59-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2be59-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be59-135">Library</span></span><br/> | <dl> <span data-ttu-id="2be59-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2be59-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be59-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2be59-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be59-138">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="2be59-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




