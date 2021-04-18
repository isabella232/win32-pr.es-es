---
description: El método CallWorker señala el subproceso con una solicitud.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Método CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690780"
---
# <a name="camthreadcallworker-method"></a><span data-ttu-id="ed033-103">CAMThread. CallWorker, método</span><span class="sxs-lookup"><span data-stu-id="ed033-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="ed033-104">El `CallWorker` método señala el subproceso con una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed033-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed033-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed033-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="ed033-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed033-107">*dwParam*</span><span class="sxs-lookup"><span data-stu-id="ed033-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed033-108">Parámetro de solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed033-108">Request parameter.</span></span> <span data-ttu-id="ed033-109">La clase derivada define el significado del parámetro.</span><span class="sxs-lookup"><span data-stu-id="ed033-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed033-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed033-110">Return value</span></span>

<span data-ttu-id="ed033-111">Devuelve un valor definido por la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="ed033-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed033-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed033-112">Remarks</span></span>

<span data-ttu-id="ed033-113">Los métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) y [**CAMThread:: CheckRequest**](camthread-checkrequest.md) recuperan el valor del parámetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="ed033-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="ed033-114">El método GetRequest se bloquea hasta que `CallWorker` se llama a.</span><span class="sxs-lookup"><span data-stu-id="ed033-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="ed033-115">Este método se bloquea hasta que se llama al método [**CAMThread:: reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="ed033-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="ed033-116">El valor devuelto es el parámetro dado a reply.</span><span class="sxs-lookup"><span data-stu-id="ed033-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="ed033-117">Este método contiene el bloqueo [**CAMThread:: m \_ AccessLock**](camthread-m-accesslock.md) para serializar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="ed033-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="ed033-118">Por consiguiente, llame a este método desde el propio subproceso o desde cualquier función miembro que se ejecute en el contexto del subproceso.</span><span class="sxs-lookup"><span data-stu-id="ed033-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed033-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed033-119">Requirements</span></span>



| <span data-ttu-id="ed033-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed033-120">Requirement</span></span> | <span data-ttu-id="ed033-121">Value</span><span class="sxs-lookup"><span data-stu-id="ed033-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed033-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed033-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ed033-123"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed033-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ed033-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed033-124">Library</span></span><br/> | <dl> <span data-ttu-id="ed033-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ed033-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed033-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed033-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed033-127">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="ed033-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




