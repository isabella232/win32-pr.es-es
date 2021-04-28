---
description: 'Método CBasePin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099443"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="ca27e-103">Método CBasePin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="ca27e-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="ca27e-104">El `BreakConnect` método libera el pin de una conexión.</span><span class="sxs-lookup"><span data-stu-id="ca27e-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca27e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca27e-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="ca27e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca27e-106">Parameters</span></span>

<span data-ttu-id="ca27e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ca27e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca27e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca27e-108">Return value</span></span>

<span data-ttu-id="ca27e-109">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca27e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca27e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca27e-110">Remarks</span></span>

<span data-ttu-id="ca27e-111">El método [**CBasePin::D isconnect**](cbasepin-disconnect.md) llama a este método durante la desconexión del pin.</span><span class="sxs-lookup"><span data-stu-id="ca27e-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="ca27e-112">También se llama durante un intento de conexión si se produce un error en el método [**CBasePin::CheckConnect.**](cbasepin-checkconnect.md)</span><span class="sxs-lookup"><span data-stu-id="ca27e-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="ca27e-113">Este método debe liberar los recursos obtenidos por el **método CheckConnect.**</span><span class="sxs-lookup"><span data-stu-id="ca27e-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="ca27e-114">Por ejemplo, si **CheckConnect** asigna memoria, `BreakConnect` debe liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="ca27e-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="ca27e-115">Si **CheckConnect** consulta el pin de conexión de una interfaz, `BreakConnect` debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="ca27e-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="ca27e-116">Tenga en `BreakConnect` cuenta que se puede llamar a sin una llamada correspondiente a **CompleteConnect.**</span><span class="sxs-lookup"><span data-stu-id="ca27e-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="ca27e-117">Por lo tanto, no puede suponer que se ha llamado a **CompleteConnect** anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ca27e-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca27e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca27e-118">Requirements</span></span>



| <span data-ttu-id="ca27e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca27e-119">Requirement</span></span> | <span data-ttu-id="ca27e-120">Value</span><span class="sxs-lookup"><span data-stu-id="ca27e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca27e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca27e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca27e-122"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca27e-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca27e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca27e-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca27e-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ca27e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca27e-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ca27e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca27e-126">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="ca27e-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




