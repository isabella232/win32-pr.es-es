---
description: El método SetTimeDelta ajusta la hora interna del reloj.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock. SetTimeDelta (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671526"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="78374-103">CBaseReferenceClock. SetTimeDelta, método</span><span class="sxs-lookup"><span data-stu-id="78374-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="78374-104">El `SetTimeDelta` método ajusta la hora interna del reloj.</span><span class="sxs-lookup"><span data-stu-id="78374-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="78374-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78374-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="78374-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78374-107">*TimeDelta* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="78374-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="78374-108">Cantidad para ajustar la hora del reloj, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="78374-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="78374-109">Un valor positivo mueve el reloj hacia delante y un valor negativo mueve el reloj hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="78374-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78374-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78374-110">Return value</span></span>

<span data-ttu-id="78374-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="78374-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="78374-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78374-112">Remarks</span></span>

<span data-ttu-id="78374-113">La clase derivada puede usar este método para ajustar el reloj interno, si se desplaza desde el dispositivo que está proporcionando información de tiempo.</span><span class="sxs-lookup"><span data-stu-id="78374-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="78374-114">El método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) nunca devuelve valores decrecientes.</span><span class="sxs-lookup"><span data-stu-id="78374-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="78374-115">Si ajusta el reloj hacia atrás, **getTime** devuelve el valor anterior hasta que el reloj llega a ese valor de nuevo.</span><span class="sxs-lookup"><span data-stu-id="78374-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="78374-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78374-116">Requirements</span></span>



| <span data-ttu-id="78374-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="78374-117">Requirement</span></span> | <span data-ttu-id="78374-118">Value</span><span class="sxs-lookup"><span data-stu-id="78374-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78374-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78374-119">Header</span></span><br/>  | <dl> <span data-ttu-id="78374-120"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78374-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78374-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78374-121">Library</span></span><br/> | <dl> <span data-ttu-id="78374-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="78374-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78374-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="78374-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78374-124">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="78374-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




