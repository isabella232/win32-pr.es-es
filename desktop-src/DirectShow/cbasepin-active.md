---
description: El método activo notifica al pin que el filtro está activo ahora.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661009"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="44e6e-103">CBasePin. Active (método)</span><span class="sxs-lookup"><span data-stu-id="44e6e-103">CBasePin.Active method</span></span>

<span data-ttu-id="44e6e-104">El `Active` método notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="44e6e-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44e6e-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="44e6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44e6e-106">Parameters</span></span>

<span data-ttu-id="44e6e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="44e6e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44e6e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44e6e-108">Return value</span></span>

<span data-ttu-id="44e6e-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="44e6e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="44e6e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44e6e-110">Remarks</span></span>

<span data-ttu-id="44e6e-111">Cuando el filtro pasa de detenido a en pausa, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los pin conectados del filtro.</span><span class="sxs-lookup"><span data-stu-id="44e6e-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="44e6e-112">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="44e6e-112">This method does nothing in the base class.</span></span> <span data-ttu-id="44e6e-113">Las clases derivadas pueden invalidar este método; por ejemplo, un PIN podría confirmar asignadores u obtener recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="44e6e-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="44e6e-114">El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve esta función miembro, de modo que no se prueba el estado desde este método.</span><span class="sxs-lookup"><span data-stu-id="44e6e-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e6e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e6e-115">Requirements</span></span>



| <span data-ttu-id="44e6e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e6e-116">Requirement</span></span> | <span data-ttu-id="44e6e-117">Value</span><span class="sxs-lookup"><span data-stu-id="44e6e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e6e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44e6e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="44e6e-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44e6e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="44e6e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44e6e-120">Library</span></span><br/> | <dl> <span data-ttu-id="44e6e-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="44e6e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e6e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="44e6e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e6e-123">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="44e6e-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




