---
description: El método EndOfStream notifica al filtro que el PIN de entrada ha recibido una notificación de final de secuencia.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Método CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660754"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="92893-103">CBaseRenderer. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="92893-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="92893-104">El `EndOfStream` método notifica al filtro que el PIN de entrada ha recibido una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="92893-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="92893-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92893-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="92893-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92893-106">Parameters</span></span>

<span data-ttu-id="92893-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="92893-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92893-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92893-108">Return value</span></span>

<span data-ttu-id="92893-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="92893-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="92893-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92893-110">Remarks</span></span>

<span data-ttu-id="92893-111">El PIN de entrada del filtro llama a este método cuando recibe una notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="92893-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="92893-112">Este método establece la [**marca CBaseRenderer:: m \_ BeOS**](cbaserenderer-m-beos.md) en **true** y llama al método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) para programar un evento de [**\_ finalización de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="92893-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="92893-113">Si el filtro está en pausa y en espera de un ejemplo, este método completa la transición de estado.</span><span class="sxs-lookup"><span data-stu-id="92893-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="92893-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92893-114">Requirements</span></span>



| <span data-ttu-id="92893-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92893-115">Requirement</span></span> | <span data-ttu-id="92893-116">Value</span><span class="sxs-lookup"><span data-stu-id="92893-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92893-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92893-117">Header</span></span><br/>  | <dl> <span data-ttu-id="92893-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92893-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92893-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92893-119">Library</span></span><br/> | <dl> <span data-ttu-id="92893-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="92893-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92893-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="92893-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92893-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="92893-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




