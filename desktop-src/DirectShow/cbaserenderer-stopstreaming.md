---
description: El método StopStreaming detiene la transmisión por secuencias cuando el filtro sale del estado de ejecución.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Método CBaseRenderer. StopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671669"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="3bf8a-103">CBaseRenderer. StopStreaming, método</span><span class="sxs-lookup"><span data-stu-id="3bf8a-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="3bf8a-104">El `StopStreaming` método detiene la transmisión por secuencias cuando el filtro sale del estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3bf8a-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bf8a-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="3bf8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bf8a-106">Parameters</span></span>

<span data-ttu-id="3bf8a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3bf8a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3bf8a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bf8a-108">Return value</span></span>

<span data-ttu-id="3bf8a-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="3bf8a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bf8a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bf8a-110">Remarks</span></span>

<span data-ttu-id="3bf8a-111">Este método llama al método [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="3bf8a-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="3bf8a-112">Ese método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="3bf8a-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf8a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bf8a-113">Requirements</span></span>



| <span data-ttu-id="3bf8a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bf8a-114">Requirement</span></span> | <span data-ttu-id="3bf8a-115">Value</span><span class="sxs-lookup"><span data-stu-id="3bf8a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf8a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bf8a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3bf8a-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bf8a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3bf8a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bf8a-118">Library</span></span><br/> | <dl> <span data-ttu-id="3bf8a-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3bf8a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bf8a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bf8a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf8a-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3bf8a-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




