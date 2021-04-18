---
description: El método GetSampleTimes recupera las marcas de tiempo de un ejemplo.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Método CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660335"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="c0863-103">CBaseRenderer. GetSampleTimes, método</span><span class="sxs-lookup"><span data-stu-id="c0863-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="c0863-104">El `GetSampleTimes` método recupera las marcas de tiempo de un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0863-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0863-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="c0863-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0863-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c0863-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c0863-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c0863-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="c0863-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c0863-110">Puntero a una variable que recibe la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="c0863-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="c0863-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="c0863-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c0863-112">Puntero a una variable que recibe la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="c0863-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0863-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0863-113">Return value</span></span>

<span data-ttu-id="c0863-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0863-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c0863-115">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0863-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c0863-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c0863-116">Return code</span></span>                                                                                                    | <span data-ttu-id="c0863-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0863-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0863-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="c0863-119">El ejemplo se debe representar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c0863-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="c0863-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="c0863-121">El ejemplo debe programarse para la representación, en función de las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c0863-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="c0863-122"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="c0863-123">No represente este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c0863-124"><dt>**hora de inicio de VFW \_ E \_ después del \_ \_ \_ final**</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="c0863-125">Marca de tiempo incorrecta: la hora de finalización es anterior a la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="c0863-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="c0863-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0863-126">Remarks</span></span>

<span data-ttu-id="c0863-127">El filtro llama a este método para determinar cómo debe controlar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="c0863-128">Si el valor devuelto es S \_ OK, el filtro representa el ejemplo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c0863-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="c0863-129">Si el valor devuelto es S \_ false, el filtro programa el ejemplo para su representación, en función de las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c0863-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="c0863-130">Si el valor devuelto es un código de error, el filtro rechaza el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="c0863-131">Este método devuelve S \_ OK si el ejemplo no tiene marcas de tiempo, o si el filtro no tiene un reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="c0863-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="c0863-132">De lo contrario, devuelve el valor del método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) .</span><span class="sxs-lookup"><span data-stu-id="c0863-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="c0863-133">En la clase base, **ShouldDrawSampleNow** siempre devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="c0863-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="c0863-134">La clase derivada puede invalidar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="c0863-134">The derived class can override this behavior.</span></span> <span data-ttu-id="c0863-135">Por ejemplo, si la clase derivada implementa la administración de control de calidad, podría devolver E \_ no quitar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c0863-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0863-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0863-136">Requirements</span></span>



| <span data-ttu-id="c0863-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0863-137">Requirement</span></span> | <span data-ttu-id="c0863-138">Value</span><span class="sxs-lookup"><span data-stu-id="c0863-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0863-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0863-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c0863-140"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0863-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0863-141">Library</span></span><br/> | <dl> <span data-ttu-id="c0863-142"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c0863-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0863-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0863-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0863-144">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c0863-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




