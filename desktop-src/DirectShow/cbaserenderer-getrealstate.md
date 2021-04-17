---
description: El método GetRealState recupera el estado del filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Método CBaseRenderer. GetRealState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660336"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="e1b8c-103">CBaseRenderer. GetRealState, método</span><span class="sxs-lookup"><span data-stu-id="e1b8c-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="e1b8c-104">El `GetRealState` método recupera el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="e1b8c-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1b8c-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="e1b8c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1b8c-106">Parameters</span></span>

<span data-ttu-id="e1b8c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e1b8c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1b8c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b8c-108">Return value</span></span>

<span data-ttu-id="e1b8c-109">Devuelve el valor de [**CBaseFilter:: m \_ State**](cbasefilter-m-state.md).</span><span class="sxs-lookup"><span data-stu-id="e1b8c-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="e1b8c-110">El valor es un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="e1b8c-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b8c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1b8c-111">Remarks</span></span>

<span data-ttu-id="e1b8c-112">Este método proporciona una alternativa más sencilla al método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e1b8c-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b8c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b8c-113">Requirements</span></span>



| <span data-ttu-id="e1b8c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b8c-114">Requirement</span></span> | <span data-ttu-id="e1b8c-115">Value</span><span class="sxs-lookup"><span data-stu-id="e1b8c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b8c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1b8c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e1b8c-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1b8c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1b8c-118">Library</span></span><br/> | <dl> <span data-ttu-id="e1b8c-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b8c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b8c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1b8c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b8c-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e1b8c-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




