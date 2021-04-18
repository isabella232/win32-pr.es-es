---
description: El método GetSchedule recupera un puntero al objeto de programación del reloj.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Método CBaseReferenceClock. GetSchedule (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660402"
---
# <a name="cbasereferenceclockgetschedule-method"></a><span data-ttu-id="62cd9-103">CBaseReferenceClock. GetSchedule, método</span><span class="sxs-lookup"><span data-stu-id="62cd9-103">CBaseReferenceClock.GetSchedule method</span></span>

<span data-ttu-id="62cd9-104">El `GetSchedule` método recupera un puntero al objeto de programación del reloj.</span><span class="sxs-lookup"><span data-stu-id="62cd9-104">The `GetSchedule` method retrieves a pointer to the clock's scheduling object.</span></span>

## <a name="syntax"></a><span data-ttu-id="62cd9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62cd9-105">Syntax</span></span>


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a><span data-ttu-id="62cd9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62cd9-106">Parameters</span></span>

<span data-ttu-id="62cd9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="62cd9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62cd9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62cd9-108">Return value</span></span>

<span data-ttu-id="62cd9-109">Devuelve la variable miembro [**CBaseReferenceClock:: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="62cd9-109">Returns the [**CBaseReferenceClock::m\_pSchedule**](cbasereferenceclock-m-pschedule.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cd9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62cd9-110">Requirements</span></span>



| <span data-ttu-id="62cd9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="62cd9-111">Requirement</span></span> | <span data-ttu-id="62cd9-112">Value</span><span class="sxs-lookup"><span data-stu-id="62cd9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cd9-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62cd9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="62cd9-114"><dt>Refclock. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62cd9-114"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="62cd9-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62cd9-115">Library</span></span><br/> | <dl> <span data-ttu-id="62cd9-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62cd9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cd9-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="62cd9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cd9-118">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="62cd9-118">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




