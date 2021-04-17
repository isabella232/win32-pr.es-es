---
description: El método IncremementPinVersion incrementa el número de versión en el conjunto de PIN.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Método CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661080"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="a3acf-103">CBaseFilter. IncrementPinVersion, método</span><span class="sxs-lookup"><span data-stu-id="a3acf-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="a3acf-104">El `IncremementPinVersion` método incrementa el número de versión en el conjunto de PIN.</span><span class="sxs-lookup"><span data-stu-id="a3acf-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3acf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3acf-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="a3acf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3acf-106">Parameters</span></span>

<span data-ttu-id="a3acf-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a3acf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3acf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3acf-108">Return value</span></span>

<span data-ttu-id="a3acf-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a3acf-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3acf-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3acf-110">Remarks</span></span>

<span data-ttu-id="a3acf-111">Este método incrementa la variable miembro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="a3acf-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="a3acf-112">Si el filtro crea o destruye dinámicamente los pin, llame a este método cada vez que cambien los pin.</span><span class="sxs-lookup"><span data-stu-id="a3acf-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3acf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3acf-113">Requirements</span></span>



| <span data-ttu-id="a3acf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3acf-114">Requirement</span></span> | <span data-ttu-id="a3acf-115">Value</span><span class="sxs-lookup"><span data-stu-id="a3acf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3acf-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3acf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a3acf-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3acf-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3acf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3acf-118">Library</span></span><br/> | <dl> <span data-ttu-id="a3acf-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3acf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3acf-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3acf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3acf-121">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a3acf-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="a3acf-122">**CBaseFilter::GetPinVersion**</span><span class="sxs-lookup"><span data-stu-id="a3acf-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




