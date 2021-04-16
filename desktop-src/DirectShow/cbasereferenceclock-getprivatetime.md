---
description: El método GetPrivateTime recupera la hora real del reloj.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Método CBaseReferenceClock. GetPrivateTime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671532"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="a539b-103">CBaseReferenceClock. GetPrivateTime, método</span><span class="sxs-lookup"><span data-stu-id="a539b-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="a539b-104">El `GetPrivateTime` método recupera la hora real del reloj.</span><span class="sxs-lookup"><span data-stu-id="a539b-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="a539b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a539b-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="a539b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a539b-106">Parameters</span></span>

<span data-ttu-id="a539b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a539b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a539b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a539b-108">Return value</span></span>

<span data-ttu-id="a539b-109">Devuelve la hora actual del reloj, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a539b-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="a539b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a539b-110">Remarks</span></span>

<span data-ttu-id="a539b-111">Este método devuelve el tiempo real indicado por el reloj.</span><span class="sxs-lookup"><span data-stu-id="a539b-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="a539b-112">Los autores de llamadas externos usan el método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) , que llama a este método.</span><span class="sxs-lookup"><span data-stu-id="a539b-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="a539b-113">A diferencia del método **getTime** , el reloj interno puede retroceder.</span><span class="sxs-lookup"><span data-stu-id="a539b-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="a539b-114">Si esto sucede, el método **getTime** continúa devolviendo la última vez que se informaba, hasta que el método se pone al día `GetPrivateTime` .</span><span class="sxs-lookup"><span data-stu-id="a539b-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="a539b-115">Este método devuelve la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="a539b-115">This method returns the system time.</span></span> <span data-ttu-id="a539b-116">Invalide este método si el reloj obtiene la hora de otro origen.</span><span class="sxs-lookup"><span data-stu-id="a539b-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="a539b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a539b-117">Requirements</span></span>



| <span data-ttu-id="a539b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a539b-118">Requirement</span></span> | <span data-ttu-id="a539b-119">Value</span><span class="sxs-lookup"><span data-stu-id="a539b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a539b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a539b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a539b-121"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a539b-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a539b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a539b-122">Library</span></span><br/> | <dl> <span data-ttu-id="a539b-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a539b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a539b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a539b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a539b-125">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="a539b-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




