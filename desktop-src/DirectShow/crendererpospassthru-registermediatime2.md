---
description: El método RegisterMediaTime almacena en caché las marcas de tiempo del ejemplo actual. Este método usa los parámetros *startTime* y *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: 'Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h): parámetros StartTime y EndTime'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187830"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="3ca5b-104">Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h): parámetros StartTime y EndTime</span><span class="sxs-lookup"><span data-stu-id="3ca5b-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="3ca5b-105">El método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) almacena en caché las marcas de tiempo del ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca5b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ca5b-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="3ca5b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ca5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca5b-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="3ca5b-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca5b-109">Hora de inicio de ejemplo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3ca5b-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="3ca5b-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca5b-111">Hora de finalización del ejemplo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca5b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ca5b-112">Return value</span></span>

<span data-ttu-id="3ca5b-113">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ca5b-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3ca5b-114">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3ca5b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3ca5b-115">Return code</span></span>                                                                          | <span data-ttu-id="3ca5b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ca5b-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="3ca5b-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3ca5b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3ca5b-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ca5b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ca5b-119">Remarks</span></span>

<span data-ttu-id="3ca5b-120">Este método almacena los valores de marca de tiempo especificados en *startTime* y *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="3ca5b-121">El método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera los mismos valores.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="3ca5b-122">El filtro debe llamar a este método para cada ejemplo que recibe.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="3ca5b-123">El método se sobrecarga para aceptar un puntero al ejemplo o los propios valores de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3ca5b-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca5b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ca5b-124">Requirements</span></span>



| <span data-ttu-id="3ca5b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ca5b-125">Requirement</span></span> | <span data-ttu-id="3ca5b-126">Value</span><span class="sxs-lookup"><span data-stu-id="3ca5b-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca5b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ca5b-127">Header</span></span>  | <span data-ttu-id="3ca5b-128">Ctlutil. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="3ca5b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ca5b-129">Library</span></span> | <span data-ttu-id="3ca5b-130">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="3ca5b-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




