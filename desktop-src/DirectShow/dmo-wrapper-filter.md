---
description: Filtro contenedor DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Filtro contenedor DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908633"
---
# <a name="dmo-wrapper-filter"></a><span data-ttu-id="0507d-103">Filtro contenedor DMO</span><span class="sxs-lookup"><span data-stu-id="0507d-103">DMO Wrapper Filter</span></span>

<span data-ttu-id="0507d-104">El filtro contenedor DMO permite que una aplicación DirectShow use un objeto [multimedia DirectX](directx-media-objects.md) (DMO) dentro de un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="0507d-104">The DMO Wrapper filter enables a DirectShow application to use a [DirectX Media Object](directx-media-objects.md) (DMO) within a filter graph.</span></span> <span data-ttu-id="0507d-105">El filtro encapsula el DMO y controla todos los detalles del uso de DMO, como pasar datos hacia y desde el DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-105">The filter wraps the DMO and handles all the details of using the DMO, such as passing data to and from the DMO.</span></span> <span data-ttu-id="0507d-106">Además, el filtro agrega el DMO, por lo que la aplicación puede consultar el filtro para las interfaces COM que expone el DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-106">Also, the filter aggregates the DMO, so the application can query the filter for any COM interfaces that the DMO exposes.</span></span>



| <span data-ttu-id="0507d-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="0507d-107">Label</span></span> | <span data-ttu-id="0507d-108">Value</span><span class="sxs-lookup"><span data-stu-id="0507d-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0507d-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="0507d-109">Filter Interfaces</span></span>                        | <span data-ttu-id="0507d-110">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IDMOWrapperFilter,**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span><span class="sxs-lookup"><span data-stu-id="0507d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span></span>                                                                                                                       |
| <span data-ttu-id="0507d-111">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="0507d-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="0507d-112">Vea Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0507d-112">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="0507d-113">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="0507d-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0507d-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0507d-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="0507d-115">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="0507d-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="0507d-116">Vea Comentarios.</span><span class="sxs-lookup"><span data-stu-id="0507d-116">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="0507d-117">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="0507d-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0507d-118">[**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0507d-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="0507d-119">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="0507d-119">Filter CLSID</span></span>                             | <span data-ttu-id="0507d-120">CLSID \_ DMOWrapperFilter</span><span class="sxs-lookup"><span data-stu-id="0507d-120">CLSID\_DMOWrapperFilter</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0507d-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0507d-121">Property Page CLSID</span></span>                      | <span data-ttu-id="0507d-122">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0507d-122">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="0507d-123">Executable</span><span class="sxs-lookup"><span data-stu-id="0507d-123">Executable</span></span>                               | <span data-ttu-id="0507d-124">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="0507d-124">Qasf.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0507d-125">Mérito</span><span class="sxs-lookup"><span data-stu-id="0507d-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="0507d-126">Consulte Comentarios</span><span class="sxs-lookup"><span data-stu-id="0507d-126">See Remarks</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="0507d-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="0507d-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0507d-128">Consulte Comentarios</span><span class="sxs-lookup"><span data-stu-id="0507d-128">See Remarks</span></span>                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0507d-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0507d-129">Remarks</span></span>

### <a name="limitations"></a><span data-ttu-id="0507d-130">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="0507d-130">Limitations</span></span>

<span data-ttu-id="0507d-131">El contenedor DMO tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="0507d-131">The DMO Wrapper has the following limitations:</span></span>

-   <span data-ttu-id="0507d-132">No admite DDO con cero entradas, varias entradas o cero salidas.</span><span class="sxs-lookup"><span data-stu-id="0507d-132">It does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span> <span data-ttu-id="0507d-133">(Admite DDO con una entrada y varias salidas).</span><span class="sxs-lookup"><span data-stu-id="0507d-133">(It does support DMOs with one input and multiple outputs.)</span></span>
-   <span data-ttu-id="0507d-134">No admite transportes personalizados.</span><span class="sxs-lookup"><span data-stu-id="0507d-134">It does not support custom transports.</span></span> <span data-ttu-id="0507d-135">Todo el transporte de datos se realiza a través de [**la interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="0507d-135">All data transport is done through the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="0507d-136">No usa la **interfaz IMediaObjectInPlace;** todo el procesamiento se realiza mediante [**métodos IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)</span><span class="sxs-lookup"><span data-stu-id="0507d-136">It does not use the **IMediaObjectInPlace** interface; all processing is done using [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) methods.</span></span>

### <a name="pins"></a><span data-ttu-id="0507d-137">Chinchetas</span><span class="sxs-lookup"><span data-stu-id="0507d-137">Pins</span></span>

<span data-ttu-id="0507d-138">Para cada flujo de entrada del DMO, el filtro crea un pin de entrada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0507d-138">For each input stream on the DMO, the filter creates a corresponding input pin.</span></span> <span data-ttu-id="0507d-139">Para cada flujo de salida, crea un pin de salida correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0507d-139">For each output stream, it creates a corresponding output pin.</span></span> <span data-ttu-id="0507d-140">Los tipos de medios que admite cada pin dependen del DMO</span><span class="sxs-lookup"><span data-stu-id="0507d-140">The media types that each pin supports depends on the DMO</span></span>

### <a name="encoder-interfaces"></a><span data-ttu-id="0507d-141">Interfaces de codificador</span><span class="sxs-lookup"><span data-stu-id="0507d-141">Encoder Interfaces</span></span>

<span data-ttu-id="0507d-142">Si el DMO es un codificador de vídeo o un codificador de audio, el pin de salida expone la [**interfaz IAMStreamConfig.**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)</span><span class="sxs-lookup"><span data-stu-id="0507d-142">If the DMO is a video encoder or an audio encoder, the output pin exposes the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span> <span data-ttu-id="0507d-143">Si DMO es un codificador de vídeo, el pin de salida también expone la [**interfaz IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)</span><span class="sxs-lookup"><span data-stu-id="0507d-143">If the DMO is a video encoder, the output pin also exposes the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="0507d-144">En ambos casos, si el DMO admite la interfaz , el pin delega en el DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-144">In both cases, if the DMO supports the interface, the pin delegates to the DMO.</span></span> <span data-ttu-id="0507d-145">De lo contrario, el pin proporciona su propia implementación.</span><span class="sxs-lookup"><span data-stu-id="0507d-145">Otherwise, the pin provides its own implementation.</span></span>

### <a name="streaming"></a><span data-ttu-id="0507d-146">Streaming</span><span class="sxs-lookup"><span data-stu-id="0507d-146">Streaming</span></span>

<span data-ttu-id="0507d-147">El filtro usa la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) para controlar todo el streaming.</span><span class="sxs-lookup"><span data-stu-id="0507d-147">The filter uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface to handle all streaming.</span></span> <span data-ttu-id="0507d-148">No admite [**conexiones IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)</span><span class="sxs-lookup"><span data-stu-id="0507d-148">It does not support [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connections.</span></span> <span data-ttu-id="0507d-149">El filtro llama [**a IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) en el DMO solo cuando recibe datos de nivel superior (incluidas las notificaciones de fin de flujo).</span><span class="sxs-lookup"><span data-stu-id="0507d-149">The filter calls [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) on the DMO only when it receives data from upstream (including end-of-stream notifications).</span></span> <span data-ttu-id="0507d-150">Por lo tanto, no admite DDO con cero flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="0507d-150">Therefore, it does not support DMOs with zero input streams.</span></span>

### <a name="seeking"></a><span data-ttu-id="0507d-151">Buscando</span><span class="sxs-lookup"><span data-stu-id="0507d-151">Seeking</span></span>

<span data-ttu-id="0507d-152">Todas las solicitudes de búsqueda se pasan al filtro ascendente, a través del primer pin de entrada en el contenedor DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-152">All seek requests are passed to the upstream filter, through the first input pin on the DMO Wrapper.</span></span> <span data-ttu-id="0507d-153">En el caso de las DDO de varias salidas, esto significa que el filtro ascendente podría recibir varias solicitudes de búsqueda cuando la aplicación busca el gráfico.</span><span class="sxs-lookup"><span data-stu-id="0507d-153">For multiple-output DMOs, this means that the upstream filter might receive multiple seek requests when the application seeks the graph.</span></span>

### <a name="merit"></a><span data-ttu-id="0507d-154">Mérito</span><span class="sxs-lookup"><span data-stu-id="0507d-154">Merit</span></span>

<span data-ttu-id="0507d-155">DirectShow asigna a todas las dmO un valor de merececión predeterminado **de NORMAL + \_** 0X800.</span><span class="sxs-lookup"><span data-stu-id="0507d-155">DirectShow assigns all DMOs a default merit value of **MERIT\_NORMAL** + 0x800.</span></span> <span data-ttu-id="0507d-156">Este valor se encuentra entre **LO \_ NORMAL y** **\_ PREFERITORIO PREFERIDO.**</span><span class="sxs-lookup"><span data-stu-id="0507d-156">This value falls between **MERIT\_NORMAL** and **MERIT\_PREFERRED**.</span></span> <span data-ttu-id="0507d-157">Por lo general, los filtros de descodificador tienen un valor de **meritorio de LO \_ NORMAL.**</span><span class="sxs-lookup"><span data-stu-id="0507d-157">Decoder filters generally have a merit value of **MERIT\_NORMAL**.</span></span> <span data-ttu-id="0507d-158">Por lo tanto, el administrador de gráficos de filtros normalmente seleccionará un descodificador DMO sobre un filtro descodificador.</span><span class="sxs-lookup"><span data-stu-id="0507d-158">Therefore, the filter graph manager will usually select a DMO decoder over a decoder filter.</span></span> <span data-ttu-id="0507d-159">Para invalidar el valor de mezquite predeterminado, agregue una entrada del Registro a la clave del Registro del DMO en HKEY \_ CLASSES \_ ROOT \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="0507d-159">To override the default merit value, add a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="0507d-160">Incluya un **valor DWORD** denominado "Valor" cuyo valor especifique el valor.</span><span class="sxs-lookup"><span data-stu-id="0507d-160">Include a **DWORD** value named "Merit" whose value specifies the merit.</span></span>

### <a name="category"></a><span data-ttu-id="0507d-161">Category</span><span class="sxs-lookup"><span data-stu-id="0507d-161">Category</span></span>

<span data-ttu-id="0507d-162">El filtro contenedor DMO no aparece por sí solo en ninguna categoría.</span><span class="sxs-lookup"><span data-stu-id="0507d-162">The DMO Wrapper filter does not appear by itself in any category.</span></span> <span data-ttu-id="0507d-163">Cuando encapsula un DMO, aparece en la categoría DirectShow que corresponde a la categoría del DMO, bajo el nombre del DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-163">When it wraps a DMO, it appears in the DirectShow category that corresponds to the DMO's category, under the name of the DMO.</span></span>

### <a name="buffers"></a><span data-ttu-id="0507d-164">Búferes</span><span class="sxs-lookup"><span data-stu-id="0507d-164">Buffers</span></span>

<span data-ttu-id="0507d-165">El filtro contenedor DMO pasa búferes multimedia al DMO que expone la [**interfaz IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer)</span><span class="sxs-lookup"><span data-stu-id="0507d-165">The DMO Wrapper filter passes media buffers to the DMO which expose the [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) interface.</span></span>

<span data-ttu-id="0507d-166">En Windows Vista o versiones posteriores, los búferes multimedia también exponen la interfaz IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="0507d-166">In Windows Vista or later, the media buffers also expose the IServiceProvider interface.</span></span> <span data-ttu-id="0507d-167">El DMO puede usar esta interfaz para obtener un puntero al ejemplo multimedia asociado al búfer.</span><span class="sxs-lookup"><span data-stu-id="0507d-167">The DMO can use this interface to get a pointer to the media sample that is associated with the buffer.</span></span> <span data-ttu-id="0507d-168">Use el identificador de **servicio IID \_ IMediaSample**.</span><span class="sxs-lookup"><span data-stu-id="0507d-168">Use the service identifier **IID\_IMediaSample**.</span></span> <span data-ttu-id="0507d-169">Un DMO de vídeo puede usar la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) del ejemplo multimedia para establecer marcas de interlace en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0507d-169">A video DMO can use the media sample's [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface to set interlace flags on the sample.</span></span> <span data-ttu-id="0507d-170">El código siguiente muestra cómo obtener el puntero al ejemplo multimedia:</span><span class="sxs-lookup"><span data-stu-id="0507d-170">The following code shows how to get the pointer to the media sample:</span></span>


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



<span data-ttu-id="0507d-171">Para obtener más información sobre las marcas de interlace por ejemplo, vea [**AM \_ SAMPLE2 \_ PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).</span><span class="sxs-lookup"><span data-stu-id="0507d-171">For more information about per-sample interlace flags, see [**AM\_SAMPLE2\_PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).</span></span>

### <a name="quality-control"></a><span data-ttu-id="0507d-172">Control de calidad</span><span class="sxs-lookup"><span data-stu-id="0507d-172">Quality Control</span></span>

<span data-ttu-id="0507d-173">Si DMO expone la interfaz [**IDMOQualityControl,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) el filtro convierte las llamadas [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) en su pin de salida en [**llamadas IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) en el DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-173">If the DMO exposes the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) interface, the filter translates [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) calls on its output pin into [**IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) calls on the DMO.</span></span> <span data-ttu-id="0507d-174">El *parámetro rtNow* de **SetNow** se calcula como la suma de los **miembros TimeStamp** y **Late** de la [**estructura Quality.**](/windows/win32/api/strmif/ns-strmif-quality)</span><span class="sxs-lookup"><span data-stu-id="0507d-174">The *rtNow* parameter of **SetNow** is calculated as the sum of the **TimeStamp** and **Late** members of the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span>

### <a name="using-the-fiter-in-graphedit"></a><span data-ttu-id="0507d-175">Uso de Fiter en GraphEdit</span><span class="sxs-lookup"><span data-stu-id="0507d-175">Using the Fiter in GraphEdit</span></span>

<span data-ttu-id="0507d-176">En GraphEdit, el filtro contenedor DMO no aparece bajo su propio nombre.</span><span class="sxs-lookup"><span data-stu-id="0507d-176">In GraphEdit, the DMO Wrapper filter does not appear under its own name.</span></span> <span data-ttu-id="0507d-177">En su lugar, cada DMO registrado aparece en la categoría de filtro adecuada.</span><span class="sxs-lookup"><span data-stu-id="0507d-177">Instead, each registered DMO is listed under the appropriate filter category.</span></span> <span data-ttu-id="0507d-178">Al agregar un DMO  mediante el cuadro de diálogo Insertar filtros, GraphEdit crea el filtro contenedor de DMO y lo configura para usar ese DMO.</span><span class="sxs-lookup"><span data-stu-id="0507d-178">When you add a DMO through the **Insert Filters** dialog, GraphEdit creates the DMO Wrapper filter and configures it to use that DMO.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0507d-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0507d-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0507d-180">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0507d-180">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0507d-181">Objetos multimedia de DirectX</span><span class="sxs-lookup"><span data-stu-id="0507d-181">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 
