---
description: 'Método CBasePin.Inactive: el método Inactivo notifica al pin que el filtro ya no está activo.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin.Inactive (Amfilter.h)
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
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099343"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="0ac61-103">CBasePin.Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="0ac61-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="0ac61-104">El `Inactive` método notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="0ac61-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ac61-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="0ac61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ac61-106">Parameters</span></span>

<span data-ttu-id="0ac61-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0ac61-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ac61-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ac61-108">Return value</span></span>

<span data-ttu-id="0ac61-109">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ac61-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac61-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ac61-110">Remarks</span></span>

<span data-ttu-id="0ac61-111">Cuando se detiene el filtro, la [**clase CBaseFilter**](cbasefilter.md) llama a este método en todos los pines conectados del filtro.</span><span class="sxs-lookup"><span data-stu-id="0ac61-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="0ac61-112">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="0ac61-112">This method does nothing in the base class.</span></span> <span data-ttu-id="0ac61-113">Las clases derivadas deben invalidar este método para liberar los recursos obtenidos por el [**método CBasePin::Active;**](cbasepin-active.md) por ejemplo, para desasignar los asignadores del pin.</span><span class="sxs-lookup"><span data-stu-id="0ac61-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="0ac61-114">El estado interno del administrador de gráficos de filtro no se actualiza hasta después de que este método vuelva, por lo que no pruebe el estado de este método.</span><span class="sxs-lookup"><span data-stu-id="0ac61-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac61-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac61-115">Requirements</span></span>



| <span data-ttu-id="0ac61-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac61-116">Requirement</span></span> | <span data-ttu-id="0ac61-117">Value</span><span class="sxs-lookup"><span data-stu-id="0ac61-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac61-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ac61-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0ac61-119"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac61-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ac61-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ac61-120">Library</span></span><br/> | <dl> <span data-ttu-id="0ac61-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac61-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac61-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0ac61-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac61-123">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="0ac61-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




