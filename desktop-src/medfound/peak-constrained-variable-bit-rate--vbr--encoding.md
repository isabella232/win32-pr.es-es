---
description: 'En la velocidad de bits variable (VBR) restringida, el contenido se codifica en una velocidad de bits y valores máximos especificados: una velocidad de bits máxima y una ventana de búfer máximo.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained codificación de velocidad de bits variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715513"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="73b7d-103">Peak-Constrained codificación de velocidad de bits variable</span><span class="sxs-lookup"><span data-stu-id="73b7d-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="73b7d-104">En la velocidad de bits variable (VBR) restringida, el contenido se codifica en una velocidad de bits y *valores máximos* especificados: una velocidad de bits máxima y una ventana de búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="73b7d-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="73b7d-105">Estos valores máximos también se denominan los valores de los *depósitos máximos de fugas*.</span><span class="sxs-lookup"><span data-stu-id="73b7d-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="73b7d-106">El archivo está codificado para ajustarse a un búfer descrito por los valores máximos, de modo que la velocidad de bits media general de la secuencia sea igual o menor que el valor de velocidad de bits promedio especificado.</span><span class="sxs-lookup"><span data-stu-id="73b7d-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="73b7d-107">Normalmente, la velocidad de bits máxima es bastante alta.</span><span class="sxs-lookup"><span data-stu-id="73b7d-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="73b7d-108">El codificador garantiza que el valor de velocidad de bits promedio especificado se mantiene a lo largo de la duración de la secuencia (velocidad de bits media >= (tamaño de flujo total en bits/duración de flujo en segundos)).</span><span class="sxs-lookup"><span data-stu-id="73b7d-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="73b7d-109">Considere el ejemplo siguiente: configure una secuencia con una velocidad de bits media de 16.000 bits por segundo, una velocidad de bits máxima de 48.000 bits por segundo y una ventana de búfer máximo de 3.000 (3 segundos).</span><span class="sxs-lookup"><span data-stu-id="73b7d-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="73b7d-110">El tamaño del búfer usado para el flujo es de 144.000 bits (48.000 bits por segundo \* 3 segundos), según lo determinen los valores máximos.</span><span class="sxs-lookup"><span data-stu-id="73b7d-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="73b7d-111">El codificador comprime los datos para que se ajusten a ese búfer.</span><span class="sxs-lookup"><span data-stu-id="73b7d-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="73b7d-112">Además, la velocidad de bits media de la secuencia debe ser de 16.000 o inferior.</span><span class="sxs-lookup"><span data-stu-id="73b7d-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="73b7d-113">Si el codificador debe crear ejemplos grandes para controlar un segmento complejo de contenido, puede aprovechar el tamaño de búfer grande.</span><span class="sxs-lookup"><span data-stu-id="73b7d-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="73b7d-114">Sin embargo, otras partes de la secuencia deben codificarse a una velocidad de bits más baja para reducir el promedio hasta el nivel especificado.</span><span class="sxs-lookup"><span data-stu-id="73b7d-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="73b7d-115">La codificación VBR máxima limitada es útil para dispositivos de reproducción con una capacidad de búfer finita y restricciones de velocidad de datos.</span><span class="sxs-lookup"><span data-stu-id="73b7d-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="73b7d-116">Un ejemplo común es la codificación que se usa para DVDs cuando la descodificación se realiza mediante un chip de un dispositivo, donde hay limitaciones de hardware que deben tenerse en cuenta.</span><span class="sxs-lookup"><span data-stu-id="73b7d-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="73b7d-117">Configuración del codificador para Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="73b7d-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="73b7d-118">La VBR máxima restringida es como [VBR no restringida](unconstrained-variable-bit-rate--vbr--encoding.md) , ya que se limita a una velocidad de bits promedio a lo largo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="73b7d-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="73b7d-119">Además, la VBR máxima restringida se ajusta a un búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="73b7d-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="73b7d-120">Este búfer se describe con una velocidad de bits máxima y una ventana de búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="73b7d-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="73b7d-121">Este modo utiliza dos fases de codificación y proporciona la flexibilidad del codificador en cómo codifica los ejemplos individuales al tiempo que se respetan las limitaciones máximas.</span><span class="sxs-lookup"><span data-stu-id="73b7d-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="73b7d-122">La configuración del codificador se establece a través de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="73b7d-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="73b7d-123">Estas propiedades se definen en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="73b7d-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="73b7d-124">Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="73b7d-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="73b7d-125">Para obtener información sobre cómo establecer propiedades en el codificador, consulte [configuración del codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="73b7d-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="73b7d-126">En función de los valores de propiedad especificados, puede enumerar los tipos de salida VBR admitidos y seleccionar el que se requiera en la transformación del codificador [Media Foundation](media-foundation-transforms.md) (MFT) en función de la velocidad de bits media.</span><span class="sxs-lookup"><span data-stu-id="73b7d-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="73b7d-127">Debe establecer el siguiente valor de propertiesfor en este tipo de codificación:</span><span class="sxs-lookup"><span data-stu-id="73b7d-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="73b7d-128">Especifique el modo de codificación VBR estableciendo la propiedad MFPKEY \_ VBRENABLED en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="73b7d-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="73b7d-129">Establezca MFPKEY \_ PASSESUSED en 2 porque el modo VBR restringido de pico utiliza dos fases de codificación.</span><span class="sxs-lookup"><span data-stu-id="73b7d-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="73b7d-130">Establezca MFPKEY \_ RMAX para especificar la velocidad de bits máxima y establezca MFPKEY \_ Bmax para especificar la ventana de búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="73b7d-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="73b7d-131">Durante la enumeración del tipo de medio de salida, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT \_ AVG \_**](mf-mt-avg-bitrate-attribute.md) Rate (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits promedio deseada que desea que el</span><span class="sxs-lookup"><span data-stu-id="73b7d-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="73b7d-132">Para obtener más información acerca de cómo seleccionar el tipo de medio de salida, consulte [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="73b7d-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="73b7d-133">Se recomienda establecer la velocidad de bits máxima en al menos dos veces la velocidad de bits promedio.</span><span class="sxs-lookup"><span data-stu-id="73b7d-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="73b7d-134">Si se establece la tasa máxima en un valor inferior, el codificador puede codificar el contenido como CBR de dos pasos en lugar de VBR limitada.</span><span class="sxs-lookup"><span data-stu-id="73b7d-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="73b7d-135">Para obtener el valor de la ventana de búfer establecido por el codificador, llame a **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido en wmcodecifaces. h, wmcodecdspuuid. lib, después de la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="73b7d-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="73b7d-136">Para agregar compatibilidad con VBR no restringida para las secuencias, debe establecer este valor en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valores de cubo con fugas máximas) en el objeto de configuración de la secuencia mientras configura el perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="73b7d-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="73b7d-137">En el ejemplo de código siguiente se modifica el método SetEncodingType de la clase de ejemplo CEncoder para configurar el modo VBR con restricción máxima.</span><span class="sxs-lookup"><span data-stu-id="73b7d-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="73b7d-138">Para obtener información sobre esta clase, vea [código de ejemplo del codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="73b7d-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="73b7d-139">Para obtener información sobre las macros auxiliares que se usan en este ejemplo, vea usar los ejemplos de código de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="73b7d-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="73b7d-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73b7d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73b7d-141">Tipos de codificación ASF</span><span class="sxs-lookup"><span data-stu-id="73b7d-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="73b7d-142">El modelo de búfer de depósito con fugas</span><span class="sxs-lookup"><span data-stu-id="73b7d-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="73b7d-143">Cómo crear una topología para Two-Pass la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="73b7d-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



