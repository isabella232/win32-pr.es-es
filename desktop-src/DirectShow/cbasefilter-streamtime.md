---
description: 'Método CBaseFilter.StreamTime: el método StreamTime recupera el tiempo de transmisión actual.'
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Método CBaseFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120073"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="29329-103">Método CBaseFilter.StreamTime</span><span class="sxs-lookup"><span data-stu-id="29329-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="29329-104">El **método StreamTime** recupera el tiempo de secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="29329-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="29329-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29329-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="29329-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29329-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="29329-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="29329-108">Referencia a un [**objeto CRefTime**](creftime.md) que recibe el tiempo de secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="29329-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29329-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29329-109">Return value</span></span>

<span data-ttu-id="29329-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="29329-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="29329-111">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="29329-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="29329-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="29329-112">Return code</span></span>                                                                                      | <span data-ttu-id="29329-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="29329-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="29329-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29329-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="29329-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="29329-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="29329-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="29329-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="29329-117">No hay ningún reloj de referencia disponible.</span><span class="sxs-lookup"><span data-stu-id="29329-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29329-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29329-118">Remarks</span></span>

<span data-ttu-id="29329-119">La hora de la secuencia se define como la hora de referencia actual (según lo indicado por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseFilter::m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="29329-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="29329-120">La marca de tiempo de *un ejemplo multimedia* especifica el tiempo de secuencia en el que se debe representar.</span><span class="sxs-lookup"><span data-stu-id="29329-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="29329-121">Si aún no se ha representado un ejemplo con una marca de tiempo inferior a la hora de transmisión actual, es tarde.</span><span class="sxs-lookup"><span data-stu-id="29329-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="29329-122">Este método obtiene el tiempo de secuencia llamando a [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener la hora de referencia actual y restando la hora de inicio inicial.</span><span class="sxs-lookup"><span data-stu-id="29329-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="29329-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29329-123">Requirements</span></span>



| <span data-ttu-id="29329-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29329-124">Requirement</span></span> | <span data-ttu-id="29329-125">Value</span><span class="sxs-lookup"><span data-stu-id="29329-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29329-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29329-126">Header</span></span><br/>  | <dl> <span data-ttu-id="29329-127"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="29329-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="29329-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29329-128">Library</span></span><br/> | <dl> <span data-ttu-id="29329-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="29329-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29329-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29329-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29329-131">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="29329-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="29329-132">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="29329-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




