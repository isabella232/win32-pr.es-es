---
description: 'Método CBaseInputPin.Notify: el método Notify notifica al pin que se solicita un cambio de calidad. Este método implementa el método IQualityControl::Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin.Notify (Amfilter.h)
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
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120003"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="2f7c9-104">Método CBaseInputPin.Notify</span><span class="sxs-lookup"><span data-stu-id="2f7c9-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="2f7c9-105">El `Notify` método notifica al pin que se solicita un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="2f7c9-106">Este método implementa el [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="2f7c9-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7c9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f7c9-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="2f7c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f7c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7c9-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="2f7c9-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="2f7c9-110">Puntero al filtro que envía el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="2f7c9-111">*Q*</span><span class="sxs-lookup"><span data-stu-id="2f7c9-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="2f7c9-112">[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7c9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f7c9-113">Return value</span></span>

<span data-ttu-id="2f7c9-114">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7c9-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f7c9-115">Remarks</span></span>

<span data-ttu-id="2f7c9-116">Los filtros suelen pasar mensajes de control de calidad a un pin de salida ascendente, no a un pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="2f7c9-117">Por lo tanto, este método devuelve S \_ OK sin hacer nada.</span><span class="sxs-lookup"><span data-stu-id="2f7c9-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7c9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7c9-118">Requirements</span></span>



| <span data-ttu-id="2f7c9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7c9-119">Requirement</span></span> | <span data-ttu-id="2f7c9-120">Value</span><span class="sxs-lookup"><span data-stu-id="2f7c9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7c9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f7c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2f7c9-122"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f7c9-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f7c9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f7c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="2f7c9-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f7c9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7c9-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f7c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7c9-126">**CBaseInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="2f7c9-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="2f7c9-127">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="2f7c9-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




