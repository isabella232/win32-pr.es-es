---
description: El método GetDefaultTimerResolution devuelve la resolución actual del temporizador del reloj de referencia.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Método CBaseReferenceClock. GetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660589"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="489ea-103">CBaseReferenceClock. GetDefaultTimerResolution, método</span><span class="sxs-lookup"><span data-stu-id="489ea-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="489ea-104">El `GetDefaultTimerResolution` método devuelve la resolución actual del temporizador del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="489ea-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="489ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="489ea-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="489ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="489ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489ea-107">*pTimerResolution*</span><span class="sxs-lookup"><span data-stu-id="489ea-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="489ea-108">Recibe la resolución del temporizador solicitada, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="489ea-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489ea-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="489ea-109">Return value</span></span>

<span data-ttu-id="489ea-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="489ea-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="489ea-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="489ea-111">Remarks</span></span>

<span data-ttu-id="489ea-112">Este método implementa el método [**IReferenceClockTimerControl:: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="489ea-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="489ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="489ea-113">Requirements</span></span>



| <span data-ttu-id="489ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="489ea-114">Requirement</span></span> | <span data-ttu-id="489ea-115">Value</span><span class="sxs-lookup"><span data-stu-id="489ea-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489ea-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="489ea-116">Header</span></span><br/>  | <dl> <span data-ttu-id="489ea-117"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="489ea-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="489ea-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="489ea-118">Library</span></span><br/> | <dl> <span data-ttu-id="489ea-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="489ea-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489ea-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="489ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489ea-121">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="489ea-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




