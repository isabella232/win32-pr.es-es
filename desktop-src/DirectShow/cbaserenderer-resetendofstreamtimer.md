---
description: El método ResetEndOfStreamTimer cancela el temporizador que programa las \_ notificaciones completas de EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Método CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661323"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="47d66-103">CBaseRenderer. ResetEndOfStreamTimer, método</span><span class="sxs-lookup"><span data-stu-id="47d66-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="47d66-104">El `ResetEndOfStreamTimer` método cancela el temporizador que programa las notificaciones [**\_ completas de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="47d66-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47d66-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="47d66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47d66-106">Parameters</span></span>

<span data-ttu-id="47d66-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="47d66-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47d66-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47d66-108">Return value</span></span>

<span data-ttu-id="47d66-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="47d66-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d66-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d66-110">Requirements</span></span>



| <span data-ttu-id="47d66-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d66-111">Requirement</span></span> | <span data-ttu-id="47d66-112">Value</span><span class="sxs-lookup"><span data-stu-id="47d66-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d66-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47d66-113">Header</span></span><br/>  | <dl> <span data-ttu-id="47d66-114"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47d66-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47d66-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47d66-115">Library</span></span><br/> | <dl> <span data-ttu-id="47d66-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="47d66-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d66-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="47d66-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d66-118">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="47d66-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="47d66-119">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="47d66-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="47d66-120">**CBaseRenderer:: TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="47d66-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




