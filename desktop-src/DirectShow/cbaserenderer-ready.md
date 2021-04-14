---
description: El método Ready indica que se ha completado una transición de estado.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Método CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661328"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="eac26-103">CBaseRenderer. Ready (método)</span><span class="sxs-lookup"><span data-stu-id="eac26-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="eac26-104">El `Ready` método indica que se ha completado una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="eac26-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eac26-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="eac26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eac26-106">Parameters</span></span>

<span data-ttu-id="eac26-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="eac26-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eac26-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eac26-108">Return value</span></span>

<span data-ttu-id="eac26-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eac26-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac26-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eac26-110">Remarks</span></span>

<span data-ttu-id="eac26-111">Este método hace que el método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) devuelva S \_ correcto, lo que indica que el filtro ha completado la transición a su estado actual.</span><span class="sxs-lookup"><span data-stu-id="eac26-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="eac26-112">El filtro llama a este método cada vez que completa una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="eac26-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac26-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eac26-113">Requirements</span></span>



| <span data-ttu-id="eac26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac26-114">Requirement</span></span> | <span data-ttu-id="eac26-115">Value</span><span class="sxs-lookup"><span data-stu-id="eac26-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac26-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eac26-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eac26-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eac26-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eac26-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eac26-118">Library</span></span><br/> | <dl> <span data-ttu-id="eac26-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eac26-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac26-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="eac26-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac26-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="eac26-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="eac26-122">**CBaseRenderer::CheckReady**</span><span class="sxs-lookup"><span data-stu-id="eac26-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="eac26-123">**CBaseRenderer::**</span><span class="sxs-lookup"><span data-stu-id="eac26-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




