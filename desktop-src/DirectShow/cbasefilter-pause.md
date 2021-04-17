---
description: El método PAUSE pausa el filtro. Este método implementa el método IMediaFilter::P ause.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Método CBaseFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661168"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="ab2d2-104">CBaseFilter. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="ab2d2-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="ab2d2-105">El `Pause` método pausa el filtro.</span><span class="sxs-lookup"><span data-stu-id="ab2d2-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="ab2d2-106">Este método implementa el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="ab2d2-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab2d2-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="ab2d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab2d2-108">Parameters</span></span>

<span data-ttu-id="ab2d2-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab2d2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab2d2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab2d2-110">Return value</span></span>

<span data-ttu-id="ab2d2-111">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="ab2d2-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab2d2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab2d2-112">Remarks</span></span>

<span data-ttu-id="ab2d2-113">Este método llama al método [**CBasePin:: Active**](cbasepin-active.md) en cada una de las clavijas conectadas del filtro.</span><span class="sxs-lookup"><span data-stu-id="ab2d2-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab2d2-114">Requirements</span></span>



| <span data-ttu-id="ab2d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2d2-115">Requirement</span></span> | <span data-ttu-id="ab2d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="ab2d2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2d2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab2d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab2d2-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2d2-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab2d2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab2d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab2d2-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2d2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2d2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab2d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2d2-122">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ab2d2-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




