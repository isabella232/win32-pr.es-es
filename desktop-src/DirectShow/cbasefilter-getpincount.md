---
description: El método GetPinCount recupera el número de clavijas.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Método CBaseFilter. GetPinCount (Amfilter. h)
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661089"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="ee81b-103">CBaseFilter. GetPinCount, método</span><span class="sxs-lookup"><span data-stu-id="ee81b-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="ee81b-104">El `GetPinCount` método recupera el número de clavijas.</span><span class="sxs-lookup"><span data-stu-id="ee81b-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee81b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee81b-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="ee81b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee81b-106">Parameters</span></span>

<span data-ttu-id="ee81b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee81b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee81b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee81b-108">Return value</span></span>

<span data-ttu-id="ee81b-109">Devuelve el número de clavijas.</span><span class="sxs-lookup"><span data-stu-id="ee81b-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee81b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee81b-110">Remarks</span></span>

<span data-ttu-id="ee81b-111">La clase derivada debe implementar este método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="ee81b-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="ee81b-112">Devuelve el número de clavijas que están disponibles actualmente en este filtro.</span><span class="sxs-lookup"><span data-stu-id="ee81b-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="ee81b-113">Los filtros pueden crear o destruir PIN dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ee81b-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee81b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee81b-114">Requirements</span></span>



| <span data-ttu-id="ee81b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee81b-115">Requirement</span></span> | <span data-ttu-id="ee81b-116">Value</span><span class="sxs-lookup"><span data-stu-id="ee81b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee81b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee81b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ee81b-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee81b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee81b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee81b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ee81b-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ee81b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee81b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee81b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee81b-122">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ee81b-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




