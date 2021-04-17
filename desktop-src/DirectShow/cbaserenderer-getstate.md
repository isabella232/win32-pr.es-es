---
description: El método GetState recupera el estado de los filtros (en ejecución, detenido o en pausa).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Método CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670608"
---
# <a name="cbaserenderergetstate-method"></a><span data-ttu-id="87f81-103">CBaseRenderer. GetState, método</span><span class="sxs-lookup"><span data-stu-id="87f81-103">CBaseRenderer.GetState method</span></span>

<span data-ttu-id="87f81-104">El `GetState` método recupera el estado del filtro (en ejecución, detenido o en pausa).</span><span class="sxs-lookup"><span data-stu-id="87f81-104">The `GetState` method retrieves the filters's state (running, stopped, or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="87f81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87f81-105">Syntax</span></span>


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a><span data-ttu-id="87f81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87f81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f81-107">*dwMilliSecsTimeout*</span><span class="sxs-lookup"><span data-stu-id="87f81-107">*dwMilliSecsTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="87f81-108">Intervalo de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="87f81-108">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="87f81-109">*State*</span><span class="sxs-lookup"><span data-stu-id="87f81-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="87f81-110">Puntero a una variable que recibe un miembro del tipo enumerado de [**\_ Estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , que indica el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="87f81-110">Pointer to a variable that receives a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type, indicating the filter's state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f81-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87f81-111">Return value</span></span>

<span data-ttu-id="87f81-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="87f81-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="87f81-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="87f81-113">Return code</span></span>                                                                                                | <span data-ttu-id="87f81-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="87f81-114">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="87f81-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="87f81-115"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="87f81-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="87f81-116">Success.</span></span><br/>                                            |
| <dl> <span data-ttu-id="87f81-117"><dt>**Estado de VFW \_ S \_ \_ intermedio**</dt></span><span class="sxs-lookup"><span data-stu-id="87f81-117"><dt>**VFW\_S\_STATE\_INTERMEDIATE**</dt></span></span> </dl> | <span data-ttu-id="87f81-118">El filtro está pasando al estado indicado.</span><span class="sxs-lookup"><span data-stu-id="87f81-118">The filter is transitioning to the indicated state.</span></span><br/> |
| <dl> <span data-ttu-id="87f81-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="87f81-119"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="87f81-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="87f81-120">**NULL** pointer argument.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="87f81-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87f81-121">Remarks</span></span>

<span data-ttu-id="87f81-122">Este método invalida el método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="87f81-122">This method overrides the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method.</span></span> <span data-ttu-id="87f81-123">Cuando el representador está en pausa, no completa la transición de estado hasta que recibe un ejemplo para representarlo.</span><span class="sxs-lookup"><span data-stu-id="87f81-123">When the renderer is paused, it does not complete the state transition until it receives a sample to render.</span></span> <span data-ttu-id="87f81-124">Si el tiempo de espera expira antes de que se complete la transición de estado, el método devuelve VFW \_ S \_ State \_ Intermediate.</span><span class="sxs-lookup"><span data-stu-id="87f81-124">If the time-out expires before the state transition is complete, the method returns VFW\_S\_STATE\_INTERMEDIATE.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f81-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87f81-125">Requirements</span></span>



| <span data-ttu-id="87f81-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f81-126">Requirement</span></span> | <span data-ttu-id="87f81-127">Value</span><span class="sxs-lookup"><span data-stu-id="87f81-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f81-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87f81-128">Header</span></span><br/>  | <dl> <span data-ttu-id="87f81-129"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87f81-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87f81-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87f81-130">Library</span></span><br/> | <dl> <span data-ttu-id="87f81-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="87f81-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f81-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="87f81-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f81-133">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="87f81-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




