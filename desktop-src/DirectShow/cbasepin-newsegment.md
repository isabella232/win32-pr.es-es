---
description: 'El método NewSegment notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento. Implementa el método IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660645"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="252cb-104">CBasePin. NewSegment, método</span><span class="sxs-lookup"><span data-stu-id="252cb-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="252cb-105">El `NewSegment` método notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento.</span><span class="sxs-lookup"><span data-stu-id="252cb-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="252cb-106">Implementa el método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="252cb-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="252cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="252cb-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="252cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="252cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="252cb-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="252cb-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="252cb-110">Posición del medio inicial del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="252cb-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="252cb-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="252cb-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="252cb-112">Fin de la posición del medio del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="252cb-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="252cb-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="252cb-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="252cb-114">Velocidad a la que se debe procesar este segmento, como porcentaje de la tasa original.</span><span class="sxs-lookup"><span data-stu-id="252cb-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="252cb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="252cb-115">Return value</span></span>

<span data-ttu-id="252cb-116">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="252cb-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="252cb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="252cb-117">Remarks</span></span>

<span data-ttu-id="252cb-118">Este método establece las variables de miembro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)y [**CBasePin:: m \_ dRate**](cbasepin-m-drate.md) .</span><span class="sxs-lookup"><span data-stu-id="252cb-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="252cb-119">En la clase derivada, Invalide este método para pasar la notificación de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="252cb-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="252cb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="252cb-120">Requirements</span></span>



| <span data-ttu-id="252cb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="252cb-121">Requirement</span></span> | <span data-ttu-id="252cb-122">Value</span><span class="sxs-lookup"><span data-stu-id="252cb-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="252cb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="252cb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="252cb-124"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="252cb-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="252cb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="252cb-125">Library</span></span><br/> | <dl> <span data-ttu-id="252cb-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="252cb-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252cb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="252cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252cb-128">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="252cb-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




