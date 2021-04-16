---
description: El método activo notifica al pin que el filtro está activo ahora.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671761"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="1d61b-103">CDynamicOutputPin. Active (método)</span><span class="sxs-lookup"><span data-stu-id="1d61b-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="1d61b-104">El `Active` método notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="1d61b-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d61b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d61b-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="1d61b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d61b-106">Parameters</span></span>

<span data-ttu-id="1d61b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d61b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d61b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d61b-108">Return value</span></span>

<span data-ttu-id="1d61b-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d61b-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d61b-110">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d61b-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1d61b-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1d61b-111">Return code</span></span>                                                                            | <span data-ttu-id="1d61b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d61b-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d61b-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1d61b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1d61b-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1d61b-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="1d61b-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="1d61b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1d61b-116">Error.</span><span class="sxs-lookup"><span data-stu-id="1d61b-116">Failure.</span></span> <span data-ttu-id="1d61b-117">No se llamó a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1d61b-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d61b-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d61b-118">Remarks</span></span>

<span data-ttu-id="1d61b-119">Este método invalida el método [**CBaseOutputPin:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="1d61b-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="1d61b-120">Restablece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="1d61b-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="1d61b-121">Si el filtro propietario no ha llamado a **SetConfigInfo**, este método devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="1d61b-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d61b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d61b-122">Requirements</span></span>



| <span data-ttu-id="1d61b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d61b-123">Requirement</span></span> | <span data-ttu-id="1d61b-124">Value</span><span class="sxs-lookup"><span data-stu-id="1d61b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d61b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d61b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1d61b-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d61b-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1d61b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d61b-127">Library</span></span><br/> | <dl> <span data-ttu-id="1d61b-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1d61b-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d61b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d61b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d61b-130">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="1d61b-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




