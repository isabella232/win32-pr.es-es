---
description: El método GetMediaTypeVersion recupera un número de versión para el conjunto de tipos de medios preferidos.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin. GetMediaTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661383"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="daef3-103">CBasePin. GetMediaTypeVersion, método</span><span class="sxs-lookup"><span data-stu-id="daef3-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="daef3-104">El `GetMediaTypeVersion` método recupera un número de versión para el conjunto de tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="daef3-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="daef3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daef3-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="daef3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daef3-106">Parameters</span></span>

<span data-ttu-id="daef3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="daef3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="daef3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daef3-108">Return value</span></span>

<span data-ttu-id="daef3-109">Devuelve la variable miembro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="daef3-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="daef3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daef3-110">Remarks</span></span>

<span data-ttu-id="daef3-111">El constructor **CBasePin** inicializa el número de versión en 1.</span><span class="sxs-lookup"><span data-stu-id="daef3-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="daef3-112">En la clase base, este número nunca cambia.</span><span class="sxs-lookup"><span data-stu-id="daef3-112">In the base class, this number never changes.</span></span> <span data-ttu-id="daef3-113">Si el PIN cambia dinámicamente su lista de tipos de medios preferidos, debe incrementar el número de versión cada vez que cambie la lista.</span><span class="sxs-lookup"><span data-stu-id="daef3-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="daef3-114">Para incrementar el número de versión, llame al método [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="daef3-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="daef3-115">El enumerador de tipo de medio, que se implementa mediante la clase [**CEnumMediaTypes**](cenummediatypes.md) , usa el número de versión para mantenerlo sincronizado con el PIN.</span><span class="sxs-lookup"><span data-stu-id="daef3-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="daef3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daef3-116">Requirements</span></span>



| <span data-ttu-id="daef3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="daef3-117">Requirement</span></span> | <span data-ttu-id="daef3-118">Value</span><span class="sxs-lookup"><span data-stu-id="daef3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daef3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daef3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="daef3-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daef3-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="daef3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="daef3-121">Library</span></span><br/> | <dl> <span data-ttu-id="daef3-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="daef3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daef3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="daef3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daef3-124">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="daef3-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




