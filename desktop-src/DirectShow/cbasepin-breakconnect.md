---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671635"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="547d8-103">CBasePin. BreakConnect, método</span><span class="sxs-lookup"><span data-stu-id="547d8-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="547d8-104">El `BreakConnect` método libera el PIN de una conexión.</span><span class="sxs-lookup"><span data-stu-id="547d8-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="547d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="547d8-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="547d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="547d8-106">Parameters</span></span>

<span data-ttu-id="547d8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="547d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="547d8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="547d8-108">Return value</span></span>

<span data-ttu-id="547d8-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="547d8-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="547d8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="547d8-110">Remarks</span></span>

<span data-ttu-id="547d8-111">Se llama a este método durante la desconexión del PIN por el método [**CBasePin::D Ulta**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="547d8-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="547d8-112">También se llama durante un intento de conexión si se produce un error en el método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="547d8-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="547d8-113">Este método debe liberar los recursos obtenidos por el método **CheckConnect** .</span><span class="sxs-lookup"><span data-stu-id="547d8-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="547d8-114">Por ejemplo, si **CheckConnect** asigna memoria, `BreakConnect` debe liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="547d8-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="547d8-115">Si **CheckConnect** consulta el PIN de conexión de una interfaz, `BreakConnect` debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="547d8-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="547d8-116">Tenga en cuenta que `BreakConnect` se puede llamar a sin una llamada correspondiente a **CompleteConnect**.</span><span class="sxs-lookup"><span data-stu-id="547d8-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="547d8-117">Por lo tanto, no puede suponer que se ha llamado previamente a **CompleteConnect** .</span><span class="sxs-lookup"><span data-stu-id="547d8-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="547d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="547d8-118">Requirements</span></span>



| <span data-ttu-id="547d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="547d8-119">Requirement</span></span> | <span data-ttu-id="547d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="547d8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="547d8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="547d8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="547d8-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="547d8-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="547d8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="547d8-123">Library</span></span><br/> | <dl> <span data-ttu-id="547d8-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="547d8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="547d8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="547d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547d8-126">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="547d8-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




