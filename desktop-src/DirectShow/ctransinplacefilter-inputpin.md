---
description: El método InputPin recupera un puntero al pin de entrada del filtro.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Método CTransInPlaceFilter. InputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679289"
---
# <a name="ctransinplacefilterinputpin-method"></a><span data-ttu-id="3b828-103">CTransInPlaceFilter. InputPin, método</span><span class="sxs-lookup"><span data-stu-id="3b828-103">CTransInPlaceFilter.InputPin method</span></span>

<span data-ttu-id="3b828-104">El `InputPin` método recupera un puntero al pin de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="3b828-104">The `InputPin` method retrieves a pointer to the filter's input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b828-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b828-105">Syntax</span></span>


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a><span data-ttu-id="3b828-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b828-106">Parameters</span></span>

<span data-ttu-id="3b828-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3b828-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b828-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b828-108">Return value</span></span>

<span data-ttu-id="3b828-109">Devuelve la variable miembro [**CTransformFilter:: m \_ pInput**](ctransformfilter-m-pinput.md) .</span><span class="sxs-lookup"><span data-stu-id="3b828-109">Returns the [**CTransformFilter::m\_pInput**](ctransformfilter-m-pinput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b828-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b828-110">Requirements</span></span>



| <span data-ttu-id="3b828-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b828-111">Requirement</span></span> | <span data-ttu-id="3b828-112">Value</span><span class="sxs-lookup"><span data-stu-id="3b828-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b828-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b828-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3b828-114"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b828-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3b828-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b828-115">Library</span></span><br/> | <dl> <span data-ttu-id="3b828-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3b828-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b828-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b828-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b828-118">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="3b828-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




