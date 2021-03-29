---
description: 'El método GetMediaTime recupera las horas de los medios de este ejemplo. Este método implementa el método IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679296"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="e3421-104">CMediaSample. GetMediaTime, método</span><span class="sxs-lookup"><span data-stu-id="e3421-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="e3421-105">El `GetMediaTime` método recupera las horas de los medios de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e3421-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="e3421-106">Este método implementa el método [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .</span><span class="sxs-lookup"><span data-stu-id="e3421-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3421-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3421-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="e3421-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3421-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="e3421-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="e3421-110">Puntero a una variable que recibe la hora de inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="e3421-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="e3421-111">*Pendiente*</span><span class="sxs-lookup"><span data-stu-id="e3421-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e3421-112">Puntero a una variable que recibe la hora de detención del medio.</span><span class="sxs-lookup"><span data-stu-id="e3421-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3421-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3421-113">Return value</span></span>

<span data-ttu-id="e3421-114">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e3421-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e3421-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3421-115">Return code</span></span>                                                                                                  | <span data-ttu-id="e3421-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3421-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="e3421-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e3421-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e3421-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e3421-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e3421-119"><dt>**\_tiempo medio de VFW E \_ \_ \_ no \_ establecido**</dt></span><span class="sxs-lookup"><span data-stu-id="e3421-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="e3421-120">No se establecieron tiempos multimedia para este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e3421-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3421-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3421-121">Remarks</span></span>

<span data-ttu-id="e3421-122">La variable miembro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica un desplazamiento desde [**CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), pero el valor recibido por el parámetro *pendiente* es un tiempo medio absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.</span><span class="sxs-lookup"><span data-stu-id="e3421-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="e3421-123">Para obtener información sobre las horas de los medios, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e3421-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3421-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3421-124">Requirements</span></span>



| <span data-ttu-id="e3421-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3421-125">Requirement</span></span> | <span data-ttu-id="e3421-126">Value</span><span class="sxs-lookup"><span data-stu-id="e3421-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3421-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3421-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e3421-128"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3421-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e3421-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3421-129">Library</span></span><br/> | <dl> <span data-ttu-id="e3421-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e3421-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3421-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3421-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3421-132">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="e3421-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




