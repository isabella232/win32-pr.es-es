---
description: Se llama al método OnStopStreaming cuando el filtro detiene la transmisión por secuencias.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Método CBaseRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671738"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="e5773-103">CBaseRenderer. OnStopStreaming, método</span><span class="sxs-lookup"><span data-stu-id="e5773-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="e5773-104">`OnStopStreaming`Se llama al método cuando el filtro detiene la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="e5773-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5773-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5773-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="e5773-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5773-106">Parameters</span></span>

<span data-ttu-id="e5773-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e5773-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5773-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5773-108">Return value</span></span>

<span data-ttu-id="e5773-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e5773-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5773-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5773-110">Remarks</span></span>

<span data-ttu-id="e5773-111">El método [**CBaseRenderer:: StopStreaming**](cbaserenderer-stopstreaming.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="e5773-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="e5773-112">No realiza ninguna acción en la clase base, pero la clase derivada puede invalidarla.</span><span class="sxs-lookup"><span data-stu-id="e5773-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5773-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5773-113">Requirements</span></span>



| <span data-ttu-id="e5773-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5773-114">Requirement</span></span> | <span data-ttu-id="e5773-115">Value</span><span class="sxs-lookup"><span data-stu-id="e5773-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5773-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5773-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e5773-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5773-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5773-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5773-118">Library</span></span><br/> | <dl> <span data-ttu-id="e5773-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e5773-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5773-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5773-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5773-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e5773-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




