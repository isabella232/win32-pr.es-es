---
description: 'El método InterésActual recupera la velocidad de segmento, establecida por el método CBasePin:: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Método CBasePin. InterésActual (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660182"
---
# <a name="cbasepincurrentrate-method"></a><span data-ttu-id="f3044-103">CBasePin. InterésActual, método</span><span class="sxs-lookup"><span data-stu-id="f3044-103">CBasePin.CurrentRate method</span></span>

<span data-ttu-id="f3044-104">El `CurrentRate` método recupera la velocidad de segmento, establecida por el método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="f3044-104">The `CurrentRate` method retrieves the segment rate, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3044-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3044-105">Syntax</span></span>


```C++
double CurrentRate();
```



## <a name="parameters"></a><span data-ttu-id="f3044-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3044-106">Parameters</span></span>

<span data-ttu-id="f3044-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f3044-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3044-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3044-108">Return value</span></span>

<span data-ttu-id="f3044-109">Devuelve el valor de [**CBasePin:: m \_ dRate**](cbasepin-m-drate.md).</span><span class="sxs-lookup"><span data-stu-id="f3044-109">Returns the value of [**CBasePin::m\_dRate**](cbasepin-m-drate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3044-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3044-110">Requirements</span></span>



| <span data-ttu-id="f3044-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3044-111">Requirement</span></span> | <span data-ttu-id="f3044-112">Value</span><span class="sxs-lookup"><span data-stu-id="f3044-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3044-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3044-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f3044-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3044-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3044-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3044-115">Library</span></span><br/> | <dl> <span data-ttu-id="f3044-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f3044-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3044-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3044-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3044-118">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f3044-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




