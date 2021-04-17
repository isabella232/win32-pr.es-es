---
description: El método StreamTime recupera la hora de la secuencia actual.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660186"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="76040-103">CBaseMediaFilter. StreamTime, método</span><span class="sxs-lookup"><span data-stu-id="76040-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="76040-104">El `StreamTime` método recupera la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="76040-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="76040-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76040-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="76040-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76040-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76040-107">*rtStream* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="76040-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="76040-108">Referencia a un objeto [**CRefTime**](creftime.md) que recibe la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="76040-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76040-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76040-109">Return value</span></span>

<span data-ttu-id="76040-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76040-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="76040-111">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="76040-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="76040-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="76040-112">Return code</span></span>                                                                                      | <span data-ttu-id="76040-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="76040-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="76040-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="76040-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="76040-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="76040-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="76040-116"><dt>**VFW \_ E \_ sin \_ reloj**</dt></span><span class="sxs-lookup"><span data-stu-id="76040-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="76040-117">No hay ningún reloj de referencia disponible.</span><span class="sxs-lookup"><span data-stu-id="76040-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76040-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76040-118">Remarks</span></span>

<span data-ttu-id="76040-119">La hora de la secuencia se define como la hora de referencia actual (indicada por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseMediaFilter:: m \_ tStart**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="76040-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="76040-120">La marca de tiempo de un ejemplo multimedia especifica el tiempo de flujo en el que se debe representar.</span><span class="sxs-lookup"><span data-stu-id="76040-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="76040-121">Si aún no se ha representado una muestra con una marca de tiempo menor que la hora actual de la secuencia, se retrasa.</span><span class="sxs-lookup"><span data-stu-id="76040-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="76040-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76040-122">Requirements</span></span>



| <span data-ttu-id="76040-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="76040-123">Requirement</span></span> | <span data-ttu-id="76040-124">Value</span><span class="sxs-lookup"><span data-stu-id="76040-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76040-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76040-125">Header</span></span><br/>  | <dl> <span data-ttu-id="76040-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76040-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="76040-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76040-127">Library</span></span><br/> | <dl> <span data-ttu-id="76040-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="76040-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76040-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="76040-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76040-130">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="76040-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




