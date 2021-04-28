---
description: 'Método CBasePin.Active: el método Active notifica al pin que el filtro ahora está activo.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin.Active (Amfilter.h)
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
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096113"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="140eb-103">Método CBasePin.Active</span><span class="sxs-lookup"><span data-stu-id="140eb-103">CBasePin.Active method</span></span>

<span data-ttu-id="140eb-104">El `Active` método notifica al pin que el filtro ahora está activo.</span><span class="sxs-lookup"><span data-stu-id="140eb-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="140eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="140eb-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="140eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="140eb-106">Parameters</span></span>

<span data-ttu-id="140eb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="140eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="140eb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="140eb-108">Return value</span></span>

<span data-ttu-id="140eb-109">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="140eb-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="140eb-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="140eb-110">Remarks</span></span>

<span data-ttu-id="140eb-111">Cuando el filtro pasa de detenido a en pausa, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los pines conectados del filtro.</span><span class="sxs-lookup"><span data-stu-id="140eb-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="140eb-112">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="140eb-112">This method does nothing in the base class.</span></span> <span data-ttu-id="140eb-113">Las clases derivadas pueden invalidar este método; Por ejemplo, un pin podría confirmar asignadores u obtener recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="140eb-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="140eb-114">El estado interno del administrador de gráficos de filtro no se actualiza hasta después de que se devuelva esta función miembro, por lo que no pruebe el estado desde este método.</span><span class="sxs-lookup"><span data-stu-id="140eb-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="140eb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140eb-115">Requirements</span></span>



| <span data-ttu-id="140eb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="140eb-116">Requirement</span></span> | <span data-ttu-id="140eb-117">Value</span><span class="sxs-lookup"><span data-stu-id="140eb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140eb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="140eb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="140eb-119"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="140eb-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="140eb-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="140eb-120">Library</span></span><br/> | <dl> <span data-ttu-id="140eb-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="140eb-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140eb-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="140eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140eb-123">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="140eb-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




