---
description: 'El método GetPin recupera un PIN. Este método implementa el método CBaseFilter:: GetPin virtual puro.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource. GetPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670705"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="bd498-104">CSource. GetPin, método</span><span class="sxs-lookup"><span data-stu-id="bd498-104">CSource.GetPin method</span></span>

<span data-ttu-id="bd498-105">El `GetPin` método recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="bd498-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="bd498-106">Este método implementa el método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="bd498-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd498-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd498-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="bd498-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd498-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd498-109">*n*</span><span class="sxs-lookup"><span data-stu-id="bd498-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="bd498-110">Número del PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="bd498-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd498-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd498-111">Return value</span></span>

<span data-ttu-id="bd498-112">Devuelve el puntero al objeto [**CBasePin**](cbasepin.md) que implementa el PIN, o **null** si el índice está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="bd498-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd498-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd498-113">Requirements</span></span>



| <span data-ttu-id="bd498-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd498-114">Requirement</span></span> | <span data-ttu-id="bd498-115">Value</span><span class="sxs-lookup"><span data-stu-id="bd498-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd498-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd498-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bd498-117"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd498-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bd498-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd498-118">Library</span></span><br/> | <dl> <span data-ttu-id="bd498-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bd498-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd498-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd498-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd498-121">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="bd498-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




