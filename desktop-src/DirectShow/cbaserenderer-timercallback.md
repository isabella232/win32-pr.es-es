---
description: El método TimerCallback es un método de devolución de llamada para el evento de temporizador de final de secuencia.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661265"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="5c81a-103">CBaseRenderer. TimerCallback, método</span><span class="sxs-lookup"><span data-stu-id="5c81a-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="5c81a-104">El `TimerCallback` método es un método de devolución de llamada para el evento de temporizador de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5c81a-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c81a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c81a-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="5c81a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c81a-106">Parameters</span></span>

<span data-ttu-id="5c81a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5c81a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c81a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c81a-108">Return value</span></span>

<span data-ttu-id="5c81a-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5c81a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c81a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c81a-110">Remarks</span></span>

<span data-ttu-id="5c81a-111">El método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa un evento de temporizador para programar \_ notificaciones completas de EC.</span><span class="sxs-lookup"><span data-stu-id="5c81a-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="5c81a-112">El método **CBaseRenderer:: TimerCallback** es la función de devolución de llamada para el evento del temporizador.</span><span class="sxs-lookup"><span data-stu-id="5c81a-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="5c81a-113">El `TimerCallback` método llama a **SendEndOfStream** de nuevo y **SendEndOfStream** determina si se debe enviar la notificación de finalización de EC \_ o establecer otro temporizador.</span><span class="sxs-lookup"><span data-stu-id="5c81a-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="5c81a-114">El método [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela el evento del temporizador.</span><span class="sxs-lookup"><span data-stu-id="5c81a-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c81a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c81a-115">Requirements</span></span>



| <span data-ttu-id="5c81a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c81a-116">Requirement</span></span> | <span data-ttu-id="5c81a-117">Value</span><span class="sxs-lookup"><span data-stu-id="5c81a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c81a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c81a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5c81a-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c81a-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c81a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c81a-120">Library</span></span><br/> | <dl> <span data-ttu-id="5c81a-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5c81a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c81a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c81a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c81a-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5c81a-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




