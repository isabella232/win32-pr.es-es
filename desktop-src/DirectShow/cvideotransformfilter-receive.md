---
description: 'El método Receive recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. Este método invalida el método CTransformFilter:: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Método CVideoTransformFilter. Receive (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680313"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="7b3dd-104">CVideoTransformFilter. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="7b3dd-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="7b3dd-105">El `Receive` método recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="7b3dd-106">Este método invalida el método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="7b3dd-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b3dd-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="7b3dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b3dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3dd-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="7b3dd-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3dd-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) en el ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3dd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b3dd-111">Return value</span></span>

<span data-ttu-id="7b3dd-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b3dd-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7b3dd-113">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b3dd-113">Possible values include the following:</span></span>



| <span data-ttu-id="7b3dd-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7b3dd-114">Return code</span></span>                                                                             | <span data-ttu-id="7b3dd-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b3dd-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="7b3dd-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3dd-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7b3dd-117">El filtro de nivel superior debe dejar de enviar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="7b3dd-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7b3dd-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7b3dd-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="7b3dd-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b3dd-120">Remarks</span></span>

<span data-ttu-id="7b3dd-121">Este método llama a [**CVideoTransformFilter:: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) para determinar si debe proporcionar este ejemplo o simplemente descartarlo.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="7b3dd-122">Si **ShouldSkipFrame** devuelve **false** (lo que indica que se debe entregar el ejemplo), el método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7b3dd-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="7b3dd-123">Llama a [**CTransformFilter:: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) para preparar el ejemplo de salida</span><span class="sxs-lookup"><span data-stu-id="7b3dd-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="7b3dd-124">Llama a [**CTransformFilter:: transform**](ctransformfilter-transform.md) para procesar el ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="7b3dd-125">Este método es virtual puro y debe implementarse en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="7b3dd-126">Llama a [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) para proporcionar el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="7b3dd-127">Además, este método comprueba los cambios de formato en el ejemplo de entrada o salida llamando a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="7b3dd-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="7b3dd-128">Si hay un cambio de formato, el método establece el tipo de conexión en el PIN correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="7b3dd-129">Antes de establecer el nuevo tipo, llama a **StopStreaming**.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="7b3dd-130">Después de establecer el nuevo tipo, llama a **StartStreaming**.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="7b3dd-131">La clase derivada puede usar estos métodos para actualizar su estado interno.</span><span class="sxs-lookup"><span data-stu-id="7b3dd-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="7b3dd-132">La clase derivada también podría necesitar comprobar el nuevo formato en su método de **transformación** .</span><span class="sxs-lookup"><span data-stu-id="7b3dd-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3dd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b3dd-133">Requirements</span></span>



| <span data-ttu-id="7b3dd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3dd-134">Requirement</span></span> | <span data-ttu-id="7b3dd-135">Value</span><span class="sxs-lookup"><span data-stu-id="7b3dd-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3dd-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b3dd-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3dd-137"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3dd-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7b3dd-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b3dd-138">Library</span></span><br/> | <dl> <span data-ttu-id="7b3dd-139"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3dd-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3dd-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b3dd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3dd-141">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="7b3dd-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




