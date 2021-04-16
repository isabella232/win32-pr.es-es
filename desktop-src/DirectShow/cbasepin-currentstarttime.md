---
description: 'El método CurrentStartTime recupera la hora de inicio del segmento, establecida por el método CBasePin:: NewSegment.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Método CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671777"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="7c652-103">CBasePin. CurrentStartTime, método</span><span class="sxs-lookup"><span data-stu-id="7c652-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="7c652-104">El `CurrentStartTime` método recupera la hora de inicio del segmento, establecida por el método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="7c652-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c652-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c652-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="7c652-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c652-106">Parameters</span></span>

<span data-ttu-id="7c652-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c652-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c652-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c652-108">Return value</span></span>

<span data-ttu-id="7c652-109">Devuelve el valor de [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md).</span><span class="sxs-lookup"><span data-stu-id="7c652-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c652-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c652-110">Requirements</span></span>



| <span data-ttu-id="7c652-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c652-111">Requirement</span></span> | <span data-ttu-id="7c652-112">Value</span><span class="sxs-lookup"><span data-stu-id="7c652-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c652-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c652-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7c652-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c652-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c652-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c652-115">Library</span></span><br/> | <dl> <span data-ttu-id="7c652-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7c652-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c652-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c652-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c652-118">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7c652-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




