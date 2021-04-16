---
description: 'El método SetTime establece los tiempos de flujo en los que este ejemplo debe comenzar y finalizar. Este método implementa el método IMediaSample:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Método CMediaSample. SetTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678888"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="2e886-104">CMediaSample. SetTime, método</span><span class="sxs-lookup"><span data-stu-id="2e886-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="2e886-105">El `SetTime` método establece los tiempos de flujo en los que este ejemplo debe comenzar y finalizar.</span><span class="sxs-lookup"><span data-stu-id="2e886-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="2e886-106">Este método implementa el método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="2e886-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e886-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e886-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="2e886-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e886-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e886-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="2e886-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2e886-110">Puntero a la hora de flujo en la que comienza el ejemplo, en unidades de 100-nanosegundos o **null**.</span><span class="sxs-lookup"><span data-stu-id="2e886-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2e886-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="2e886-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2e886-112">Puntero a la hora de flujo en la que finaliza el ejemplo, en unidades 100-nanosegundos, o **null**.</span><span class="sxs-lookup"><span data-stu-id="2e886-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e886-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e886-113">Return value</span></span>

<span data-ttu-id="2e886-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2e886-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e886-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e886-115">Remarks</span></span>

<span data-ttu-id="2e886-116">Este método establece las variables de miembro de [**Inicio CMediaSample:: m \_ Start**](cmediasample-m-start.md) y [**CMediaSample:: m \_ End**](cmediasample-m-end.md) , que especifican las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2e886-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="2e886-117">También actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica si las marcas de tiempo son válidas.</span><span class="sxs-lookup"><span data-stu-id="2e886-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="2e886-118">Para obtener información acerca de las marcas de tiempo, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="2e886-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e886-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e886-119">Requirements</span></span>



| <span data-ttu-id="2e886-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e886-120">Requirement</span></span> | <span data-ttu-id="2e886-121">Value</span><span class="sxs-lookup"><span data-stu-id="2e886-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e886-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e886-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2e886-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e886-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2e886-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e886-124">Library</span></span><br/> | <dl> <span data-ttu-id="2e886-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2e886-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e886-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e886-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e886-127">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="2e886-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




