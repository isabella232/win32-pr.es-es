---
description: El método OutputPin recupera un puntero al pin de salida del filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Método CTransInPlaceFilter. OutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680201"
---
# <a name="ctransinplacefilteroutputpin-method"></a><span data-ttu-id="810ab-103">CTransInPlaceFilter. OutputPin, método</span><span class="sxs-lookup"><span data-stu-id="810ab-103">CTransInPlaceFilter.OutputPin method</span></span>

<span data-ttu-id="810ab-104">El `OutputPin` método recupera un puntero a la clavija de salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="810ab-104">The `OutputPin` method retrieves a pointer to the filter's output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="810ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="810ab-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a><span data-ttu-id="810ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="810ab-106">Parameters</span></span>

<span data-ttu-id="810ab-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="810ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="810ab-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="810ab-108">Return value</span></span>

<span data-ttu-id="810ab-109">Devuelve la variable miembro [**CTransformFilter:: m \_ pOutput**](ctransformfilter-m-poutput.md) .</span><span class="sxs-lookup"><span data-stu-id="810ab-109">Returns the [**CTransformFilter::m\_pOutput**](ctransformfilter-m-poutput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="810ab-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="810ab-110">Requirements</span></span>



| <span data-ttu-id="810ab-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="810ab-111">Requirement</span></span> | <span data-ttu-id="810ab-112">Value</span><span class="sxs-lookup"><span data-stu-id="810ab-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810ab-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="810ab-113">Header</span></span><br/>  | <dl> <span data-ttu-id="810ab-114"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="810ab-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="810ab-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="810ab-115">Library</span></span><br/> | <dl> <span data-ttu-id="810ab-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="810ab-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810ab-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="810ab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810ab-118">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="810ab-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




