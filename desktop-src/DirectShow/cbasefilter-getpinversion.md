---
description: El método GetPinVersion recupera un número de versión para el conjunto de PIN de este filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Método CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661085"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="e82c2-103">CBaseFilter. GetPinVersion, método</span><span class="sxs-lookup"><span data-stu-id="e82c2-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="e82c2-104">El `GetPinVersion` método recupera un número de versión para el conjunto de PIN de este filtro.</span><span class="sxs-lookup"><span data-stu-id="e82c2-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e82c2-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="e82c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e82c2-106">Parameters</span></span>

<span data-ttu-id="e82c2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e82c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e82c2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e82c2-108">Return value</span></span>

<span data-ttu-id="e82c2-109">Devuelve la variable miembro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="e82c2-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e82c2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e82c2-110">Remarks</span></span>

<span data-ttu-id="e82c2-111">El constructor **CBaseFilter** inicializa la versión del PIN en 1.</span><span class="sxs-lookup"><span data-stu-id="e82c2-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="e82c2-112">En la clase base, este número nunca cambia.</span><span class="sxs-lookup"><span data-stu-id="e82c2-112">In the base class, this number never changes.</span></span> <span data-ttu-id="e82c2-113">Si el filtro crea o destruye dinámicamente los pin, debe incrementar la versión del PIN cada vez que cambien los pin.</span><span class="sxs-lookup"><span data-stu-id="e82c2-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="e82c2-114">Para incrementar el número de versión, llame al método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="e82c2-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="e82c2-115">El objeto de enumerador de PIN, implementado por la clase [**CEnumPins**](cenumpins.md) , usa la versión del PIN para mantener la sincronización con el filtro.</span><span class="sxs-lookup"><span data-stu-id="e82c2-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e82c2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e82c2-116">Requirements</span></span>



| <span data-ttu-id="e82c2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e82c2-117">Requirement</span></span> | <span data-ttu-id="e82c2-118">Value</span><span class="sxs-lookup"><span data-stu-id="e82c2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e82c2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e82c2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e82c2-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e82c2-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e82c2-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e82c2-121">Library</span></span><br/> | <dl> <span data-ttu-id="e82c2-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e82c2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82c2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e82c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82c2-124">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e82c2-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




