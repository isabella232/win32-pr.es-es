---
description: La MFT de estabilización de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la estabilización de la imagen en una secuencia de vídeo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Video Stabilization MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671607"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="de161-103">Video Stabilization MFT</span><span class="sxs-lookup"><span data-stu-id="de161-103">Video Stabilization MFT</span></span>

<span data-ttu-id="de161-104">La MFT de estabilización de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la estabilización de la imagen en una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="de161-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="de161-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="de161-105">CLSID</span></span>

<span data-ttu-id="de161-106">CLSID \_ CMSVideoDSPMFT</span><span class="sxs-lookup"><span data-stu-id="de161-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="de161-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="de161-107">Interfaces</span></span>

-   [<span data-ttu-id="de161-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="de161-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="de161-109">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="de161-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="de161-110">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="de161-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="de161-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="de161-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="de161-112">**IMediaExtension**</span><span class="sxs-lookup"><span data-stu-id="de161-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="de161-113">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="de161-113">Input Formats</span></span>

<span data-ttu-id="de161-114">El tipo de medio de entrada y las combinaciones de subtipos aceptadas por el MFT de estabilización de vídeo para el vídeo sin comprimir son:</span><span class="sxs-lookup"><span data-stu-id="de161-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="de161-115">**vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="de161-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="de161-116">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="de161-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="de161-117">**MEDIASUBTYPE \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="de161-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="de161-118">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="de161-118">Output Formats</span></span>

<span data-ttu-id="de161-119">El tipo de medio de salida y las combinaciones de subtipos aceptadas por la MFT de estabilización de vídeo son:</span><span class="sxs-lookup"><span data-stu-id="de161-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="de161-120">**vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="de161-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="de161-121">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="de161-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="de161-122">El tipo de medio de entrada debe establecerse antes que el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="de161-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="de161-123">En la mayoría de los casos, la compatibilidad con formato limitado no es un problema porque la canalización inserta automáticamente las conversiones de color necesarias.</span><span class="sxs-lookup"><span data-stu-id="de161-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="de161-124">El componente MFT de estabilización de vídeo es capaz de cambiar el formato dinámico cuando cambia la entrada.</span><span class="sxs-lookup"><span data-stu-id="de161-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="de161-125">Cuando cambia el tamaño de la imagen de entrada o cambia el subtipo, se desencadena un cambio de formato dinámico en el flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="de161-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="de161-126">La MFT de estabilización de vídeo realizará la conversión de colores en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="de161-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="de161-127">Cuando el formato de entrada es **MEDIASUBTYPE \_ YUY2**.</span><span class="sxs-lookup"><span data-stu-id="de161-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="de161-128">Cuando se utiliza el modo de compatibilidad de Microsoft DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="de161-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="de161-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="de161-129">Attributes</span></span>

<span data-ttu-id="de161-130">Los siguientes atributos son compatibles con la MFT de estabilización de vídeo a través de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="de161-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="de161-131">El atributo [MF \_ VIDEODSP \_ mode](mf-videodsp-mode.md) coloca el MFT de estabilización de vídeo en el modo de estabilización o en el modo de paso a través.</span><span class="sxs-lookup"><span data-stu-id="de161-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="de161-132">La aplicación debe llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el **\_ \_ tipo VIDEODSP** de GUID MF con un entero correspondiente a uno de los siguientes valores válidos: **\_ estabilización MFVideoDSPMode** = 4, **MFVideoDSPMode \_ passthrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="de161-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="de161-133">\_ \_ El modo MF VIDEODSP se puede cambiar en cualquier momento durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="de161-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="de161-134">Esto provoca un cambio de modo dinámico.</span><span class="sxs-lookup"><span data-stu-id="de161-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="de161-135">La salida cambiará a estabilizada o a paso a través después de 16 o 2 fotogramas (dependiendo del modo de latencia) una vez cambiado el atributo.</span><span class="sxs-lookup"><span data-stu-id="de161-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="de161-136">El atributo [MF \_ Low \_ latencia](mf-low-latency.md) coloca la MFT de estabilización de vídeo en el modo de latencia baja o en el modo de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="de161-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="de161-137">La aplicación debe llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MF \_ Low \_ latencia** con un entero correspondiente a uno de los siguientes valores válidos: latencia baja = 1 alta calidad = 0</span><span class="sxs-lookup"><span data-stu-id="de161-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="de161-138">La canalización usa el atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) para especificar las marcas de enlace D3D11 con las que se van a crear los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="de161-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="de161-139">Cualquier combinación de valores de la enumeración de [**\_ \_ marcadores de enlace D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) es válida.</span><span class="sxs-lookup"><span data-stu-id="de161-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="de161-140">La canalización utiliza el atributo **MF de \_ ejemplo de salida mínima de la \_ \_ \_ \_ cuenta** para especificar el número mínimo de muestras que este componente debe admitir en la salida.</span><span class="sxs-lookup"><span data-stu-id="de161-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="de161-141">El atributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) se establece en cada muestra generada por la estabilización para indicar el [ \_ \_ modo de MF VIDEODSP](mf-videodsp-mode.md) vigente que se aplica a ese ejemplo (si el ejemplo se ha estabilizado o no).</span><span class="sxs-lookup"><span data-stu-id="de161-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="de161-142">En determinadas condiciones, es posible que los ejemplos no estén estabilizados (debido a una carga elevada del sistema o a las solicitudes del usuario).</span><span class="sxs-lookup"><span data-stu-id="de161-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="de161-143">Este atributo tiene los mismos valores que el \_ atributo de modo MF VIDEODSP \_ (**\_ estabilización MFVideoDSPMode** y **MFVideoDSPMode \_ passthrough**).</span><span class="sxs-lookup"><span data-stu-id="de161-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="de161-144">Para obtener el valor de este atributo, las aplicaciones deben llamar a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) en el GUID **MFSampleExtension \_ VideoDSPMode**.</span><span class="sxs-lookup"><span data-stu-id="de161-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="de161-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de161-145">Remarks</span></span>

<span data-ttu-id="de161-146">Una instancia del DSP de estabilización de vídeo se puede crear de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="de161-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="de161-147">Llamando a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="de161-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="de161-148">El DSP de estabilización de vídeo se registra en la categoría de **\_ efecto de \_ vídeo \_ efecto de la categoría MFT** .</span><span class="sxs-lookup"><span data-stu-id="de161-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="de161-149">Llamando a la función de COM **CoCreateInstance** pasándole el CLSID CLSID **\_ CMSVideoDSPMFT**.</span><span class="sxs-lookup"><span data-stu-id="de161-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="de161-150">Para usar este método, debe incluir wmcodecdsp. h y vincular con wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="de161-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="de161-151">Además, el DSP de estabilización de vídeo admite la creación de instancias mediante Windows Runtime como una extensión de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="de161-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="de161-152">Se define en los [**efectos Windows. Media.**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)video, y su nombre completo es "Windows. Media. videoeffects. videoestabilization".</span><span class="sxs-lookup"><span data-stu-id="de161-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="de161-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de161-153">Requirements</span></span>



| <span data-ttu-id="de161-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="de161-154">Requirement</span></span> | <span data-ttu-id="de161-155">Value</span><span class="sxs-lookup"><span data-stu-id="de161-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de161-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de161-156">Header</span></span><br/> | <dl> <span data-ttu-id="de161-157"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="de161-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de161-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="de161-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de161-159">Procesadores de señal digital</span><span class="sxs-lookup"><span data-stu-id="de161-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="de161-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="de161-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
