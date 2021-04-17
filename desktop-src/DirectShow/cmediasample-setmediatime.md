---
description: 'El método SetMediaTime establece las horas de los medios para este ejemplo. Este método implementa el método IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Método CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670529"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="bdda8-104">CMediaSample. SetMediaTime, método</span><span class="sxs-lookup"><span data-stu-id="bdda8-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="bdda8-105">El `SetMediaTime` método establece las horas de los medios para este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bdda8-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="bdda8-106">Este método implementa el método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="bdda8-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdda8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdda8-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="bdda8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdda8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdda8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="bdda8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bdda8-110">Puntero a la hora de inicio del medio o **null**.</span><span class="sxs-lookup"><span data-stu-id="bdda8-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdda8-111">*Pendiente*</span><span class="sxs-lookup"><span data-stu-id="bdda8-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bdda8-112">Puntero a la hora de detención del medio o **null**.</span><span class="sxs-lookup"><span data-stu-id="bdda8-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdda8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdda8-113">Return value</span></span>

<span data-ttu-id="bdda8-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="bdda8-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdda8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdda8-115">Remarks</span></span>

<span data-ttu-id="bdda8-116">La hora de detención del medio debe ser mayor que la hora de inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="bdda8-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="bdda8-117">Use **null** para invalidar las horas de los medios.</span><span class="sxs-lookup"><span data-stu-id="bdda8-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="bdda8-118">El parámetro *pendiente* especifica una hora de medio absoluta, pero la variable miembro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) se calcula como un desplazamiento desde *pStart*.</span><span class="sxs-lookup"><span data-stu-id="bdda8-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="bdda8-119">En otras palabras, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  </span><span class="sxs-lookup"><span data-stu-id="bdda8-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="bdda8-120">Para obtener información sobre las horas de los medios, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="bdda8-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdda8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdda8-121">Requirements</span></span>



| <span data-ttu-id="bdda8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdda8-122">Requirement</span></span> | <span data-ttu-id="bdda8-123">Value</span><span class="sxs-lookup"><span data-stu-id="bdda8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdda8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdda8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bdda8-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdda8-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdda8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdda8-126">Library</span></span><br/> | <dl> <span data-ttu-id="bdda8-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bdda8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdda8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdda8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdda8-129">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="bdda8-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




