---
description: El filtro Sample Grabber proporciona una manera de recuperar muestras a medida que pasan por el gráfico de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Sample Grabber Filter (Qedit.h)
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
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909673"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="3a833-103">Filtro de captura de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a833-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="3a833-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3a833-104">\[Deprecated.</span></span> <span data-ttu-id="3a833-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3a833-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3a833-106">El filtro Sample Grabber proporciona una manera de recuperar muestras a medida que pasan por el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="3a833-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="3a833-107">Es un filtro de transformación con un pin de entrada y un pin de salida.</span><span class="sxs-lookup"><span data-stu-id="3a833-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="3a833-108">Pasa todos los ejemplos de nivel inferior sin modificar, por lo que puede insertarlo en un gráfico de filtros sin modificar el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="3a833-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="3a833-109">A continuación, la aplicación puede recuperar ejemplos individuales del filtro llamando a métodos en la [**interfaz ISampleGrabber.**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="3a833-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="3a833-110">Si desea recuperar ejemplos sin representar los datos, conecte el filtro Sample Grabber al [**filtro Representador**](null-renderer-filter.md) null.</span><span class="sxs-lookup"><span data-stu-id="3a833-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="3a833-111">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="3a833-111">Label</span></span> | <span data-ttu-id="3a833-112">Value</span><span class="sxs-lookup"><span data-stu-id="3a833-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a833-113">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="3a833-113">Filter interfaces</span></span>                        | <span data-ttu-id="3a833-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="3a833-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="3a833-115">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="3a833-115">Input pin media types</span></span>                    | <span data-ttu-id="3a833-116">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="3a833-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="3a833-117">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="3a833-117">Input pin interfaces</span></span>                     | <span data-ttu-id="3a833-118">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a833-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="3a833-119">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="3a833-119">Output pin media types</span></span>                   | <span data-ttu-id="3a833-120">Cualquier tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="3a833-120">Any media type.</span></span> <span data-ttu-id="3a833-121">Coincide con el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="3a833-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="3a833-122">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="3a833-122">Output pin interfaces</span></span>                    | <span data-ttu-id="3a833-123">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3a833-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3a833-124">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="3a833-124">Filter CLSID</span></span>                             | <span data-ttu-id="3a833-125">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="3a833-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="3a833-126">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="3a833-126">Property Page CLSID</span></span>                      | <span data-ttu-id="3a833-127">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a833-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="3a833-128">Executable</span><span class="sxs-lookup"><span data-stu-id="3a833-128">Executable</span></span>                               | <span data-ttu-id="3a833-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="3a833-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="3a833-130">Mérito</span><span class="sxs-lookup"><span data-stu-id="3a833-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="3a833-131">NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.</span><span class="sxs-lookup"><span data-stu-id="3a833-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="3a833-132">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="3a833-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3a833-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3a833-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3a833-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a833-134">Remarks</span></span>

<span data-ttu-id="3a833-135">Para usar este filtro, agrégalo al gráfico de filtros y llame a [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) con el tipo de medio deseado.</span><span class="sxs-lookup"><span data-stu-id="3a833-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="3a833-136">Este método especifica el tipo de medio para las conexiones de pin de entrada y salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="3a833-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="3a833-137">A continuación, conecte el filtro a otros filtros del gráfico.</span><span class="sxs-lookup"><span data-stu-id="3a833-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="3a833-138">Si llama a [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **TRUE**, el filtro almacena en búfer cada muestra que recibe antes de pasarlo de bajada.</span><span class="sxs-lookup"><span data-stu-id="3a833-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="3a833-139">Llame al [**método ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar el contenido actual del búfer.</span><span class="sxs-lookup"><span data-stu-id="3a833-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="3a833-140">Como alternativa, puede llamar a [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) para que el filtro invoque una función de devolución de llamada cada vez que reciba un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3a833-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="3a833-141">El filtro tiene las siguientes limitaciones para los formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="3a833-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="3a833-142">No admite tipos de vídeo con orientación de arriba a abajo **(biHeight negativo).**</span><span class="sxs-lookup"><span data-stu-id="3a833-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="3a833-143">No admite la estructura de [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual a **FORMAT \_ VideoInfo2).**</span><span class="sxs-lookup"><span data-stu-id="3a833-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="3a833-144">Rechaza cualquier tipo de vídeo en el que el paso de superficie no coincida con el ancho del vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a833-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="3a833-145">Como resultado, Sample Grabber no se conectará al representador de mezcla de vídeo (VMR) para algunos tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a833-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a833-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a833-146">Requirements</span></span>



| <span data-ttu-id="3a833-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a833-147">Requirement</span></span> | <span data-ttu-id="3a833-148">Value</span><span class="sxs-lookup"><span data-stu-id="3a833-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a833-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a833-149">Header</span></span><br/> | <dl> <span data-ttu-id="3a833-150"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="3a833-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a833-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3a833-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a833-152">Objetos de Servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a833-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="3a833-153">Uso de Sample Grabber</span><span class="sxs-lookup"><span data-stu-id="3a833-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




