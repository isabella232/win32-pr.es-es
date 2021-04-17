---
description: El método ResetStreamingTimes restablece todas las horas que controlan el streaming.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Método CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660242"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="8c5b8-103">CBaseVideoRenderer. ResetStreamingTimes, método</span><span class="sxs-lookup"><span data-stu-id="8c5b8-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="8c5b8-104">El `ResetStreamingTimes` método restablece todo el tiempo que controla la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="8c5b8-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c5b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c5b8-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="8c5b8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c5b8-106">Parameters</span></span>

<span data-ttu-id="8c5b8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c5b8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c5b8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c5b8-108">Return value</span></span>

<span data-ttu-id="8c5b8-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c5b8-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c5b8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c5b8-110">Remarks</span></span>

<span data-ttu-id="8c5b8-111">Las horas se establecen para que los marcos no se quiten inicialmente y para que se dibuje el primer fotograma.</span><span class="sxs-lookup"><span data-stu-id="8c5b8-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5b8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c5b8-112">Requirements</span></span>



| <span data-ttu-id="8c5b8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c5b8-113">Requirement</span></span> | <span data-ttu-id="8c5b8-114">Value</span><span class="sxs-lookup"><span data-stu-id="8c5b8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5b8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c5b8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8c5b8-116"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5b8-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c5b8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c5b8-117">Library</span></span><br/> | <dl> <span data-ttu-id="8c5b8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5b8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c5b8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c5b8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5b8-120">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="8c5b8-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




