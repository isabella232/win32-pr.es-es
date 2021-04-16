---
description: El método ResetEndOfStream restablece las marcas de fin de secuencia.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Método CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671730"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="24cb8-103">CBaseRenderer. ResetEndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="24cb8-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="24cb8-104">El `ResetEndOfStream` método restablece las marcas de fin de secuencia.</span><span class="sxs-lookup"><span data-stu-id="24cb8-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="24cb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24cb8-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="24cb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24cb8-106">Parameters</span></span>

<span data-ttu-id="24cb8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="24cb8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24cb8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24cb8-108">Return value</span></span>

<span data-ttu-id="24cb8-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="24cb8-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="24cb8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24cb8-110">Remarks</span></span>

<span data-ttu-id="24cb8-111">Este método borra la condición de final de secuencia anterior.</span><span class="sxs-lookup"><span data-stu-id="24cb8-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="24cb8-112">En ese momento, el filtro puede recibir datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="24cb8-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="24cb8-113">Los métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) y [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) llaman a este método.</span><span class="sxs-lookup"><span data-stu-id="24cb8-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="24cb8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24cb8-114">Requirements</span></span>



| <span data-ttu-id="24cb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24cb8-115">Requirement</span></span> | <span data-ttu-id="24cb8-116">Value</span><span class="sxs-lookup"><span data-stu-id="24cb8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24cb8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24cb8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="24cb8-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24cb8-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24cb8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24cb8-119">Library</span></span><br/> | <dl> <span data-ttu-id="24cb8-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="24cb8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24cb8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="24cb8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24cb8-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="24cb8-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




