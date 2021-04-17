---
description: El método GetPinCount recupera el número de clavijas en el filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661036"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="9ef2d-103">CTransformFilter. GetPinCount, método</span><span class="sxs-lookup"><span data-stu-id="9ef2d-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="9ef2d-104">El `GetPinCount` método recupera el número de clavijas en el filtro.</span><span class="sxs-lookup"><span data-stu-id="9ef2d-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ef2d-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="9ef2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ef2d-106">Parameters</span></span>

<span data-ttu-id="9ef2d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ef2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ef2d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ef2d-108">Return value</span></span>

<span data-ttu-id="9ef2d-109">Devuelve 2.</span><span class="sxs-lookup"><span data-stu-id="9ef2d-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef2d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ef2d-110">Remarks</span></span>

<span data-ttu-id="9ef2d-111">Este método invalida el método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef2d-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="9ef2d-112">La clase **CTransformFilter** admite exactamente un PIN de entrada y un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="9ef2d-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef2d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef2d-113">Requirements</span></span>



| <span data-ttu-id="9ef2d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef2d-114">Requirement</span></span> | <span data-ttu-id="9ef2d-115">Value</span><span class="sxs-lookup"><span data-stu-id="9ef2d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef2d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ef2d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9ef2d-117"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef2d-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ef2d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ef2d-118">Library</span></span><br/> | <dl> <span data-ttu-id="9ef2d-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef2d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef2d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ef2d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef2d-121">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9ef2d-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




