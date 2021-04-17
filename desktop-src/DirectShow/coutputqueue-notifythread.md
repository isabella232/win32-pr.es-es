---
description: El método NotifyThread notifica al subproceso que la cola contiene datos.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Método COutputQueue. NotifyThread (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670410"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="2340c-103">COutputQueue. NotifyThread, método</span><span class="sxs-lookup"><span data-stu-id="2340c-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="2340c-104">El `NotifyThread` método notifica al subproceso que la cola contiene datos.</span><span class="sxs-lookup"><span data-stu-id="2340c-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2340c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2340c-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="2340c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2340c-106">Parameters</span></span>

<span data-ttu-id="2340c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2340c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2340c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2340c-108">Return value</span></span>

<span data-ttu-id="2340c-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2340c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2340c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2340c-110">Remarks</span></span>

<span data-ttu-id="2340c-111">Mantenga la sección crítica antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="2340c-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2340c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2340c-112">Requirements</span></span>



| <span data-ttu-id="2340c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2340c-113">Requirement</span></span> | <span data-ttu-id="2340c-114">Value</span><span class="sxs-lookup"><span data-stu-id="2340c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2340c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2340c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2340c-116"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2340c-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2340c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2340c-117">Library</span></span><br/> | <dl> <span data-ttu-id="2340c-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2340c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2340c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2340c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2340c-120">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="2340c-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




