---
description: El método DeliverNewSegment entrega una notificación de nuevo segmento al pin de entrada conectado.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Método CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671505"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="bdba3-103">CBaseOutputPin. DeliverNewSegment, método</span><span class="sxs-lookup"><span data-stu-id="bdba3-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="bdba3-104">El `DeliverNewSegment` método entrega una notificación de nuevo segmento al pin de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="bdba3-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdba3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdba3-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="bdba3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdba3-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="bdba3-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bdba3-108">Posición del medio inicial del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="bdba3-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="bdba3-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="bdba3-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="bdba3-110">Fin de la posición del medio del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="bdba3-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="bdba3-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="bdba3-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="bdba3-112">Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.</span><span class="sxs-lookup"><span data-stu-id="bdba3-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdba3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdba3-113">Return value</span></span>

<span data-ttu-id="bdba3-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdba3-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bdba3-115">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bdba3-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="bdba3-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bdba3-116">Return code</span></span>                                                                                           | <span data-ttu-id="bdba3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdba3-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bdba3-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bdba3-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bdba3-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bdba3-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="bdba3-120"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="bdba3-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bdba3-121">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="bdba3-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdba3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdba3-122">Remarks</span></span>

<span data-ttu-id="bdba3-123">Este método llama al método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdba3-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdba3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdba3-124">Requirements</span></span>



| <span data-ttu-id="bdba3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdba3-125">Requirement</span></span> | <span data-ttu-id="bdba3-126">Value</span><span class="sxs-lookup"><span data-stu-id="bdba3-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdba3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdba3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bdba3-128"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdba3-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdba3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdba3-129">Library</span></span><br/> | <dl> <span data-ttu-id="bdba3-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bdba3-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdba3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdba3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdba3-132">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bdba3-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




