---
description: El método SynchronousBlockOutputPin bloquea el PIN; no devuelve ningún resultado hasta que se bloquea el PIN.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671688"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="f7170-103">CDynamicOutputPin. SynchronousBlockOutputPin, método</span><span class="sxs-lookup"><span data-stu-id="f7170-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="f7170-104">El `SynchronousBlockOutputPin` método bloquea el PIN; no vuelve hasta que no se bloquea el PIN.</span><span class="sxs-lookup"><span data-stu-id="f7170-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7170-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7170-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="f7170-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7170-106">Parameters</span></span>

<span data-ttu-id="f7170-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f7170-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7170-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7170-108">Return value</span></span>

<span data-ttu-id="f7170-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f7170-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f7170-110">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7170-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f7170-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f7170-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="f7170-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7170-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f7170-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="f7170-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f7170-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f7170-115"><dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="f7170-116">El PIN ya está bloqueado en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="f7170-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="f7170-117"><dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="f7170-118">El PIN ya está bloqueado en el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f7170-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7170-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7170-119">Remarks</span></span>

<span data-ttu-id="f7170-120">No llame a este método desde el subproceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="f7170-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7170-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7170-121">Requirements</span></span>



| <span data-ttu-id="f7170-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7170-122">Requirement</span></span> | <span data-ttu-id="f7170-123">Value</span><span class="sxs-lookup"><span data-stu-id="f7170-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7170-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7170-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f7170-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f7170-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7170-126">Library</span></span><br/> | <dl> <span data-ttu-id="f7170-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f7170-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7170-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7170-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7170-129">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="f7170-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




