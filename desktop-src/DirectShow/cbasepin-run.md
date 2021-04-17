---
description: El método Run notifica al pin que el filtro se está ejecutando ahora.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Método CBasePin. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670872"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="ba40d-103">CBasePin. Run (método)</span><span class="sxs-lookup"><span data-stu-id="ba40d-103">CBasePin.Run method</span></span>

<span data-ttu-id="ba40d-104">El `Run` método notifica al pin que el filtro se está ejecutando ahora.</span><span class="sxs-lookup"><span data-stu-id="ba40d-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba40d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba40d-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="ba40d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba40d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba40d-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="ba40d-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ba40d-108">Hora de inicio que se pasa al método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) del filtro.</span><span class="sxs-lookup"><span data-stu-id="ba40d-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba40d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba40d-109">Return value</span></span>

<span data-ttu-id="ba40d-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ba40d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba40d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba40d-111">Remarks</span></span>

<span data-ttu-id="ba40d-112">Cuando el filtro pasa de pausado a en ejecución, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="ba40d-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="ba40d-113">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="ba40d-113">This method does nothing in the base class.</span></span> <span data-ttu-id="ba40d-114">Las clases derivadas pueden invalidar este método.</span><span class="sxs-lookup"><span data-stu-id="ba40d-114">Derived classes can override this method.</span></span> <span data-ttu-id="ba40d-115">Por ejemplo, un PIN podría iniciar un subproceso de trabajo que entregue ejemplos.</span><span class="sxs-lookup"><span data-stu-id="ba40d-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="ba40d-116">El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve esta función miembro, de modo que no se prueba el estado desde este método.</span><span class="sxs-lookup"><span data-stu-id="ba40d-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba40d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba40d-117">Requirements</span></span>



| <span data-ttu-id="ba40d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba40d-118">Requirement</span></span> | <span data-ttu-id="ba40d-119">Value</span><span class="sxs-lookup"><span data-stu-id="ba40d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba40d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba40d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ba40d-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba40d-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba40d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba40d-122">Library</span></span><br/> | <dl> <span data-ttu-id="ba40d-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ba40d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba40d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba40d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba40d-125">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="ba40d-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




