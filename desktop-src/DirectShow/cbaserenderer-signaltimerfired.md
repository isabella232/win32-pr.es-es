---
description: El método SignalTimerFired borra el identificador del temporizador que se usa para programar la representación.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671671"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="381f6-103">CBaseRenderer. SignalTimerFired, método</span><span class="sxs-lookup"><span data-stu-id="381f6-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="381f6-104">El `SignalTimerFired` método borra el identificador del temporizador que se usa para programar la representación.</span><span class="sxs-lookup"><span data-stu-id="381f6-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="381f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="381f6-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="381f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="381f6-106">Parameters</span></span>

<span data-ttu-id="381f6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="381f6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="381f6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="381f6-108">Return value</span></span>

<span data-ttu-id="381f6-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="381f6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="381f6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="381f6-110">Remarks</span></span>

<span data-ttu-id="381f6-111">El filtro llama a este método cuando se activa el temporizador de representación (vea [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) o cuando se cancela el temporizador (vea [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="381f6-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="381f6-112">El método restablece la variable miembro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) en cero.</span><span class="sxs-lookup"><span data-stu-id="381f6-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="381f6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="381f6-113">Requirements</span></span>



| <span data-ttu-id="381f6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="381f6-114">Requirement</span></span> | <span data-ttu-id="381f6-115">Value</span><span class="sxs-lookup"><span data-stu-id="381f6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="381f6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="381f6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="381f6-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="381f6-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="381f6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="381f6-118">Library</span></span><br/> | <dl> <span data-ttu-id="381f6-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="381f6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381f6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="381f6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381f6-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="381f6-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




