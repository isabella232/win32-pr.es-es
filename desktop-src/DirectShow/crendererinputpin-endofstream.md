---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método invalida el método CBasePin:: EndOfStream.'
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Método CRendererInputPin. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671704"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="1cbfc-104">CRendererInputPin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="1cbfc-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="1cbfc-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="1cbfc-106">Este método invalida el método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="1cbfc-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbfc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cbfc-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="1cbfc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cbfc-108">Parameters</span></span>

<span data-ttu-id="1cbfc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cbfc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cbfc-110">Return value</span></span>

<span data-ttu-id="1cbfc-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cbfc-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbfc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbfc-112">Requirements</span></span>



| <span data-ttu-id="1cbfc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbfc-113">Requirement</span></span> | <span data-ttu-id="1cbfc-114">Value</span><span class="sxs-lookup"><span data-stu-id="1cbfc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbfc-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cbfc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1cbfc-116"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbfc-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1cbfc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cbfc-117">Library</span></span><br/> | <dl> <span data-ttu-id="1cbfc-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbfc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbfc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cbfc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbfc-120">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="1cbfc-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




