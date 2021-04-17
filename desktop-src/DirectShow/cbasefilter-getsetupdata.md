---
description: El método GetSetupData recupera los datos de registro para el filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Método CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661084"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="10d61-103">CBaseFilter. GetSetupData, método</span><span class="sxs-lookup"><span data-stu-id="10d61-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="10d61-104">El `GetSetupData` método recupera los datos de registro para el filtro.</span><span class="sxs-lookup"><span data-stu-id="10d61-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="10d61-105">Este método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="10d61-105">This method is obsolete.</span></span> <span data-ttu-id="10d61-106">Lo llaman los métodos [**CBaseFilter:: Register**](cbasefilter-register.md) y [**CBaseFilter:: unregister**](cbasefilter-unregister.md) .</span><span class="sxs-lookup"><span data-stu-id="10d61-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="10d61-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10d61-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="10d61-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10d61-108">Parameters</span></span>

<span data-ttu-id="10d61-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="10d61-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10d61-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10d61-110">Return value</span></span>

<span data-ttu-id="10d61-111">Devuelve un puntero a una estructura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) que contiene información de registro para el filtro.</span><span class="sxs-lookup"><span data-stu-id="10d61-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d61-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10d61-112">Remarks</span></span>

<span data-ttu-id="10d61-113">La clase base devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="10d61-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d61-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10d61-114">Requirements</span></span>



| <span data-ttu-id="10d61-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d61-115">Requirement</span></span> | <span data-ttu-id="10d61-116">Value</span><span class="sxs-lookup"><span data-stu-id="10d61-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d61-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10d61-117">Header</span></span><br/>  | <dl> <span data-ttu-id="10d61-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10d61-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="10d61-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10d61-119">Library</span></span><br/> | <dl> <span data-ttu-id="10d61-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="10d61-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d61-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="10d61-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d61-122">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="10d61-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




