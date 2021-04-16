---
description: El método GetRequest espera a la solicitud siguiente.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Método CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690576"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="3f5de-103">CAMThread. GetRequest, método</span><span class="sxs-lookup"><span data-stu-id="3f5de-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="3f5de-104">El `GetRequest` método espera a la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f5de-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f5de-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="3f5de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f5de-106">Parameters</span></span>

<span data-ttu-id="3f5de-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3f5de-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f5de-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f5de-108">Return value</span></span>

<span data-ttu-id="3f5de-109">Devuelve un valor definido por la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="3f5de-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f5de-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f5de-110">Remarks</span></span>

<span data-ttu-id="3f5de-111">Este método se bloquea hasta que otro subproceso llama al método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5de-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="3f5de-112">A continuación, devuelve el parámetro que se pasó a CallWorker.</span><span class="sxs-lookup"><span data-stu-id="3f5de-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="3f5de-113">Llame al método [**CAMThread:: reply**](camthread-reply.md) para liberar el subproceso que lo solicita.</span><span class="sxs-lookup"><span data-stu-id="3f5de-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f5de-114">Requirements</span></span>



| <span data-ttu-id="3f5de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5de-115">Requirement</span></span> | <span data-ttu-id="3f5de-116">Value</span><span class="sxs-lookup"><span data-stu-id="3f5de-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5de-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f5de-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3f5de-118"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3f5de-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f5de-119">Library</span></span><br/> | <dl> <span data-ttu-id="3f5de-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5de-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5de-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f5de-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5de-122">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="3f5de-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




