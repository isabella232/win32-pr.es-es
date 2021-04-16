---
description: El método TriggerThread reactiva el subproceso de trabajo que controla la programación.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Método CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671525"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="6982f-103">CBaseReferenceClock. TriggerThread, método</span><span class="sxs-lookup"><span data-stu-id="6982f-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="6982f-104">El `TriggerThread` método reactiva el subproceso de trabajo que controla la programación.</span><span class="sxs-lookup"><span data-stu-id="6982f-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="6982f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6982f-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="6982f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6982f-106">Parameters</span></span>

<span data-ttu-id="6982f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6982f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6982f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6982f-108">Return value</span></span>

<span data-ttu-id="6982f-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6982f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6982f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6982f-110">Remarks</span></span>

<span data-ttu-id="6982f-111">El reloj usa un subproceso de trabajo que llama al método [**CAMSchedule:: Advise**](camschedule-advise.md) en los momentos adecuados.</span><span class="sxs-lookup"><span data-stu-id="6982f-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="6982f-112">La clase derivada puede llamar `TriggerThread` a para reactivar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="6982f-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="6982f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6982f-113">Requirements</span></span>



| <span data-ttu-id="6982f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6982f-114">Requirement</span></span> | <span data-ttu-id="6982f-115">Value</span><span class="sxs-lookup"><span data-stu-id="6982f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6982f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6982f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6982f-117"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6982f-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6982f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6982f-118">Library</span></span><br/> | <dl> <span data-ttu-id="6982f-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6982f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6982f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6982f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6982f-121">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="6982f-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




