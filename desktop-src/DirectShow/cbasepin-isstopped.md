---
description: El método IsStopped determina si el filtro que contiene este pin está detenido.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Método CBasePin. IsStopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661254"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="a2aa4-103">CBasePin. IsStopped, método</span><span class="sxs-lookup"><span data-stu-id="a2aa4-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="a2aa4-104">El `IsStopped` método determina si el filtro que contiene este pin está detenido.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2aa4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2aa4-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="a2aa4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2aa4-106">Parameters</span></span>

<span data-ttu-id="a2aa4-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2aa4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2aa4-108">Return value</span></span>

<span data-ttu-id="a2aa4-109">Devuelve **true** si el filtro está detenido.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="a2aa4-110">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2aa4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2aa4-111">Remarks</span></span>

<span data-ttu-id="a2aa4-112">No llame a este método desde dentro del método de constructor **CBasePin** , porque el filtro podría no haberse inicializado todavía.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2aa4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2aa4-113">Requirements</span></span>



| <span data-ttu-id="a2aa4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2aa4-114">Requirement</span></span> | <span data-ttu-id="a2aa4-115">Value</span><span class="sxs-lookup"><span data-stu-id="a2aa4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2aa4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2aa4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a2aa4-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2aa4-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2aa4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2aa4-118">Library</span></span><br/> | <dl> <span data-ttu-id="a2aa4-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a2aa4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2aa4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2aa4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2aa4-121">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="a2aa4-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




