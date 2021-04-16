---
description: El método OnStopStreaming se llama al final del streaming para corregir los tiempos del informe de la página de propiedades.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Método CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679103"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="d3f48-103">CBaseVideoRenderer. OnStopStreaming, método</span><span class="sxs-lookup"><span data-stu-id="d3f48-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="d3f48-104">`OnStopStreaming`Se llama al método al final del streaming para corregir los tiempos del informe de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d3f48-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f48-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3f48-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="d3f48-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3f48-106">Parameters</span></span>

<span data-ttu-id="d3f48-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3f48-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3f48-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3f48-108">Return value</span></span>

<span data-ttu-id="d3f48-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3f48-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f48-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3f48-110">Remarks</span></span>

<span data-ttu-id="d3f48-111">Se llama a esta función miembro dos veces, una vez al pausar y de nuevo cuando la secuencia se detiene realmente.</span><span class="sxs-lookup"><span data-stu-id="d3f48-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="d3f48-112">Esta función miembro invalida [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="d3f48-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f48-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f48-113">Requirements</span></span>



| <span data-ttu-id="d3f48-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f48-114">Requirement</span></span> | <span data-ttu-id="d3f48-115">Value</span><span class="sxs-lookup"><span data-stu-id="d3f48-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f48-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3f48-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d3f48-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f48-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3f48-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3f48-118">Library</span></span><br/> | <dl> <span data-ttu-id="d3f48-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f48-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f48-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3f48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f48-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="d3f48-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




