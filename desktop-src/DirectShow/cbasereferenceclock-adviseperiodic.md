---
description: 'El método AdvisePeriodic crea una solicitud de notificación periódica. Este método implementa el método IReferenceClock:: AdvisePeriodic.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Método CBaseReferenceClock. AdvisePeriodic (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671254"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="3f5b7-104">CBaseReferenceClock. AdvisePeriodic, método</span><span class="sxs-lookup"><span data-stu-id="3f5b7-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="3f5b7-105">El `AdvisePeriodic` método crea una solicitud de notificación periódica.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="3f5b7-106">Este método implementa el método [**IReferenceClock:: AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) .</span><span class="sxs-lookup"><span data-stu-id="3f5b7-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f5b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f5b7-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="3f5b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f5b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f5b7-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="3f5b7-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5b7-110">Hora de la primera notificación, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="3f5b7-111">Debe ser mayor que cero y menor que \_ el tiempo máximo.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="3f5b7-112">*PeriodTime*</span><span class="sxs-lookup"><span data-stu-id="3f5b7-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5b7-113">Tiempo entre notificaciones, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="3f5b7-114">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="3f5b7-115">*hSemaphore*</span><span class="sxs-lookup"><span data-stu-id="3f5b7-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5b7-116">Identificador de un semáforo, creado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="3f5b7-117">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="3f5b7-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="3f5b7-118">Puntero a una variable que recibe un identificador para la solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f5b7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f5b7-119">Return value</span></span>

<span data-ttu-id="3f5b7-120">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3f5b7-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3f5b7-121">Return code</span></span>                                                                                   | <span data-ttu-id="3f5b7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f5b7-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="3f5b7-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3f5b7-124">Correcto</span><span class="sxs-lookup"><span data-stu-id="3f5b7-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="3f5b7-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3f5b7-126">Valores de hora no válidos</span><span class="sxs-lookup"><span data-stu-id="3f5b7-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="3f5b7-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3f5b7-128">Error</span><span class="sxs-lookup"><span data-stu-id="3f5b7-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="3f5b7-129"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3f5b7-130">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="3f5b7-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f5b7-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f5b7-131">Remarks</span></span>

<span data-ttu-id="3f5b7-132">En cada momento de la notificación, el reloj libera el semáforo especificado en el parámetro *hSemaphore* .</span><span class="sxs-lookup"><span data-stu-id="3f5b7-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="3f5b7-133">Cuando no se requieran más notificaciones, llame al método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor de *pdwAdviseToken* devuelto desde esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3f5b7-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f5b7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f5b7-134">Requirements</span></span>



| <span data-ttu-id="3f5b7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f5b7-135">Requirement</span></span> | <span data-ttu-id="3f5b7-136">Value</span><span class="sxs-lookup"><span data-stu-id="3f5b7-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5b7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f5b7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="3f5b7-138"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3f5b7-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f5b7-139">Library</span></span><br/> | <dl> <span data-ttu-id="3f5b7-140"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3f5b7-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f5b7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f5b7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f5b7-142">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="3f5b7-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




