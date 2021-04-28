---
description: 'Método CDynamicOutputPin.Active: el método Active notifica al pin que el filtro ahora está activo.'
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin.Active (Amfilter.h)
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
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099333"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="b3a1e-103">Método CDynamicOutputPin.Active</span><span class="sxs-lookup"><span data-stu-id="b3a1e-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="b3a1e-104">El `Active` método notifica al pin que el filtro ahora está activo.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3a1e-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="b3a1e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3a1e-106">Parameters</span></span>

<span data-ttu-id="b3a1e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3a1e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3a1e-108">Return value</span></span>

<span data-ttu-id="b3a1e-109">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b3a1e-110">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b3a1e-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b3a1e-111">Return code</span></span>                                                                            | <span data-ttu-id="b3a1e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a1e-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3a1e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b3a1e-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="b3a1e-115"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b3a1e-116">Error.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-116">Failure.</span></span> <span data-ttu-id="b3a1e-117">[**No se llamó a CDynamicOutputPin::SetConfigInfo.**](cdynamicoutputpin-setconfiginfo.md)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3a1e-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3a1e-118">Remarks</span></span>

<span data-ttu-id="b3a1e-119">Este método invalida el [**método CBaseOutputPin::Active.**](cbaseoutputpin-active.md)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="b3a1e-120">Restablece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="b3a1e-121">Si el filtro propietario no ha llamado a **SetConfigInfo**, este método devuelve E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a1e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3a1e-122">Requirements</span></span>



| <span data-ttu-id="b3a1e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a1e-123">Requirement</span></span> | <span data-ttu-id="b3a1e-124">Value</span><span class="sxs-lookup"><span data-stu-id="b3a1e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a1e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3a1e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a1e-126"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1e-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3a1e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3a1e-127">Library</span></span><br/> | <dl> <span data-ttu-id="b3a1e-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1e-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a1e-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3a1e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a1e-130">**CDynamicOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




