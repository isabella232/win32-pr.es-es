---
description: Recupera un objeto CMsg en cola que contiene una solicitud.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Método CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680346"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="9563b-103">CMsgThread. GetThreadMsg, método</span><span class="sxs-lookup"><span data-stu-id="9563b-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="9563b-104">Recupera un objeto [**CMsg**](cmsg.md) en cola que contiene una solicitud.</span><span class="sxs-lookup"><span data-stu-id="9563b-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9563b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9563b-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="9563b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9563b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9563b-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="9563b-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="9563b-108">Puntero a un objeto [**CMsg**](cmsg.md) asignado.</span><span class="sxs-lookup"><span data-stu-id="9563b-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9563b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9563b-109">Return value</span></span>

<span data-ttu-id="9563b-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9563b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9563b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9563b-111">Remarks</span></span>

<span data-ttu-id="9563b-112">Se llama a esta función miembro desde la función [**ThreadProc**](camthread-threadproc.md) Private del subproceso de trabajo para recuperar la función miembro siguiente.</span><span class="sxs-lookup"><span data-stu-id="9563b-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="9563b-113">El parámetro *MSG* debe apuntar a un objeto [**CMsg**](cmsg.md) asignado que se rellenará con los parámetros de la siguiente solicitud de la cola.</span><span class="sxs-lookup"><span data-stu-id="9563b-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="9563b-114">Si no hay ninguna solicitud en cola, esta función miembro se bloquea hasta que se pone en cola la siguiente solicitud (mediante una llamada a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).</span><span class="sxs-lookup"><span data-stu-id="9563b-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="9563b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9563b-115">Requirements</span></span>



| <span data-ttu-id="9563b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9563b-116">Requirement</span></span> | <span data-ttu-id="9563b-117">Value</span><span class="sxs-lookup"><span data-stu-id="9563b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9563b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9563b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9563b-119"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9563b-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9563b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9563b-120">Library</span></span><br/> | <dl> <span data-ttu-id="9563b-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9563b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9563b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9563b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9563b-123">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="9563b-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




