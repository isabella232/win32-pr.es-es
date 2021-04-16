---
description: El método Inactive notifica al pin que el filtro se ha detenido.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Método CDynamicOutputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670341"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="28736-103">CDynamicOutputPin. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="28736-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="28736-104">El `Inactive` método notifica al pin que el filtro se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="28736-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="28736-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28736-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="28736-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28736-106">Parameters</span></span>

<span data-ttu-id="28736-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28736-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28736-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28736-108">Return value</span></span>

<span data-ttu-id="28736-109">Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="28736-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="28736-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28736-110">Remarks</span></span>

<span data-ttu-id="28736-111">Este método invalida el método [**CBaseOutputPin:: Inactive**](cbaseoutputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="28736-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="28736-112">Establece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="28736-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="28736-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28736-113">Requirements</span></span>



| <span data-ttu-id="28736-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28736-114">Requirement</span></span> | <span data-ttu-id="28736-115">Value</span><span class="sxs-lookup"><span data-stu-id="28736-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28736-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28736-116">Header</span></span><br/>  | <dl> <span data-ttu-id="28736-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28736-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="28736-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28736-118">Library</span></span><br/> | <dl> <span data-ttu-id="28736-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="28736-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28736-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="28736-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28736-121">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="28736-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




