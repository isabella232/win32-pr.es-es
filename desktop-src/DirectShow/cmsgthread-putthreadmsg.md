---
description: Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Método CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671409"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="62514-103">CMsgThread. PutThreadMsg, método</span><span class="sxs-lookup"><span data-stu-id="62514-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="62514-104">Pone en cola una solicitud de ejecución por parte del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="62514-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="62514-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62514-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="62514-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62514-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62514-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="62514-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="62514-108">Código de solicitud.</span><span class="sxs-lookup"><span data-stu-id="62514-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="62514-109">*dwMsgFlags*</span><span class="sxs-lookup"><span data-stu-id="62514-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="62514-110">Parámetro opcional Flags.</span><span class="sxs-lookup"><span data-stu-id="62514-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62514-111">*lpMsgParam*</span><span class="sxs-lookup"><span data-stu-id="62514-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62514-112">Puntero opcional a un bloque de datos que contiene parámetros o valores devueltos adicionales.</span><span class="sxs-lookup"><span data-stu-id="62514-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="62514-113">Debe ser estático o asignado por montón y no automático.</span><span class="sxs-lookup"><span data-stu-id="62514-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="62514-114">*As*</span><span class="sxs-lookup"><span data-stu-id="62514-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="62514-115">Puntero opcional a un objeto de evento que se va a señalar al finalizar.</span><span class="sxs-lookup"><span data-stu-id="62514-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62514-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62514-116">Return value</span></span>

<span data-ttu-id="62514-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="62514-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62514-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62514-118">Remarks</span></span>

<span data-ttu-id="62514-119">Esta función miembro pone en cola una solicitud de ejecución por parte del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="62514-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="62514-120">Los parámetros de esta función miembro se pondrán en cola (en un objeto [**CMsg**](cmsg.md) ) y se pasarán a la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="62514-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="62514-121">Esta función miembro devuelve inmediatamente después de poner en cola la solicitud y no espera a que el subproceso complete la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62514-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="62514-122">La función miembro **CMsgThread:: ThreadMessageProc** de la clase derivada define los cuatro parámetros.</span><span class="sxs-lookup"><span data-stu-id="62514-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="62514-123">Esta función miembro usa una lista segura para subprocesos, por lo que se pueden realizar varias llamadas a esta función miembro desde distintos subprocesos de forma segura.</span><span class="sxs-lookup"><span data-stu-id="62514-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="62514-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62514-124">Requirements</span></span>



| <span data-ttu-id="62514-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62514-125">Requirement</span></span> | <span data-ttu-id="62514-126">Value</span><span class="sxs-lookup"><span data-stu-id="62514-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62514-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62514-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62514-128"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62514-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62514-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62514-129">Library</span></span><br/> | <dl> <span data-ttu-id="62514-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62514-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62514-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="62514-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62514-132">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="62514-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




