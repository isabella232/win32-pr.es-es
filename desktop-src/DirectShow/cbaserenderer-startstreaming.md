---
description: El método StartStreaming inicia el streaming cuando el filtro cambia a un estado de ejecución.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Método CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671670"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="392e3-103">CBaseRenderer. StartStreaming, método</span><span class="sxs-lookup"><span data-stu-id="392e3-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="392e3-104">El `StartStreaming` método inicia la transmisión por secuencias cuando el filtro cambia a un estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="392e3-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="392e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="392e3-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="392e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="392e3-106">Parameters</span></span>

<span data-ttu-id="392e3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="392e3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="392e3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="392e3-108">Return value</span></span>

<span data-ttu-id="392e3-109">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="392e3-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="392e3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="392e3-110">Remarks</span></span>

<span data-ttu-id="392e3-111">Si el filtro tiene un ejemplo, programa el ejemplo para su representación.</span><span class="sxs-lookup"><span data-stu-id="392e3-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="392e3-112">De lo contrario, si hay una notificación de final de secuencia pendiente, el filtro envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="392e3-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="392e3-113">Este método llama al método [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="392e3-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="392e3-114">Ese método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="392e3-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="392e3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="392e3-115">Requirements</span></span>



| <span data-ttu-id="392e3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="392e3-116">Requirement</span></span> | <span data-ttu-id="392e3-117">Value</span><span class="sxs-lookup"><span data-stu-id="392e3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392e3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="392e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="392e3-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="392e3-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="392e3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="392e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="392e3-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="392e3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="392e3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="392e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392e3-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="392e3-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




