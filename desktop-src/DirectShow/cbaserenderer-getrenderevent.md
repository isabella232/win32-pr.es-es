---
description: El método GetRenderEvent recupera el evento que programa la representación.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Método CBaseRenderer. GetRenderEvent (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670435"
---
# <a name="cbaserenderergetrenderevent-method"></a><span data-ttu-id="1aa2f-103">CBaseRenderer. GetRenderEvent, método</span><span class="sxs-lookup"><span data-stu-id="1aa2f-103">CBaseRenderer.GetRenderEvent method</span></span>

<span data-ttu-id="1aa2f-104">El `GetRenderEvent` método recupera el evento que programa la representación.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-104">The `GetRenderEvent` method retrieves the event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1aa2f-105">Syntax</span></span>


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a><span data-ttu-id="1aa2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1aa2f-106">Parameters</span></span>

<span data-ttu-id="1aa2f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1aa2f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aa2f-108">Return value</span></span>

<span data-ttu-id="1aa2f-109">Devuelve un puntero al evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa2f-109">Returns a pointer to the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa2f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aa2f-110">Requirements</span></span>



| <span data-ttu-id="1aa2f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa2f-111">Requirement</span></span> | <span data-ttu-id="1aa2f-112">Value</span><span class="sxs-lookup"><span data-stu-id="1aa2f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa2f-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1aa2f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1aa2f-114"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa2f-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1aa2f-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1aa2f-115">Library</span></span><br/> | <dl> <span data-ttu-id="1aa2f-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1aa2f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa2f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aa2f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa2f-118">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="1aa2f-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




