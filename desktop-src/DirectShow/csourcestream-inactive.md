---
description: 'El método Inactive notifica al pin que el filtro ya no está activo. Este método invalida el método CBasePin:: INACTIVE. Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Método CSourceStream. Inactive (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690418"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="a3a8e-105">CSourceStream. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="a3a8e-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="a3a8e-106">El `Inactive` método notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="a3a8e-107">Este método invalida el método [**CBasePin:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a8e-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="a3a8e-108">Si el subproceso de streaming está activo, este método lo detiene y espera a que se cierre el subproceso.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a8e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3a8e-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="a3a8e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3a8e-110">Parameters</span></span>

<span data-ttu-id="a3a8e-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3a8e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3a8e-112">Return value</span></span>

<span data-ttu-id="a3a8e-113">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3a8e-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a8e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a8e-114">Requirements</span></span>



| <span data-ttu-id="a3a8e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a8e-115">Requirement</span></span> | <span data-ttu-id="a3a8e-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3a8e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a8e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3a8e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3a8e-118"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8e-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a3a8e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3a8e-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3a8e-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3a8e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3a8e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3a8e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a8e-122">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="a3a8e-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




