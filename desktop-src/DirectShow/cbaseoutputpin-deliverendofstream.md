---
description: El método DeliverEndOfStream entrega una notificación de final de secuencia al pin de entrada conectado.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Método CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661164"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="9c7e2-103">CBaseOutputPin. DeliverEndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="9c7e2-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="9c7e2-104">El `DeliverEndOfStream` método entrega una notificación de final de secuencia al pin de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c7e2-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="9c7e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c7e2-106">Parameters</span></span>

<span data-ttu-id="9c7e2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c7e2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c7e2-108">Return value</span></span>

<span data-ttu-id="9c7e2-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9c7e2-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9c7e2-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9c7e2-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c7e2-111">Return code</span></span>                                                                                           | <span data-ttu-id="9c7e2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c7e2-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9c7e2-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e2-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9c7e2-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="9c7e2-115"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e2-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9c7e2-116">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c7e2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c7e2-117">Remarks</span></span>

<span data-ttu-id="9c7e2-118">Este método llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="9c7e2-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c7e2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c7e2-119">Requirements</span></span>



| <span data-ttu-id="9c7e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c7e2-120">Requirement</span></span> | <span data-ttu-id="9c7e2-121">Value</span><span class="sxs-lookup"><span data-stu-id="9c7e2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7e2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c7e2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9c7e2-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e2-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9c7e2-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c7e2-124">Library</span></span><br/> | <dl> <span data-ttu-id="9c7e2-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9c7e2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c7e2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c7e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c7e2-127">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="9c7e2-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




