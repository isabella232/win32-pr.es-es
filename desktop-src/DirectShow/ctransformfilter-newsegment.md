---
description: El método NewSegment notifica al filtro que los ejemplos multimedia recibidos después de que esta llamada se agrupe como un segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Método CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661025"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="ff0f0-103">CTransformFilter. NewSegment, método</span><span class="sxs-lookup"><span data-stu-id="ff0f0-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="ff0f0-104">El `NewSegment` método notifica al filtro que los ejemplos multimedia recibidos después de que esta llamada se agrupe como un segmento.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff0f0-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="ff0f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff0f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0f0-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="ff0f0-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0f0-108">Hora de inicio del segmento, relativa al origen original.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="ff0f0-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="ff0f0-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0f0-110">Hora de detención del segmento, relativa al origen original.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="ff0f0-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="ff0f0-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ff0f0-112">Velocidad a la que se debe procesar el segmento.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0f0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff0f0-113">Return value</span></span>

<span data-ttu-id="ff0f0-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0f0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff0f0-115">Remarks</span></span>

<span data-ttu-id="ff0f0-116">El método [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) del PIN de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="ff0f0-117">Este método entrega la `NewSegment` llamada al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0f0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff0f0-118">Requirements</span></span>



| <span data-ttu-id="ff0f0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0f0-119">Requirement</span></span> | <span data-ttu-id="ff0f0-120">Value</span><span class="sxs-lookup"><span data-stu-id="ff0f0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0f0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff0f0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ff0f0-122"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff0f0-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff0f0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff0f0-123">Library</span></span><br/> | <dl> <span data-ttu-id="ff0f0-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ff0f0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0f0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff0f0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0f0-126">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="ff0f0-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




