---
description: 'El método QueryAccept determina si el PIN acepta un tipo de medio especificado. Este método implementa el método IPin:: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Método CBasePin. QueryAccept (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671831"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="7a288-104">CBasePin. QueryAccept, método</span><span class="sxs-lookup"><span data-stu-id="7a288-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="7a288-105">El `QueryAccept` método determina si el PIN acepta un tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="7a288-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="7a288-106">Este método implementa el método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .</span><span class="sxs-lookup"><span data-stu-id="7a288-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a288-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a288-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7a288-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a288-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="7a288-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7a288-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="7a288-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a288-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a288-111">Return value</span></span>

<span data-ttu-id="7a288-112">Devuelve S \_ correcto si el tipo de medio es aceptable.</span><span class="sxs-lookup"><span data-stu-id="7a288-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="7a288-113">De lo contrario, devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="7a288-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a288-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a288-114">Remarks</span></span>

<span data-ttu-id="7a288-115">En la clase base, este método delega en el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="7a288-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="7a288-116">Si **CheckMediaType** produce un error, `QueryAccept` devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="7a288-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="7a288-117">Este método no contiene la sección crítica del PIN ([**CBasePin:: m \_ Plock**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="7a288-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="7a288-118">Si la clase derivada modifica dinámicamente el conjunto de tipos de medios aceptables, debe invalidar este método para que contenga la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="7a288-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a288-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a288-119">Requirements</span></span>



| <span data-ttu-id="7a288-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a288-120">Requirement</span></span> | <span data-ttu-id="7a288-121">Value</span><span class="sxs-lookup"><span data-stu-id="7a288-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a288-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a288-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7a288-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a288-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a288-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a288-124">Library</span></span><br/> | <dl> <span data-ttu-id="7a288-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7a288-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a288-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a288-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a288-127">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7a288-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




