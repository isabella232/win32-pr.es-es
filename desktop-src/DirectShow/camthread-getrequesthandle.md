---
description: 'El método GetRequestHandle recupera un identificador para el evento señalado por el método CAMThread:: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Método CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690732"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="eed18-103">CAMThread. GetRequestHandle, método</span><span class="sxs-lookup"><span data-stu-id="eed18-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="eed18-104">El `GetRequestHandle` método recupera un identificador para el evento señalado por el método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="eed18-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eed18-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="eed18-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eed18-106">Parameters</span></span>

<span data-ttu-id="eed18-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="eed18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eed18-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eed18-108">Return value</span></span>

<span data-ttu-id="eed18-109">Devuelve un identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="eed18-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed18-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eed18-110">Remarks</span></span>

<span data-ttu-id="eed18-111">La clase CAMEvent mantiene un evento privado de restablecimiento manual, establecido por CallWorker y restablecido por el método [**CAMThread:: reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="eed18-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="eed18-112">Si llama a una función como WaitForMultipleObjects, use GetRequestHandle para recuperar el identificador de eventos.</span><span class="sxs-lookup"><span data-stu-id="eed18-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed18-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed18-113">Requirements</span></span>



| <span data-ttu-id="eed18-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed18-114">Requirement</span></span> | <span data-ttu-id="eed18-115">Value</span><span class="sxs-lookup"><span data-stu-id="eed18-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed18-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eed18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eed18-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eed18-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eed18-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eed18-118">Library</span></span><br/> | <dl> <span data-ttu-id="eed18-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eed18-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed18-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="eed18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed18-121">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="eed18-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




