---
description: En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en un filtro de descodificador de DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Compatibilidad con DXVA 2,0 en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908369"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="789ed-103">Compatibilidad con DXVA 2,0 en DirectShow</span><span class="sxs-lookup"><span data-stu-id="789ed-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="789ed-104">En este tema se describe cómo admitir la aceleración de vídeo de DirectX (DXVA) 2,0 en un filtro de descodificador de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="789ed-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="789ed-105">En concreto, describe la comunicación entre el descodificador y el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="789ed-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="789ed-106">En este tema no se describe cómo implementar la descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="789ed-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="789ed-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="789ed-108">Notas de migración</span><span class="sxs-lookup"><span data-stu-id="789ed-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="789ed-109">Buscar una configuración de descodificador</span><span class="sxs-lookup"><span data-stu-id="789ed-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="789ed-110">Notificar al representador de vídeo</span><span class="sxs-lookup"><span data-stu-id="789ed-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="789ed-111">Asignación de búferes sin comprimir</span><span class="sxs-lookup"><span data-stu-id="789ed-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="789ed-112">Descodificación</span><span class="sxs-lookup"><span data-stu-id="789ed-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="789ed-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="789ed-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="789ed-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="789ed-114">Prerequisites</span></span>

<span data-ttu-id="789ed-115">En este tema se da por supuesto que está familiarizado con la escritura de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="789ed-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="789ed-116">Para obtener más información, vea el tema [Writing DirectShow filters](../directshow/writing-directshow-filters.md) en la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="789ed-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="789ed-117">En los ejemplos de código de este tema se supone que el filtro del descodificador se deriva de la clase [**CTransformFilter**](../directshow/ctransformfilter.md) , con la siguiente definición de clase:</span><span class="sxs-lookup"><span data-stu-id="789ed-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="789ed-118">En el resto de este tema, el término *descodificador* hace referencia al filtro del descodificador, que recibe vídeo comprimido y genera vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="789ed-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="789ed-119">El término *dispositivo descodificador* hace referencia a un acelerador de vídeo de hardware implementado por el controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="789ed-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="789ed-120">Estos son los pasos básicos que un filtro de descodificador debe realizar para admitir DXVA 2,0:</span><span class="sxs-lookup"><span data-stu-id="789ed-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="789ed-121">Negocie un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="789ed-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="789ed-122">Busque una configuración de descodificador de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="789ed-123">Notifique al representador de vídeo que el descodificador usa la descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="789ed-124">Proporcione un asignador personalizado que asigne superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="789ed-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="789ed-125">Estos pasos se describen con más detalle en el resto de este tema.</span><span class="sxs-lookup"><span data-stu-id="789ed-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="789ed-126">Notas de migración</span><span class="sxs-lookup"><span data-stu-id="789ed-126">Migration Notes</span></span>

<span data-ttu-id="789ed-127">Si va a migrar desde DXVA 1,0, debe tener en cuenta algunas diferencias significativas entre las dos versiones:</span><span class="sxs-lookup"><span data-stu-id="789ed-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="789ed-128">DXVA 2,0 no usa las interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) y [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , porque el descodificador puede acceder a las API de DXVA 2,0 directamente a través de la interfaz [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="789ed-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="789ed-129">Durante la negociación del tipo de medio, el descodificador no utiliza un GUID de aceleración de vídeo como subtipo.</span><span class="sxs-lookup"><span data-stu-id="789ed-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="789ed-130">En su lugar, el subtipo es simplemente el formato de vídeo sin comprimir (como NV12), al igual que con la descodificación de software.</span><span class="sxs-lookup"><span data-stu-id="789ed-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="789ed-131">Ha cambiado el procedimiento para configurar el acelerador.</span><span class="sxs-lookup"><span data-stu-id="789ed-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="789ed-132">En DXVA 1,0, el descodificador llama a **Execute** con una estructura de **DXVA \_ ConfigPictureDecode** para configurar accerlator.</span><span class="sxs-lookup"><span data-stu-id="789ed-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="789ed-133">En DXVA 2,0, el descodificador usa la interfaz [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="789ed-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="789ed-134">El descodificador asigna los búferes sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="789ed-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="789ed-135">El representador de vídeo ya no los asigna.</span><span class="sxs-lookup"><span data-stu-id="789ed-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="789ed-136">En lugar de llamar a [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) para mostrar el fotograma descodificado, el descodificador entrega el fotograma al representador llamando a [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), como con la descodificación de software.</span><span class="sxs-lookup"><span data-stu-id="789ed-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="789ed-137">El descodificador ya no es responsable de comprobar cuándo los búferes de datos son seguros para las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="789ed-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="789ed-138">Por lo tanto, DXVA 2,0 no tiene ningún método equivalente a [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span><span class="sxs-lookup"><span data-stu-id="789ed-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="789ed-139">El representador de vídeo realiza la combinación de subimágenes mediante las API del procesador de vídeo de DXVA 2.0.</span><span class="sxs-lookup"><span data-stu-id="789ed-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="789ed-140">Los descodificadores que proporcionan subimágenes (por ejemplo, descodificadores de DVD) deben enviar datos de subimagen en un PIN de salida independiente.</span><span class="sxs-lookup"><span data-stu-id="789ed-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="789ed-141">En el caso de las operaciones de descodificación, DXVA 2,0 utiliza las mismas estructuras de datos que DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="789ed-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="789ed-142">El filtro de representador de vídeo mejorado (EVR) admite DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="789ed-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="789ed-143">Los filtros de representador de combinación de vídeo (VMR-7 y VMR-9) solo admiten DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="789ed-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="789ed-144">Buscar una configuración de descodificador</span><span class="sxs-lookup"><span data-stu-id="789ed-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="789ed-145">Después de que el descodificador negocie el tipo de medio de salida, debe encontrar una configuración compatible para el dispositivo descodificador de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="789ed-146">Puede realizar este paso dentro del método [**CBaseOutputPin:: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="789ed-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="789ed-147">Este paso garantiza que el controlador de gráficos admita las capacidades que necesita el descodificador antes de que el descodificador se confirme para usar DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="789ed-148">Para buscar una configuración para el dispositivo descodificador, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="789ed-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="789ed-149">Consulte el PIN de entrada del representador para la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="789ed-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="789ed-150">Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="789ed-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="789ed-151">El GUID del servicio es el \_ servicio de aceleración de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="789ed-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="789ed-152">Llame a [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obtener un identificador para el dispositivo Direct3D del representador.</span><span class="sxs-lookup"><span data-stu-id="789ed-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="789ed-153">Llame a [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) y pase el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="789ed-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="789ed-154">Este método devuelve un puntero a la interfaz [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="789ed-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="789ed-155">Llame a [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="789ed-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="789ed-156">Este método devuelve una matriz de GUID de dispositivo de descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="789ed-157">Recorra en iteración la matriz de GUID del descodificador para buscar los que admite el filtro del descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="789ed-158">Por ejemplo, para un descodificador MPEG-2, buscará **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** o **DXVA2 \_ \_** ModeMPEG2 VLD.</span><span class="sxs-lookup"><span data-stu-id="789ed-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="789ed-159">Cuando encuentre un GUID de dispositivo descodificador candidato, pase el GUID al método [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) .</span><span class="sxs-lookup"><span data-stu-id="789ed-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="789ed-160">Este método devuelve una matriz de formatos de destino de representación, especificados como valores de **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="789ed-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="789ed-161">Recorra los formatos de destino de representación y busque uno que coincida con el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="789ed-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="789ed-162">Normalmente, un dispositivo descodificador admite un solo formato de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="789ed-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="789ed-163">El filtro del descodificador debe conectarse al representador mediante este subtipo.</span><span class="sxs-lookup"><span data-stu-id="789ed-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="789ed-164">En la primera llamada a [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), el descodificador puede determinar el formato del destino de representación y, a continuación, devolver este formato como un tipo de salida preferido.</span><span class="sxs-lookup"><span data-stu-id="789ed-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="789ed-165">Llame a [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="789ed-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="789ed-166">Pase el mismo GUID del dispositivo descodificador, junto con una [**estructura \_ videodesc DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que describe el formato propuesto.</span><span class="sxs-lookup"><span data-stu-id="789ed-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="789ed-167">El método devuelve una matriz de estructuras [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) .</span><span class="sxs-lookup"><span data-stu-id="789ed-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="789ed-168">Cada estructura describe una posible configuración para el dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="789ed-169">Suponiendo que los pasos anteriores son correctos, almacene el identificador del dispositivo Direct3D, el GUID del dispositivo descodificador y la estructura de configuración.</span><span class="sxs-lookup"><span data-stu-id="789ed-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="789ed-170">El filtro usará esta información para crear el dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="789ed-171">En el código siguiente se muestra cómo buscar una configuración de descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="789ed-172">Dado que este ejemplo es genérico, parte de la lógica se ha colocado en funciones auxiliares que deben ser implementadas por el descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="789ed-173">En el código siguiente se muestran las declaraciones de estas funciones:</span><span class="sxs-lookup"><span data-stu-id="789ed-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="789ed-174">Notificar al representador de vídeo</span><span class="sxs-lookup"><span data-stu-id="789ed-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="789ed-175">Si el descodificador encuentra una configuración de descodificador, el siguiente paso es notificar al representador de vídeo que el descodificador usará la aceleración de hardware.</span><span class="sxs-lookup"><span data-stu-id="789ed-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="789ed-176">Puede realizar este paso dentro del método [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="789ed-177">Este paso debe realizarse antes de que se seleccione allocator, porque afecta al modo en que se selecciona allocator.</span><span class="sxs-lookup"><span data-stu-id="789ed-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="789ed-178">Consulte el PIN de entrada del representador para la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="789ed-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="789ed-179">Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la interfaz [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="789ed-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="789ed-180">El GUID del servicio es el **\_ servicio de \_ aceleración \_ de vídeo Mr**.</span><span class="sxs-lookup"><span data-stu-id="789ed-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="789ed-181">Llame a [**IDirectXVideoMemoryConfiguration:: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) en un bucle, incrementando la variable *dwTypeIndex* desde cero.</span><span class="sxs-lookup"><span data-stu-id="789ed-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="789ed-182">Detenga cuando el método devuelva el valor **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** en el parámetro *pdwType* .</span><span class="sxs-lookup"><span data-stu-id="789ed-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="789ed-183">Este paso garantiza que el representador de vídeo admita la descodificación acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="789ed-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="789ed-184">Este paso siempre se realizará correctamente para el filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="789ed-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="789ed-185">Si el paso anterior se realizó correctamente, llame a [**IDirectXVideoMemoryConfiguration:: SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) con el valor DXVA2 \_ SurfaceType \_ DecoderRenderTarget.</span><span class="sxs-lookup"><span data-stu-id="789ed-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="789ed-186">Al llamar a **SetSurfaceType** con este valor, el representador de vídeo se coloca en el modo DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="789ed-187">Cuando el representador de vídeo está en este modo, el descodificador debe proporcionar su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="789ed-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="789ed-188">En el código siguiente se muestra cómo notificar al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="789ed-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="789ed-189">Si el descodificador encuentra una configuración válida y notifica correctamente al representador de vídeo, el descodificador puede usar DXVA para la descodificación.</span><span class="sxs-lookup"><span data-stu-id="789ed-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="789ed-190">El descodificador debe implementar un asignador personalizado para su PIN de salida, tal y como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="789ed-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="789ed-191">Asignación de búferes sin comprimir</span><span class="sxs-lookup"><span data-stu-id="789ed-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="789ed-192">En DXVA 2,0, el descodificador es responsable de asignar las superficies de Direct3D que se usarán como búferes de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="789ed-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="789ed-193">Por lo tanto, el descodificador debe implementar un asignador personalizado que creará las superficies.</span><span class="sxs-lookup"><span data-stu-id="789ed-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="789ed-194">Los ejemplos de medios proporcionados por este asignador conservarán los punteros a las superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="789ed-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="789ed-195">EVR recupera un puntero a la superficie llamando a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="789ed-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="789ed-196">El identificador de servicio es **el \_ \_ servicio de búfer Mr**.</span><span class="sxs-lookup"><span data-stu-id="789ed-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="789ed-197">Para proporcionar el asignador personalizado, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="789ed-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="789ed-198">Defina una clase para los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="789ed-198">Define a class for the media samples.</span></span> <span data-ttu-id="789ed-199">Esta clase se puede derivar de la clase [**CMediaSample**](../directshow/cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="789ed-200">Dentro de esta clase, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="789ed-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="789ed-201">Almacene un puntero a la superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="789ed-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="789ed-202">Implemente la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="789ed-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="789ed-203">En el método [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , si el GUID del servicio es el **\_ \_ servicio de búfer Mr**, consulte la superficie de Direct3D para la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="789ed-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="789ed-204">De lo contrario, **GetService** puede devolver el **\_ servicio MF E \_ no compatible \_**.</span><span class="sxs-lookup"><span data-stu-id="789ed-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="789ed-205">Invalide el método [**CMediaSample:: GetPointer**](../directshow/cmediasample-getpointer.md) para devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="789ed-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="789ed-206">Defina una clase para el asignador.</span><span class="sxs-lookup"><span data-stu-id="789ed-206">Define a class for the allocator.</span></span> <span data-ttu-id="789ed-207">El asignador puede derivar de la clase [**CBaseAllocator**](../directshow/cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="789ed-208">Dentro de esta clase, haga lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="789ed-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="789ed-209">Invalide el método [**CBaseAllocator:: Alloc**](../directshow/cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="789ed-210">Dentro de este método, llame a [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) para crear las superficies.</span><span class="sxs-lookup"><span data-stu-id="789ed-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="789ed-211">(La interfaz [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) hereda este método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)).</span><span class="sxs-lookup"><span data-stu-id="789ed-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="789ed-212">Invalide el método [**CBaseAllocator:: Free**](../directshow/cbaseallocator-free.md) para liberar las superficies.</span><span class="sxs-lookup"><span data-stu-id="789ed-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="789ed-213">En el PIN de salida del filtro, invalide el método [**CBaseOutputPin:: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="789ed-214">Dentro de este método, cree una instancia de su asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="789ed-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="789ed-215">En el filtro, implemente el método [**CTransformFilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="789ed-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="789ed-216">El parámetro *pProperties* indica el número de superficies que requiere EVR.</span><span class="sxs-lookup"><span data-stu-id="789ed-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="789ed-217">Agregue a este valor el número de superficies que el descodificador requiere y llame a [**IMemAllocator:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) en el asignador.</span><span class="sxs-lookup"><span data-stu-id="789ed-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="789ed-218">En el código siguiente se muestra cómo implementar la clase de ejemplo multimedia:</span><span class="sxs-lookup"><span data-stu-id="789ed-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="789ed-219">En el código siguiente se muestra cómo implementar el método [**Alloc**](../directshow/cbaseallocator-alloc.md) en el asignador.</span><span class="sxs-lookup"><span data-stu-id="789ed-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="789ed-220">Este es el código para el método [**Free**](../directshow/cbaseallocator-free.md) :</span><span class="sxs-lookup"><span data-stu-id="789ed-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="789ed-221">Para obtener más información sobre la implementación de asignadores personalizados, vea el tema [proporcionar un asignador personalizado](../directshow/providing-a-custom-allocator.md) en la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="789ed-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="789ed-222">Descodificación</span><span class="sxs-lookup"><span data-stu-id="789ed-222">Decoding</span></span>

<span data-ttu-id="789ed-223">Para crear el dispositivo descodificador, llame a [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span><span class="sxs-lookup"><span data-stu-id="789ed-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="789ed-224">El método devuelve un puntero a la interfaz [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) del dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="789ed-225">En cada fotograma, llame a [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para probar el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="789ed-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="789ed-226">Si el dispositivo ha cambiado, el método devuelve DXVA2 \_ E \_ nuevo \_ dispositivo de vídeo \_ .</span><span class="sxs-lookup"><span data-stu-id="789ed-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="789ed-227">Si esto ocurre, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="789ed-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="789ed-228">Cierre el identificador del dispositivo mediante una llamada a [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="789ed-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="789ed-229">Libere los punteros [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) y [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="789ed-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="789ed-230">Abra un nuevo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="789ed-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="789ed-231">Negocie una nueva configuración del descodificador, como se describe en la sección [buscar una configuración de descodificador](#finding-a-decoder-configuration).</span><span class="sxs-lookup"><span data-stu-id="789ed-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="789ed-232">Cree un nuevo dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="789ed-232">Create a new decoder device.</span></span>

<span data-ttu-id="789ed-233">Suponiendo que el identificador del dispositivo es válido, el proceso de descodificación funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="789ed-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="789ed-234">Llame a [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="789ed-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="789ed-235">Haga lo siguiente una o varias veces:</span><span class="sxs-lookup"><span data-stu-id="789ed-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="789ed-236">Llame a [**IDirectXVideoDecoder:: getBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obtener un búfer del descodificador de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="789ed-237">Rellene el búfer.</span><span class="sxs-lookup"><span data-stu-id="789ed-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="789ed-238">Llame a [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="789ed-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="789ed-239">Llame a [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para realizar las operaciones de descodificación en el marco.</span><span class="sxs-lookup"><span data-stu-id="789ed-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="789ed-240">DXVA 2,0 utiliza las mismas estructuras de datos que DXVA 1,0 para las operaciones de descodificación.</span><span class="sxs-lookup"><span data-stu-id="789ed-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="789ed-241">En el conjunto original de perfiles de DXVA (para H. 261, H. 263 y MPEG-2), estas estructuras de datos se describen en la [especificación de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="789ed-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="789ed-242">Dentro de cada par de llamadas de ejecución de [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , puede llamar a [**getBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) varias veces, pero solo una vez para cada tipo de búfer de DXVA.</span><span class="sxs-lookup"><span data-stu-id="789ed-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="789ed-243">Si se llama dos veces con el mismo tipo de búfer, se sobrescribirán los datos.</span><span class="sxs-lookup"><span data-stu-id="789ed-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="789ed-244">Después de llamar a [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), llame a [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) para enviar el fotograma al representador de vídeo, como con la descodificación de software.</span><span class="sxs-lookup"><span data-stu-id="789ed-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="789ed-245">El método **Receive** es asincrónico; una vez que devuelve, el descodificador puede continuar descodificando el fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="789ed-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="789ed-246">El controlador de pantalla impide que los comandos de descodificación sobrescriban el búfer mientras el búfer está en uso.</span><span class="sxs-lookup"><span data-stu-id="789ed-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="789ed-247">El descodificador no debe reutilizar una superficie para descodificar otro fotograma hasta que el representador haya lanzado el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="789ed-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="789ed-248">Cuando el representador libera el ejemplo, el asignador vuelve a colocar el ejemplo en su grupo de ejemplos disponibles.</span><span class="sxs-lookup"><span data-stu-id="789ed-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="789ed-249">Para obtener el siguiente ejemplo disponible, llame a [**CBaseOutputPin:: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), que a su vez llama a [**IMemAllocator:: getBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="789ed-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="789ed-250">Para obtener más información, vea el tema [información general sobre el flujo de datos en DirectShow](../directshow/overview-of-data-flow-in-directshow.md) en la documentación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="789ed-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="789ed-251">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="789ed-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="789ed-252">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="789ed-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
