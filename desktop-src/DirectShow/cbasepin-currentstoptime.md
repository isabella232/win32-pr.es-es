---
description: 'El método CurrentStopTime recupera la hora de detención del segmento, establecida por el método CBasePin:: NewSegment.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Método CBasePin. CurrentStopTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660608"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="575ef-103">CBasePin. CurrentStopTime, método</span><span class="sxs-lookup"><span data-stu-id="575ef-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="575ef-104">El `CurrentStopTime` método recupera la hora de detención del segmento, establecida por el método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="575ef-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="575ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="575ef-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="575ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="575ef-106">Parameters</span></span>

<span data-ttu-id="575ef-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="575ef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="575ef-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="575ef-108">Return value</span></span>

<span data-ttu-id="575ef-109">Devuelve el valor de [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md).</span><span class="sxs-lookup"><span data-stu-id="575ef-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="575ef-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575ef-110">Requirements</span></span>



| <span data-ttu-id="575ef-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="575ef-111">Requirement</span></span> | <span data-ttu-id="575ef-112">Value</span><span class="sxs-lookup"><span data-stu-id="575ef-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575ef-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="575ef-113">Header</span></span><br/>  | <dl> <span data-ttu-id="575ef-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="575ef-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="575ef-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="575ef-115">Library</span></span><br/> | <dl> <span data-ttu-id="575ef-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="575ef-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575ef-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="575ef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575ef-118">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="575ef-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




