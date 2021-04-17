---
description: El método ShouldDrawSampleNow determina cómo se programa un ejemplo para su representación.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Método CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661271"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="5e091-103">CBaseRenderer. ShouldDrawSampleNow, método</span><span class="sxs-lookup"><span data-stu-id="5e091-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="5e091-104">El `ShouldDrawSampleNow` método determina cómo se programa un ejemplo para su representación.</span><span class="sxs-lookup"><span data-stu-id="5e091-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e091-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e091-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="5e091-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e091-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e091-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="5e091-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5e091-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e091-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5e091-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="5e091-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5e091-110">Puntero a una variable que contiene la hora de inicio del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e091-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="5e091-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="5e091-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5e091-112">Puntero a una variable que contiene la hora de finalización del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e091-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e091-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e091-113">Return value</span></span>

<span data-ttu-id="5e091-114">Devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="5e091-114">Returns S\_FALSE.</span></span> <span data-ttu-id="5e091-115">Si la clase derivada reemplaza este método, devuelva uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e091-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="5e091-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5e091-116">Return code</span></span>                                                                               | <span data-ttu-id="5e091-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e091-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e091-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5e091-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5e091-119">El ejemplo se debe representar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5e091-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="5e091-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5e091-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="5e091-121">El ejemplo debe programarse para la representación, en función de las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5e091-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="5e091-122"><dt>**Código de error**</dt></span><span class="sxs-lookup"><span data-stu-id="5e091-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="5e091-123">No represente este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e091-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="5e091-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e091-124">Remarks</span></span>

<span data-ttu-id="5e091-125">El método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="5e091-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="5e091-126">De forma predeterminada, los ejemplos siempre están programados para su representación en función de sus marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5e091-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="5e091-127">La clase derivada puede invalidar este método. por ejemplo, para implementar el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="5e091-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e091-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e091-128">Requirements</span></span>



| <span data-ttu-id="5e091-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e091-129">Requirement</span></span> | <span data-ttu-id="5e091-130">Value</span><span class="sxs-lookup"><span data-stu-id="5e091-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e091-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e091-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5e091-132"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e091-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e091-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e091-133">Library</span></span><br/> | <dl> <span data-ttu-id="5e091-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5e091-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e091-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e091-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e091-136">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5e091-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




