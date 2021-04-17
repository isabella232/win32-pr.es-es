---
description: 'El método AdviseTime crea una solicitud de notificación de una captura. Este método implementa el método IReferenceClock:: AdviseTime.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Método CBaseReferenceClock. AdviseTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660941"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="e6367-104">CBaseReferenceClock. AdviseTime, método</span><span class="sxs-lookup"><span data-stu-id="e6367-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="e6367-105">El `AdviseTime` método crea una solicitud de notificación de una captura.</span><span class="sxs-lookup"><span data-stu-id="e6367-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="e6367-106">Este método implementa el método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .</span><span class="sxs-lookup"><span data-stu-id="e6367-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6367-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6367-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="e6367-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6367-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6367-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="e6367-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e6367-110">Tiempo de referencia base, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e6367-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e6367-111">*streamTime*</span><span class="sxs-lookup"><span data-stu-id="e6367-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e6367-112">Tiempo de desplazamiento de flujo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="e6367-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e6367-113">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="e6367-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="e6367-114">Identificador de un evento creado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e6367-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="e6367-115">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="e6367-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="e6367-116">Puntero a una variable que recibe un identificador para la solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="e6367-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6367-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6367-117">Return value</span></span>

<span data-ttu-id="e6367-118">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e6367-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e6367-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e6367-119">Return code</span></span>                                                                                   | <span data-ttu-id="e6367-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6367-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="e6367-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e6367-122">Correcto</span><span class="sxs-lookup"><span data-stu-id="e6367-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="e6367-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e6367-124">Valores de hora no válidos</span><span class="sxs-lookup"><span data-stu-id="e6367-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="e6367-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e6367-126">Error</span><span class="sxs-lookup"><span data-stu-id="e6367-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="e6367-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e6367-128">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="e6367-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6367-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6367-129">Remarks</span></span>

<span data-ttu-id="e6367-130">Este método crea una solicitud de notificación de una captura para el tiempo de referencia *baseTime*  +  *streamTime*.</span><span class="sxs-lookup"><span data-stu-id="e6367-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="e6367-131">La suma debe ser mayor que cero y menor que \_ el tiempo máximo, o el método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e6367-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="e6367-132">En el momento solicitado, el reloj señala el evento especificado en el parámetro *hEvent* .</span><span class="sxs-lookup"><span data-stu-id="e6367-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="e6367-133">Para cancelar la notificación antes de que se alcance el tiempo, llame al método [**CBaseReferenceClock:: Unadvise**](cbasereferenceclock-unadvise.md) y pase el valor de *pdwAdviseToken* devuelto desde esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e6367-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="e6367-134">Una vez que se ha producido la notificación, el reloj la borra automáticamente, por lo que no es necesario llamar a **unvise**.</span><span class="sxs-lookup"><span data-stu-id="e6367-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="e6367-135">Sin embargo, no es un error hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e6367-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6367-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6367-136">Requirements</span></span>



| <span data-ttu-id="e6367-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6367-137">Requirement</span></span> | <span data-ttu-id="e6367-138">Value</span><span class="sxs-lookup"><span data-stu-id="e6367-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6367-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6367-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e6367-140"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6367-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6367-141">Library</span></span><br/> | <dl> <span data-ttu-id="e6367-142"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6367-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6367-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6367-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6367-144">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="e6367-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




