---
description: 'El método SetClockDelta ajusta la hora de reloj. Este método implementa el método IAMClockAdjust:: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Método CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660167"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="4127d-104">CSystemClock. SetClockDelta, método</span><span class="sxs-lookup"><span data-stu-id="4127d-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="4127d-105">El `SetClockDelta` método ajusta la hora de reloj.</span><span class="sxs-lookup"><span data-stu-id="4127d-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="4127d-106">Este método implementa el método [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .</span><span class="sxs-lookup"><span data-stu-id="4127d-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4127d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4127d-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="4127d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4127d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4127d-109">*rtDelta*</span><span class="sxs-lookup"><span data-stu-id="4127d-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="4127d-110">Especifica la cantidad por la que se va a ajustar el reloj, como un valor de [**\_ tiempo de referencia**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="4127d-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="4127d-111">Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="4127d-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4127d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4127d-112">Return value</span></span>

<span data-ttu-id="4127d-113">Devuelve \_ un código de error de correcto o **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4127d-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4127d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4127d-114">Remarks</span></span>

<span data-ttu-id="4127d-115">Este método simplemente llama a [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span><span class="sxs-lookup"><span data-stu-id="4127d-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="4127d-116">Los valores de hora devueltos por [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aumentan de forma continuada.</span><span class="sxs-lookup"><span data-stu-id="4127d-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="4127d-117">Si vuelve a establecer el reloj, **getTime** continúa notificando la hora anterior hasta que el reloj interno se pone al día.</span><span class="sxs-lookup"><span data-stu-id="4127d-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="4127d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4127d-118">Requirements</span></span>



| <span data-ttu-id="4127d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4127d-119">Requirement</span></span> | <span data-ttu-id="4127d-120">Value</span><span class="sxs-lookup"><span data-stu-id="4127d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4127d-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4127d-121">Version</span></span><br/> | <span data-ttu-id="4127d-122">Clase CSystemClock</span><span class="sxs-lookup"><span data-stu-id="4127d-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="4127d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4127d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4127d-124"><dt>Sysclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4127d-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4127d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4127d-125">Library</span></span><br/> | <dl> <span data-ttu-id="4127d-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4127d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




