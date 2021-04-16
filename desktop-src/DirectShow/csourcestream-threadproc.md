---
description: 'El método ThreadProc es el procedimiento de subproceso para el subproceso de trabajo. Este método implementa el método CAMThread:: ThreadProc virtual puro.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream. ThreadProc (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679169"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="98214-104">CSourceStream. ThreadProc (método)</span><span class="sxs-lookup"><span data-stu-id="98214-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="98214-105">El `ThreadProc` método es el procedimiento de subproceso para el subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="98214-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="98214-106">Este método implementa el método [**CAMThread:: ThreadProc**](camthread-threadproc.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="98214-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98214-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98214-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="98214-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98214-108">Parameters</span></span>

<span data-ttu-id="98214-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="98214-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98214-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98214-110">Return value</span></span>

<span data-ttu-id="98214-111">Devuelve 0 si el subproceso se completó correctamente o 1 de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="98214-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="98214-112">Si el valor devuelto es 1, es posible que los recursos del subproceso sigan asignados.</span><span class="sxs-lookup"><span data-stu-id="98214-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="98214-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98214-113">Remarks</span></span>

<span data-ttu-id="98214-114">Este método espera indefinidamente a las solicitudes de subprocesos llamando al método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="98214-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="98214-115">Si recibe una solicitud [**CSourceStream:: Run**](csourcestream-run.md) o [**CSourceStream::P ause**](csourcestream-pause.md) , llama al método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="98214-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="98214-116">El método **DoBufferProcessingLoop** envía datos hasta que recibe una solicitud [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="98214-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="98214-117">El procedimiento de subproceso se cierra cuando recibe una solicitud [**CSourceStream:: Exit**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="98214-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="98214-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98214-118">Requirements</span></span>



| <span data-ttu-id="98214-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98214-119">Requirement</span></span> | <span data-ttu-id="98214-120">Value</span><span class="sxs-lookup"><span data-stu-id="98214-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98214-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98214-121">Header</span></span><br/>  | <dl> <span data-ttu-id="98214-122"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98214-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="98214-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98214-123">Library</span></span><br/> | <dl> <span data-ttu-id="98214-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98214-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98214-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98214-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98214-126">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="98214-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




