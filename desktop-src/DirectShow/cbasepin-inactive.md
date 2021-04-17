---
description: El método Inactive notifica al pin que el filtro ya no está activo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671101"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="5da80-103">CBasePin. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="5da80-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="5da80-104">El `Inactive` método notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="5da80-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da80-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5da80-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="5da80-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5da80-106">Parameters</span></span>

<span data-ttu-id="5da80-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5da80-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5da80-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5da80-108">Return value</span></span>

<span data-ttu-id="5da80-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5da80-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5da80-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5da80-110">Remarks</span></span>

<span data-ttu-id="5da80-111">Cuando el filtro se detiene, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todas las clavijas conectadas del filtro.</span><span class="sxs-lookup"><span data-stu-id="5da80-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="5da80-112">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="5da80-112">This method does nothing in the base class.</span></span> <span data-ttu-id="5da80-113">Las clases derivadas deben invalidar este método para liberar los recursos obtenidos por el método [**CBasePin:: Active**](cbasepin-active.md) ; por ejemplo, para anular la confirmación de los asignadores del PIN.</span><span class="sxs-lookup"><span data-stu-id="5da80-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="5da80-114">El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve este método, por lo que no se prueba el estado desde este método.</span><span class="sxs-lookup"><span data-stu-id="5da80-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da80-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da80-115">Requirements</span></span>



| <span data-ttu-id="5da80-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da80-116">Requirement</span></span> | <span data-ttu-id="5da80-117">Value</span><span class="sxs-lookup"><span data-stu-id="5da80-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da80-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5da80-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5da80-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5da80-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5da80-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5da80-120">Library</span></span><br/> | <dl> <span data-ttu-id="5da80-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5da80-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da80-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5da80-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da80-123">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5da80-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




