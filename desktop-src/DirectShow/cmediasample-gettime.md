---
description: 'El método GetTime recupera los tiempos de flujo en los que este ejemplo debe comenzar y finalizar. Este método implementa el método IMediaSample:: GetTime.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Método CMediaSample. GetTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670475"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="a10df-104">CMediaSample. GetTime (método)</span><span class="sxs-lookup"><span data-stu-id="a10df-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="a10df-105">El `GetTime` método recupera los tiempos de flujo en los que este ejemplo debe comenzar y finalizar.</span><span class="sxs-lookup"><span data-stu-id="a10df-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="a10df-106">Este método implementa el método [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="a10df-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a10df-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a10df-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="a10df-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a10df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a10df-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="a10df-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a10df-110">Puntero a una variable que recibe el tiempo de secuencia inicial, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a10df-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a10df-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="a10df-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a10df-112">Puntero a una variable que recibe la hora de finalización del flujo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a10df-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="a10df-113">Si el ejemplo no tiene ninguna hora de detención, el valor se establece en la hora de inicio más una.</span><span class="sxs-lookup"><span data-stu-id="a10df-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a10df-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a10df-114">Return value</span></span>

<span data-ttu-id="a10df-115">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a10df-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a10df-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a10df-116">Return code</span></span>                                                                                                   | <span data-ttu-id="a10df-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a10df-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="a10df-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a10df-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="a10df-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a10df-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a10df-120"><dt>**VFW \_ S \_ sin \_ hora de detención \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a10df-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="a10df-121">El ejemplo tiene una hora de inicio válida, pero no una hora de detención.</span><span class="sxs-lookup"><span data-stu-id="a10df-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="a10df-122"><dt>**\_hora de ejemplo VFW E \_ \_ \_ no \_ establecida**</dt></span><span class="sxs-lookup"><span data-stu-id="a10df-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="a10df-123">El ejemplo no tiene marcas de tiempo válidas.</span><span class="sxs-lookup"><span data-stu-id="a10df-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a10df-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a10df-124">Remarks</span></span>

<span data-ttu-id="a10df-125">Las variables de miembro Start y [**CMediaSample:: m \_ End**](cmediasample-m-end.md) de [**CMediaSample:: m \_**](cmediasample-m-start.md) especifican las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a10df-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="a10df-126">La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica si las marcas de tiempo son válidas.</span><span class="sxs-lookup"><span data-stu-id="a10df-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="a10df-127">Para obtener información acerca de las marcas de tiempo, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="a10df-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a10df-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a10df-128">Requirements</span></span>



| <span data-ttu-id="a10df-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a10df-129">Requirement</span></span> | <span data-ttu-id="a10df-130">Value</span><span class="sxs-lookup"><span data-stu-id="a10df-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a10df-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a10df-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a10df-132"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a10df-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a10df-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a10df-133">Library</span></span><br/> | <dl> <span data-ttu-id="a10df-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a10df-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a10df-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a10df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a10df-136">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="a10df-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




