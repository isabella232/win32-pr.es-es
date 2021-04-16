---
description: El método SetDefaultTimerResolution establece la resolución del temporizador del reloj de referencia.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Método CBaseReferenceClock. SetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671529"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="0e7a6-103">CBaseReferenceClock. SetDefaultTimerResolution, método</span><span class="sxs-lookup"><span data-stu-id="0e7a6-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="0e7a6-104">El `SetDefaultTimerResolution` método establece la resolución del temporizador del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="0e7a6-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e7a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e7a6-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="0e7a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e7a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e7a6-107">*timerResolution*</span><span class="sxs-lookup"><span data-stu-id="0e7a6-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="0e7a6-108">Resolución mínima del temporizador, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="0e7a6-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="0e7a6-109">Si el valor es cero, el reloj de referencia cancela su solicitud anterior.</span><span class="sxs-lookup"><span data-stu-id="0e7a6-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e7a6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e7a6-110">Return value</span></span>

<span data-ttu-id="0e7a6-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e7a6-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e7a6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e7a6-112">Remarks</span></span>

<span data-ttu-id="0e7a6-113">Este método implementa el método [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="0e7a6-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e7a6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e7a6-114">Requirements</span></span>



| <span data-ttu-id="0e7a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e7a6-115">Requirement</span></span> | <span data-ttu-id="0e7a6-116">Value</span><span class="sxs-lookup"><span data-stu-id="0e7a6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7a6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e7a6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0e7a6-118"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e7a6-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0e7a6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e7a6-119">Library</span></span><br/> | <dl> <span data-ttu-id="0e7a6-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0e7a6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e7a6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e7a6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e7a6-122">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="0e7a6-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




