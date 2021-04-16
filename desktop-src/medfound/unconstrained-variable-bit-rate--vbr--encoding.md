---
description: Codificación de velocidad de bits variable sin restricciones
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codificación de velocidad de bits variable sin restricciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696866"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="5e3f3-103">Codificación de velocidad de bits variable sin restricciones</span><span class="sxs-lookup"><span data-stu-id="5e3f3-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="5e3f3-104">En el modo de codificación de velocidad de bits variable (VBR) sin restricciones, el contenido se codifica con la máxima calidad posible manteniendo una velocidad de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="5e3f3-105">La codificación VBR sin restricciones utiliza dos fases de codificación.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="5e3f3-106">Cuando se usa la codificación VBR sin restricciones, se especifica una velocidad de bits para la secuencia, tal y como se haría con la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f3-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="5e3f3-107">Sin embargo, el codificador usa este valor solo como la velocidad de bits promedio para el flujo y codificaciones para que la calidad sea lo más alta posible mientras se mantiene el promedio.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="5e3f3-108">Los ejemplos individuales generados por el codificador varían en tamaño sin ningún límite explícito de búfer.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="5e3f3-109">Sin embargo, la velocidad de bits media durante la sesión de codificación y la duración de la secuencia no debe ser superior al valor especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="5e3f3-110">La velocidad de bits real en cualquier punto de la secuencia codificada puede variar considerablemente respecto al valor medio.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="5e3f3-111">No se establece una ventana de búfer para la codificación VBR sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="5e3f3-112">En su lugar, el codificador calcula el tamaño de la ventana de búfer necesaria en función de los requisitos de los ejemplos codificados.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="5e3f3-113">Esto significa que no hay ningún límite en el tamaño de los ejemplos individuales de la secuencia, siempre que la velocidad de bits media sea menor o igual que el valor establecido.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="5e3f3-114">La ventaja de la codificación VBR no restringida es que el flujo comprimido tiene la máxima calidad posible y permanece dentro de un ancho de banda medio predecible.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="5e3f3-115">Úselo si necesita especificar un ancho de banda, pero se aceptan las fluctuaciones en torno al ancho de banda especificado. por ejemplo, para archivos locales o solo descarga.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="5e3f3-116">El inconveniente de este modo de codificación es que el codificador puede establecer la ventana del búfer en el valor que sea necesario después de la codificación, lo que no le permite controlar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="5e3f3-117">En la mayoría de los casos, si no le preocupa el tamaño del búfer o la coherencia del uso de ancho de banda, debe usar la [codificación de velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3f3-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="5e3f3-118">Configuración del codificador para VBR sin restricciones</span><span class="sxs-lookup"><span data-stu-id="5e3f3-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="5e3f3-119">La configuración del codificador se establece a través de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="5e3f3-120">Estas propiedades se definen en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="5e3f3-121">Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="5e3f3-122">Para obtener información sobre cómo establecer propiedades en el codificador, consulte [configuración del codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f3-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="5e3f3-123">En función de los valores de propiedad especificados, puede enumerar los tipos de salida VBR admitidos y seleccionar el que se requiera en la transformación del codificador [Media Foundation](media-foundation-transforms.md) (MFT) en función de la velocidad de bits media.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="5e3f3-124">En la lista siguiente se muestran las propiedades que se deben establecer para este tipo de codificación:</span><span class="sxs-lookup"><span data-stu-id="5e3f3-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="5e3f3-125">Especifique el modo de codificación VBR estableciendo la propiedad MFPKEY \_ VBRENABLED en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="5e3f3-126">Establezca MFPKEY \_ PASSESUSED en 2 porque el modo VBR sin restricciones utiliza dos fases de codificación.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="5e3f3-127">Mientras enumera el tipo de medio de salida, compruebe el atributo [**MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (en el caso de secuencias de audio) o el atributo [**MF \_ MT \_ AVG de velocidad de \_ bits**](mf-mt-avg-bitrate-attribute.md) (para secuencias de vídeo) de los tipos de medios de salida disponibles.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="5e3f3-128">Elija un tipo de medio de salida que tenga la velocidad de bits media más cercana a la velocidad de bits promedio deseada que desea que el codificador mantenga en el contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="5e3f3-129">Para obtener más información acerca de cómo seleccionar el tipo de medio de salida, consulte [negociación de tipo de medio en el codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f3-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="5e3f3-130">Para obtener el valor de la ventana de búfer establecido por el codificador, llame a **IWMCodecLeakyBucket:: GetBufferSizeBits**, definido en wmcodecifaces. h y wmcodecdspuuid. lib, después de la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="5e3f3-131">Para agregar compatibilidad con VBR no restringida para las secuencias, debe establecer este valor en el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valores de depósito de pérdida promedio) en el objeto de configuración de la secuencia mientras configura el perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="5e3f3-132">A continuación se modifica el método SetEncodingType de la clase de ejemplo CEncoder para configurar el modo VBR sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="5e3f3-133">Para obtener información sobre esta clase, vea [código de ejemplo del codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="5e3f3-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="5e3f3-134">Para obtener información sobre las macros auxiliares que se usan en este ejemplo, vea usar los ejemplos de código de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5e3f3-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="5e3f3-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e3f3-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e3f3-136">Tipos de codificación ASF</span><span class="sxs-lookup"><span data-stu-id="5e3f3-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="5e3f3-137">El modelo de búfer de depósito con fugas</span><span class="sxs-lookup"><span data-stu-id="5e3f3-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="5e3f3-138">Cómo crear una topología para Two-Pass la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="5e3f3-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



