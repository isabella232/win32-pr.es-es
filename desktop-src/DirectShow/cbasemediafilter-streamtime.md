---
description: 'Método CBaseMediaFilter.StreamTime: el método StreamTime recupera el tiempo de secuencia actual.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter.StreamTime (Amfilter.h)
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
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096253"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="2587c-103">Método CBaseMediaFilter.StreamTime</span><span class="sxs-lookup"><span data-stu-id="2587c-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="2587c-104">El `StreamTime` método recupera el tiempo de secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="2587c-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2587c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2587c-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="2587c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2587c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2587c-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="2587c-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2587c-108">Referencia a un [**objeto CRefTime**](creftime.md) que recibe el tiempo de secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="2587c-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2587c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2587c-109">Return value</span></span>

<span data-ttu-id="2587c-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="2587c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2587c-111">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2587c-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2587c-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2587c-112">Return code</span></span>                                                                                      | <span data-ttu-id="2587c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2587c-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="2587c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2587c-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="2587c-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2587c-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="2587c-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="2587c-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="2587c-117">No hay ningún reloj de referencia disponible.</span><span class="sxs-lookup"><span data-stu-id="2587c-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2587c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2587c-118">Remarks</span></span>

<span data-ttu-id="2587c-119">La hora de la secuencia se define como la hora de referencia actual (según lo indicado por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseMediaFilter::m \_ tStart).**](cbasemediafilter-m-tstart.md)</span><span class="sxs-lookup"><span data-stu-id="2587c-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="2587c-120">La marca de tiempo de un ejemplo multimedia especifica el tiempo de secuencia en el que se debe representar.</span><span class="sxs-lookup"><span data-stu-id="2587c-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="2587c-121">Si aún no se ha representado un ejemplo con una marca de tiempo inferior a la hora de transmisión actual, es tarde.</span><span class="sxs-lookup"><span data-stu-id="2587c-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="2587c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2587c-122">Requirements</span></span>



| <span data-ttu-id="2587c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2587c-123">Requirement</span></span> | <span data-ttu-id="2587c-124">Value</span><span class="sxs-lookup"><span data-stu-id="2587c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2587c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2587c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2587c-126"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2587c-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2587c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2587c-127">Library</span></span><br/> | <dl> <span data-ttu-id="2587c-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2587c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2587c-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2587c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2587c-130">**CBaseMediaFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="2587c-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




