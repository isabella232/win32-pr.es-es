---
description: 'El método GetStopPosition recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. Este método implementa el método IMediaSeeking:: GetStopPosition.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Método CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690554"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="9c76c-104">CSourceSeeking. GetStopPosition, método</span><span class="sxs-lookup"><span data-stu-id="9c76c-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="9c76c-105">El `GetStopPosition` método recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9c76c-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="9c76c-106">Este método implementa el método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="9c76c-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c76c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c76c-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="9c76c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c76c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c76c-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="9c76c-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="9c76c-110">Puntero a una variable que recibe la hora de detención, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="9c76c-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c76c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c76c-111">Return value</span></span>

<span data-ttu-id="9c76c-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9c76c-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="9c76c-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c76c-113">Return code</span></span>                                                                               | <span data-ttu-id="9c76c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c76c-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="9c76c-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c76c-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9c76c-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="9c76c-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="9c76c-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9c76c-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="9c76c-118">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="9c76c-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c76c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c76c-119">Remarks</span></span>

<span data-ttu-id="9c76c-120">La hora de detención se especifica mediante la variable miembro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="9c76c-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c76c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c76c-121">Requirements</span></span>



| <span data-ttu-id="9c76c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c76c-122">Requirement</span></span> | <span data-ttu-id="9c76c-123">Value</span><span class="sxs-lookup"><span data-stu-id="9c76c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c76c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c76c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9c76c-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c76c-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9c76c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c76c-126">Library</span></span><br/> | <dl> <span data-ttu-id="9c76c-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9c76c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c76c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c76c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c76c-129">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="9c76c-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




