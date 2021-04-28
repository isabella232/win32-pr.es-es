---
description: 'Método CBaseFilter.GetPinCount: el método GetPinCount recupera el número de pines.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Método CBaseFilter.GetPinCount (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099793"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="9ebc2-103">Método CBaseFilter.GetPinCount</span><span class="sxs-lookup"><span data-stu-id="9ebc2-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="9ebc2-104">El `GetPinCount` método recupera el número de pines.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebc2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ebc2-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="9ebc2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ebc2-106">Parameters</span></span>

<span data-ttu-id="9ebc2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ebc2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ebc2-108">Return value</span></span>

<span data-ttu-id="9ebc2-109">Devuelve el número de pines.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebc2-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ebc2-110">Remarks</span></span>

<span data-ttu-id="9ebc2-111">La clase derivada debe implementar este método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="9ebc2-112">Devuelve el número de pines que están disponibles actualmente en este filtro.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="9ebc2-113">Los filtros pueden crear o destruir de forma dinámica los pines.</span><span class="sxs-lookup"><span data-stu-id="9ebc2-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebc2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ebc2-114">Requirements</span></span>



| <span data-ttu-id="9ebc2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ebc2-115">Requirement</span></span> | <span data-ttu-id="9ebc2-116">Value</span><span class="sxs-lookup"><span data-stu-id="9ebc2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebc2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ebc2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9ebc2-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ebc2-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ebc2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ebc2-119">Library</span></span><br/> | <dl> <span data-ttu-id="9ebc2-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9ebc2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ebc2-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ebc2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebc2-122">**CBaseFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="9ebc2-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




