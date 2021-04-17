---
description: El método CheckRequest comprueba si hay una solicitud, sin bloqueos.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Método CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690444"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="346cc-103">CAMThread. CheckRequest, método</span><span class="sxs-lookup"><span data-stu-id="346cc-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="346cc-104">El `CheckRequest` método comprueba si hay una solicitud, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="346cc-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="346cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="346cc-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="346cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="346cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346cc-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="346cc-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="346cc-108">Puntero a una variable que recibe el valor pasado en la última llamada al método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="346cc-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346cc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="346cc-109">Return value</span></span>

<span data-ttu-id="346cc-110">Devuelve **true** si hay una solicitud pendiente o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="346cc-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="346cc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="346cc-111">Remarks</span></span>

<span data-ttu-id="346cc-112">Este método es una versión que no es de bloqueo del método [**CAMThread:: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="346cc-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="346cc-113">Si otro subproceso está esperando en una llamada a CallWorker, este método recupera el parámetro de solicitud y devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="346cc-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="346cc-114">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="346cc-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="346cc-115">Si el método devuelve **true**, llame al método [**CAMThread:: reply**](camthread-reply.md) para liberar el subproceso que lo solicita.</span><span class="sxs-lookup"><span data-stu-id="346cc-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="346cc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="346cc-116">Requirements</span></span>



| <span data-ttu-id="346cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="346cc-117">Requirement</span></span> | <span data-ttu-id="346cc-118">Value</span><span class="sxs-lookup"><span data-stu-id="346cc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346cc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="346cc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="346cc-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="346cc-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="346cc-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="346cc-121">Library</span></span><br/> | <dl> <span data-ttu-id="346cc-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="346cc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346cc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="346cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346cc-124">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="346cc-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




