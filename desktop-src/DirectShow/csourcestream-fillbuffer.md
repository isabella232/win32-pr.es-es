---
description: El método FillBuffer rellena un ejemplo multimedia con datos.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: CSourceStream. FillBuffer (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690268"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="5cf42-103">CSourceStream. FillBuffer, método</span><span class="sxs-lookup"><span data-stu-id="5cf42-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="5cf42-104">El `FillBuffer` método rellena un ejemplo multimedia con datos.</span><span class="sxs-lookup"><span data-stu-id="5cf42-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cf42-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="5cf42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5cf42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cf42-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="5cf42-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5cf42-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5cf42-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cf42-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cf42-109">Return value</span></span>

<span data-ttu-id="5cf42-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5cf42-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5cf42-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5cf42-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="5cf42-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5cf42-112">Return code</span></span>                                                                             | <span data-ttu-id="5cf42-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cf42-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="5cf42-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5cf42-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5cf42-115">Final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="5cf42-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="5cf42-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5cf42-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5cf42-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="5cf42-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5cf42-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cf42-118">Remarks</span></span>

<span data-ttu-id="5cf42-119">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="5cf42-119">The derived class must implement this method.</span></span>

<span data-ttu-id="5cf42-120">El ejemplo multimedia dado a este método no tiene marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5cf42-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="5cf42-121">La clase derivada debe llamar al método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) para establecer las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5cf42-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="5cf42-122">Si es adecuado para el tipo de medio, la clase derivada también debe establecer las horas del medio, llamando al método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="5cf42-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="5cf42-123">Para obtener más información, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5cf42-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="5cf42-124">Devuelve S \_ false al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cf42-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="5cf42-125">Esto hace que la clase **CSourceStream** envíe la notificación de final de secuencia y detenga el bucle de procesamiento del búfer.</span><span class="sxs-lookup"><span data-stu-id="5cf42-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="5cf42-126">Vea [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5cf42-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf42-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cf42-127">Requirements</span></span>



| <span data-ttu-id="5cf42-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cf42-128">Requirement</span></span> | <span data-ttu-id="5cf42-129">Value</span><span class="sxs-lookup"><span data-stu-id="5cf42-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf42-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cf42-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5cf42-131"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf42-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5cf42-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cf42-132">Library</span></span><br/> | <dl> <span data-ttu-id="5cf42-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf42-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf42-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cf42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf42-135">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="5cf42-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




