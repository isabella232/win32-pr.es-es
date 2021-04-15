---
description: El método PrepareReceive prepara el filtro para representar un ejemplo.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Método CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661329"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="833df-103">CBaseRenderer. PrepareReceive, método</span><span class="sxs-lookup"><span data-stu-id="833df-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="833df-104">El `PrepareReceive` método prepara el filtro para representar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="833df-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="833df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="833df-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="833df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="833df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833df-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="833df-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="833df-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="833df-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833df-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="833df-109">Return value</span></span>

<span data-ttu-id="833df-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="833df-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="833df-111">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="833df-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="833df-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="833df-112">Return code</span></span>                                                                                             | <span data-ttu-id="833df-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="833df-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="833df-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="833df-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="833df-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="833df-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="833df-116"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="833df-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="833df-117">Failed.</span><span class="sxs-lookup"><span data-stu-id="833df-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="833df-118"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="833df-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="833df-119">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="833df-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="833df-120"><dt>**\_ejemplo VFW \_ E \_ rechazado**</dt></span><span class="sxs-lookup"><span data-stu-id="833df-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="833df-121">El filtro está quitando este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="833df-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="833df-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="833df-122">Remarks</span></span>

<span data-ttu-id="833df-123">El filtro llama a este método desde dentro del método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) , antes de representar un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="833df-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="833df-124">Si el filtro se está ejecutando, este método programa el ejemplo para la representación.</span><span class="sxs-lookup"><span data-stu-id="833df-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="833df-125">Si el filtro ya tiene un ejemplo pendiente, o si ya se ha alcanzado el final de la secuencia, el método devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="833df-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="833df-126">Posiblemente el filtro de nivel superior no está serializando correctamente sus llamadas de streaming.</span><span class="sxs-lookup"><span data-stu-id="833df-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="833df-127">Si el algoritmo de programación determina que se debe quitar el ejemplo (vea [**CBaseRenderer:: ScheduleSample**](cbaserenderer-schedulesample.md)), el método devuelve el \_ ejemplo VFW E \_ \_ rechazado.</span><span class="sxs-lookup"><span data-stu-id="833df-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="833df-128">Sin embargo, el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN de entrada no pasa este código de error al filtro de nivel superior, porque la eliminación de una muestra no es un error.</span><span class="sxs-lookup"><span data-stu-id="833df-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="833df-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="833df-129">Requirements</span></span>



| <span data-ttu-id="833df-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="833df-130">Requirement</span></span> | <span data-ttu-id="833df-131">Value</span><span class="sxs-lookup"><span data-stu-id="833df-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="833df-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="833df-132">Header</span></span><br/>  | <dl> <span data-ttu-id="833df-133"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="833df-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="833df-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="833df-134">Library</span></span><br/> | <dl> <span data-ttu-id="833df-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="833df-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833df-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="833df-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833df-137">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="833df-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




