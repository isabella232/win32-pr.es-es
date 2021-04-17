---
description: El método CompleteStateChange determina si se ha completado una transición al estado en pausa.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671073"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="9d2fd-103">CBaseRenderer. CompleteStateChange, método</span><span class="sxs-lookup"><span data-stu-id="9d2fd-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="9d2fd-104">El `CompleteStateChange` método determina si se ha completado una transición al estado en pausa.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d2fd-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="9d2fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d2fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d2fd-107">*OldState*</span><span class="sxs-lookup"><span data-stu-id="9d2fd-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="9d2fd-108">Estado anterior a la transición.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d2fd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d2fd-109">Return value</span></span>

<span data-ttu-id="9d2fd-110">Devuelve S \_ OK si la transición se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="9d2fd-111">De lo contrario, devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d2fd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d2fd-112">Remarks</span></span>

<span data-ttu-id="9d2fd-113">El método [**CBaseRenderer::P ause**](cbaserenderer-pause.md) llama a este método para actualizar el estado de la transición de estado.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="9d2fd-114">En general, la transición a pausado no finaliza hasta que el filtro recibe un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="9d2fd-115">Sin embargo, en algunas situaciones la transición se completa inmediatamente: por ejemplo, si el filtro está desconectado o si se alcanzó el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="9d2fd-116">Este método comprueba los distintos criterios y, a continuación, llama al método [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) o al método [**CBaseRenderer::**](cbaserenderer-notready.md) para actualizar el estado de la transición.</span><span class="sxs-lookup"><span data-stu-id="9d2fd-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d2fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d2fd-117">Requirements</span></span>



| <span data-ttu-id="9d2fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d2fd-118">Requirement</span></span> | <span data-ttu-id="9d2fd-119">Value</span><span class="sxs-lookup"><span data-stu-id="9d2fd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d2fd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d2fd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9d2fd-121"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d2fd-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d2fd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d2fd-122">Library</span></span><br/> | <dl> <span data-ttu-id="9d2fd-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d2fd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d2fd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d2fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2fd-125">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="9d2fd-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




