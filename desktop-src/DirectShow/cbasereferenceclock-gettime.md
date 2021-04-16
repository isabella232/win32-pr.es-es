---
description: 'El método GetTime recupera la hora de referencia actual. Este método implementa el método IReferenceClock:: GetTime.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Método CBaseReferenceClock. GetTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671531"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="33ac7-104">CBaseReferenceClock. GetTime (método)</span><span class="sxs-lookup"><span data-stu-id="33ac7-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="33ac7-105">El `GetTime` método recupera la hora de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="33ac7-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="33ac7-106">Este método implementa el método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="33ac7-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ac7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33ac7-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="33ac7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33ac7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ac7-109">*pTime*</span><span class="sxs-lookup"><span data-stu-id="33ac7-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="33ac7-110">Puntero a una variable que recibe la hora actual, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="33ac7-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ac7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33ac7-111">Return value</span></span>

<span data-ttu-id="33ac7-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="33ac7-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="33ac7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="33ac7-113">Return code</span></span>                                                                               | <span data-ttu-id="33ac7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="33ac7-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="33ac7-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="33ac7-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="33ac7-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="33ac7-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="33ac7-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="33ac7-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="33ac7-118">La hora devuelta es igual que el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="33ac7-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="33ac7-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="33ac7-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="33ac7-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="33ac7-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="33ac7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33ac7-121">Remarks</span></span>

<span data-ttu-id="33ac7-122">Este método llama al método [**CBaseReferenceClock:: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) para determinar la hora real del reloj.</span><span class="sxs-lookup"><span data-stu-id="33ac7-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="33ac7-123">Si la hora del reloj es estrictamente mayor que el valor anterior, `GetTime` usa la hora de reloj y devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="33ac7-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="33ac7-124">De lo contrario, `GetTime` utiliza el valor anterior y devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="33ac7-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="33ac7-125">Por lo tanto, el reloj interno puede ejecutarse hacia atrás durante un breve período, sin provocar que el tiempo de referencia se ejecute hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="33ac7-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="33ac7-126">En su lugar, el tiempo de referencia se "detendrá" en el mismo valor hasta que el reloj interno se ponga al día.</span><span class="sxs-lookup"><span data-stu-id="33ac7-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ac7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ac7-127">Requirements</span></span>



| <span data-ttu-id="33ac7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ac7-128">Requirement</span></span> | <span data-ttu-id="33ac7-129">Value</span><span class="sxs-lookup"><span data-stu-id="33ac7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ac7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33ac7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="33ac7-131"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33ac7-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33ac7-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33ac7-132">Library</span></span><br/> | <dl> <span data-ttu-id="33ac7-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="33ac7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ac7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="33ac7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ac7-135">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="33ac7-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




