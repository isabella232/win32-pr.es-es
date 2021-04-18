---
description: 'El método Notify notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método IQualityControl:: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671353"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="883cd-104">CBaseInputPin. Notify (método)</span><span class="sxs-lookup"><span data-stu-id="883cd-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="883cd-105">El `Notify` método notifica al pin que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="883cd-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="883cd-106">Este método implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="883cd-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="883cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="883cd-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="883cd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="883cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="883cd-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="883cd-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="883cd-110">Puntero al filtro que envía el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="883cd-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="883cd-111">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="883cd-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="883cd-112">Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="883cd-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="883cd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="883cd-113">Return value</span></span>

<span data-ttu-id="883cd-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="883cd-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="883cd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="883cd-115">Remarks</span></span>

<span data-ttu-id="883cd-116">Normalmente, los filtros pasan mensajes de control de calidad a un PIN de salida ascendente, no a un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="883cd-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="883cd-117">Por lo tanto, este método devuelve S \_ OK sin hacer nada.</span><span class="sxs-lookup"><span data-stu-id="883cd-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="883cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883cd-118">Requirements</span></span>



| <span data-ttu-id="883cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="883cd-119">Requirement</span></span> | <span data-ttu-id="883cd-120">Value</span><span class="sxs-lookup"><span data-stu-id="883cd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="883cd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="883cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="883cd-122"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="883cd-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="883cd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="883cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="883cd-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="883cd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883cd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="883cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883cd-126">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="883cd-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="883cd-127">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="883cd-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




