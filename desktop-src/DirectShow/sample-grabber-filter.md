---
description: El filtro de enganche de ejemplo proporciona una manera de recuperar ejemplos a medida que pasan por el gráfico de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro de enganche de ejemplo (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679025"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="8b4e5-103">Filtro de enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b4e5-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="8b4e5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-104">\[Deprecated.</span></span> <span data-ttu-id="8b4e5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b4e5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8b4e5-106">El filtro de enganche de ejemplo proporciona una manera de recuperar ejemplos a medida que pasan por el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="8b4e5-107">Es un filtro de transformación con un PIN de entrada y un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="8b4e5-108">Pasa todos los ejemplos de nivel inferior sin cambios, por lo que puede insertarlo en un gráfico de filtro sin modificar el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="8b4e5-109">A continuación, la aplicación puede recuperar muestras individuales del filtro llamando a los métodos de la interfaz [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="8b4e5-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="8b4e5-110">Si desea recuperar muestras sin representar los datos, conecte el filtro de enganche de ejemplo al filtro de [**representador nulo**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8b4e5-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4e5-111">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="8b4e5-111">Filter interfaces</span></span>                        | <span data-ttu-id="8b4e5-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="8b4e5-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="8b4e5-113">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="8b4e5-113">Input pin media types</span></span>                    | <span data-ttu-id="8b4e5-114">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="8b4e5-115">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="8b4e5-115">Input pin interfaces</span></span>                     | <span data-ttu-id="8b4e5-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8b4e5-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="8b4e5-117">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="8b4e5-117">Output pin media types</span></span>                   | <span data-ttu-id="8b4e5-118">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-118">Any media type.</span></span> <span data-ttu-id="8b4e5-119">Coincide con el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="8b4e5-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="8b4e5-120">Output pin interfaces</span></span>                    | <span data-ttu-id="8b4e5-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8b4e5-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8b4e5-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="8b4e5-122">Filter CLSID</span></span>                             | <span data-ttu-id="8b4e5-123">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="8b4e5-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="8b4e5-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="8b4e5-124">Property Page CLSID</span></span>                      | <span data-ttu-id="8b4e5-125">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="8b4e5-126">Executable</span><span class="sxs-lookup"><span data-stu-id="8b4e5-126">Executable</span></span>                               | <span data-ttu-id="8b4e5-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="8b4e5-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="8b4e5-128">Fundament</span><span class="sxs-lookup"><span data-stu-id="8b4e5-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="8b4e5-129">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="8b4e5-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="8b4e5-130">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="8b4e5-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8b4e5-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8b4e5-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="8b4e5-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b4e5-132">Remarks</span></span>

<span data-ttu-id="8b4e5-133">Para usar este filtro, agréguelo al gráfico de filtro y llame a [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) con el tipo de medio deseado.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="8b4e5-134">Este método especifica el tipo de medio para las conexiones de la clavija de entrada y salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="8b4e5-135">A continuación, conecte el filtro a otros filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="8b4e5-136">Si llama a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **true**, el filtro almacena en búfer cada ejemplo que recibe antes de pasarlo a nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="8b4e5-137">Llame al método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar el contenido actual del búfer.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="8b4e5-138">Como alternativa, puede llamar a [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) para que el filtro invoque una función de devolución de llamada cada vez que reciba un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="8b4e5-139">El filtro tiene las siguientes limitaciones para los formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="8b4e5-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="8b4e5-140">No admite los tipos de vídeo con orientación descendente ( **bialtura** negativa).</span><span class="sxs-lookup"><span data-stu-id="8b4e5-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="8b4e5-141">No admite la estructura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (el tipo de formato es igual al **formato \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="8b4e5-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="8b4e5-142">Rechaza cualquier tipo de vídeo en el que el intervalo de la superficie no coincida con el ancho del vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="8b4e5-143">Como resultado, el enganche de ejemplo no se conectará al representador de mezcla de vídeo (VMR) para algunos tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b4e5-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4e5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b4e5-144">Requirements</span></span>



| <span data-ttu-id="8b4e5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b4e5-145">Requirement</span></span> | <span data-ttu-id="8b4e5-146">Value</span><span class="sxs-lookup"><span data-stu-id="8b4e5-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4e5-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b4e5-147">Header</span></span><br/> | <dl> <span data-ttu-id="8b4e5-148"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b4e5-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b4e5-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b4e5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4e5-150">Objetos de servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b4e5-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="8b4e5-151">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b4e5-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




