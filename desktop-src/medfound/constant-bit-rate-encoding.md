---
description: Codificación de velocidad de bits constante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codificación de velocidad de bits constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000866"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="5088c-103">Codificación de velocidad de bits constante</span><span class="sxs-lookup"><span data-stu-id="5088c-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="5088c-104">En la codificación de velocidad de bits constante (CBR), el codificador conoce la velocidad de bits de los ejemplos de medios de salida y la ventana de búfer (parámetros de cubo de fugas) antes de que comience la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="5088c-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="5088c-105">El codificador usa el mismo número de bits para codificar cada segundo de ejemplo a lo largo de la duración del archivo a fin de lograr la velocidad de bits de destino de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="5088c-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="5088c-106">Esto limita la variación en el tamaño de los ejemplos de flujo.</span><span class="sxs-lookup"><span data-stu-id="5088c-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="5088c-107">Además, durante la sesión de codificación, la velocidad de bits no está exactamente en el valor especificado, pero permanece cerca de la velocidad de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="5088c-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="5088c-108">La codificación CBR es útil cuando desea saber la velocidad de bits o la duración aproximada de un archivo sin tener que analizar todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="5088c-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="5088c-109">Esto es necesario en los escenarios de transmisión por secuencias en directo en los que el contenido multimedia debe transmitirse a una velocidad de bits predecible y con un uso de ancho de banda coherente.</span><span class="sxs-lookup"><span data-stu-id="5088c-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="5088c-110">La desventaja de la codificación CBR es que la calidad del contenido codificado no será constante.</span><span class="sxs-lookup"><span data-stu-id="5088c-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="5088c-111">Dado que el contenido es más difícil de comprimir, las partes de un flujo CBR serán de menor calidad que otras.</span><span class="sxs-lookup"><span data-stu-id="5088c-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="5088c-112">Por ejemplo, una película típica tiene algunas escenas que son bastante estáticas y algunas escenas que están llenas de acción.</span><span class="sxs-lookup"><span data-stu-id="5088c-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="5088c-113">Si codifica una película con CBR, las escenas que son estáticas y, por lo tanto, son fáciles de codificar de forma eficaz, tendrán una mayor calidad que las escenas de acción, lo que habría requerido tamaños de ejemplo más altos para mantener la misma calidad.</span><span class="sxs-lookup"><span data-stu-id="5088c-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="5088c-114">En general, las variaciones en la calidad de un archivo CBR son más pronunciadas a velocidades de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="5088c-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="5088c-115">A velocidades de bits más altas, la calidad de un archivo con codificación CBR seguirá variando, pero los problemas de calidad serán menos perceptibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="5088c-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="5088c-116">Cuando se usa la codificación CBR, se debe establecer el ancho de banda tan alto como permita el escenario de entrega.</span><span class="sxs-lookup"><span data-stu-id="5088c-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="5088c-117">Opciones de configuración CBR</span><span class="sxs-lookup"><span data-stu-id="5088c-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="5088c-118">Configuración del depósito de fugas</span><span class="sxs-lookup"><span data-stu-id="5088c-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="5088c-119">Opciones de configuración CBR</span><span class="sxs-lookup"><span data-stu-id="5088c-119">CBR Configuration Settings</span></span>

<span data-ttu-id="5088c-120">Debe configurar un codificador especificando el tipo de codificación y los distintos valores específicos de la secuencia antes de la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="5088c-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="5088c-121">**Para configurar el codificador para la codificación CBR**</span><span class="sxs-lookup"><span data-stu-id="5088c-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="5088c-122">Especifique el modo de codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="5088c-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="5088c-123">De forma predeterminada, el codificador está configurado para usar codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="5088c-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="5088c-124">La configuración del codificador se establece a través de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5088c-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="5088c-125">Estas propiedades se definen en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="5088c-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="5088c-126">Puede especificar explícitamente este modo estableciendo la propiedad [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) en Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="5088c-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="5088c-127">Para obtener información sobre cómo establecer propiedades en los codificadores, vea [configurar el codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5088c-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="5088c-128">Elija la velocidad de bits de codificación.</span><span class="sxs-lookup"><span data-stu-id="5088c-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="5088c-129">Para la codificación CBR, debe saber la velocidad de bits en la que desea codificar el flujo antes de que se inicie la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="5088c-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="5088c-130">Debe establecer la velocidad de bits durante la configuración del codificador.</span><span class="sxs-lookup"><span data-stu-id="5088c-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="5088c-131">Para ello, mientras realiza la negociación de tipo de medio, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT AVG de \_ \_ velocidad**](mf-mt-avg-bitrate-attribute.md) de bits (para secuencias de vídeo) de los tipos de medios de salida disponibles y elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits de destino</span><span class="sxs-lookup"><span data-stu-id="5088c-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="5088c-132">Para obtener más información, vea [negociación de tipos multimedia en el codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5088c-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="5088c-133">En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="5088c-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="5088c-134">Esta función establece las propiedades de codificación de nivel de secuencia para CBR y VBR.</span><span class="sxs-lookup"><span data-stu-id="5088c-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="5088c-135">Configuración del depósito de fugas</span><span class="sxs-lookup"><span data-stu-id="5088c-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="5088c-136">En el caso de la codificación CBR, el promedio y los valores máximos del depósito de fugas de la secuencia son los mismos.</span><span class="sxs-lookup"><span data-stu-id="5088c-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="5088c-137">Para obtener más información acerca de estos parámetros, vea [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="5088c-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="5088c-138">Para codificar secuencias de audio con CBR, debe establecer los valores del depósito con fugas después de negociar el tipo de medio de salida en el codificador.</span><span class="sxs-lookup"><span data-stu-id="5088c-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="5088c-139">El codificador calcula la ventana del búfer internamente basándose en la velocidad de bits promedio establecida en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="5088c-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="5088c-140">Para establecer los valores del cubo con fugas, cree una matriz de DWORDs puede establecer los siguientes valores en la propiedad [**MFPKEY \_ ASFSTREAMSINK \_ corregida \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) en el almacén de propiedades del receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="5088c-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="5088c-141">Para obtener más información, vea [establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="5088c-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="5088c-142">Velocidad de bits media: obtiene la velocidad de bits media del tipo de medio de salida que se selecciona durante la negociación del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5088c-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="5088c-143">Use el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="5088c-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="5088c-144">Ventana de búfer: Consulte el codificador para la interfaz [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) y, a continuación, llame a [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).</span><span class="sxs-lookup"><span data-stu-id="5088c-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="5088c-145">Tamaño de búfer inicial: establézcalo en 0.</span><span class="sxs-lookup"><span data-stu-id="5088c-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5088c-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5088c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5088c-147">Tipos de codificación ASF</span><span class="sxs-lookup"><span data-stu-id="5088c-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="5088c-148">Tutorial: 1-pasar la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="5088c-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="5088c-149">Tutorial: escribir un archivo WMA con codificación CBR</span><span class="sxs-lookup"><span data-stu-id="5088c-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
