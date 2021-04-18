---
description: Quality-Based codificación de velocidad de bits variable
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based codificación de velocidad de bits variable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696679"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="476b4-103">Quality-Based codificación de velocidad de bits variable</span><span class="sxs-lookup"><span data-stu-id="476b4-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="476b4-104">A diferencia de la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md) (CBR), donde el codificador se esfuerza por mantener una velocidad de bits determinada de los medios codificados, en el modo de velocidad de bits variable (VBR), el codificador se esfuerza por lograr la mejor calidad posible de los medios codificados.</span><span class="sxs-lookup"><span data-stu-id="476b4-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="476b4-105">La principal diferencia entre CBR y VBR es el tamaño de la ventana de búfer utilizada.</span><span class="sxs-lookup"><span data-stu-id="476b4-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="476b4-106">Las secuencias con codificación VBR suelen tener ventanas de búfer grandes en comparación con las secuencias con codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="476b4-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="476b4-107">La calidad del contenido codificado viene determinada por la cantidad de datos que se pierden cuando se comprime el contenido.</span><span class="sxs-lookup"><span data-stu-id="476b4-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="476b4-108">Muchos factores afectan a la pérdida de datos en el proceso de compresión; pero en general, cuanto más complejos sean los datos originales y mayor sea la razón de compresión, más detalles se perderán en el proceso de compresión.</span><span class="sxs-lookup"><span data-stu-id="476b4-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="476b4-109">En el modo VBR basado en la calidad, no se define una velocidad de bits o una ventana de búfer que el codificador debe seguir.</span><span class="sxs-lookup"><span data-stu-id="476b4-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="476b4-110">En su lugar, especifique un nivel de calidad para una secuencia de medios digitales en lugar de una velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="476b4-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="476b4-111">El codificador comprime el contenido para que todos los ejemplos sean de calidad comparable; Esto garantiza que la calidad sea coherente a lo largo de la duración de la reproducción, independientemente de los requisitos de búfer del flujo resultante.</span><span class="sxs-lookup"><span data-stu-id="476b4-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="476b4-112">La codificación VBR basada en la calidad tiende a crear grandes flujos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="476b4-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="476b4-113">En general, este tipo de codificación es adecuado para la reproducción local o las conexiones de red de ancho de banda alto (o descarga y reproducción).</span><span class="sxs-lookup"><span data-stu-id="476b4-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="476b4-114">Por ejemplo, puede escribir una aplicación para copiar canciones de archivos de CD a ASF en un equipo.</span><span class="sxs-lookup"><span data-stu-id="476b4-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="476b4-115">El uso de la codificación VBR basada en la calidad garantiza que todas las canciones copiadas tengan la misma calidad.</span><span class="sxs-lookup"><span data-stu-id="476b4-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="476b4-116">En esos casos, la calidad coherente proporcionará una mejor experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="476b4-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="476b4-117">La desventaja de la codificación VBR basada en la calidad es que no hay ninguna manera de conocer los requisitos de tamaño o ancho de banda de los medios codificados antes de la sesión de codificación, ya que el codificador utiliza un único paso de codificación.</span><span class="sxs-lookup"><span data-stu-id="476b4-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="476b4-118">Esto puede hacer que los archivos de codificación VBR basados en la calidad sean inadecuados para las circunstancias en las que la memoria o el ancho de banda están restringidos, como reproducir contenido en reproductores multimedia portátiles o streaming a través de una red de ancho de banda bajo.</span><span class="sxs-lookup"><span data-stu-id="476b4-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="476b4-119">Configuración del codificador para la codificación VBR Quality-Based</span><span class="sxs-lookup"><span data-stu-id="476b4-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="476b4-120">La configuración del codificador se establece a través de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="476b4-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="476b4-121">Estas propiedades se definen en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="476b4-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="476b4-122">Las propiedades de configuración deben establecerse en el codificador antes de negociar el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="476b4-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="476b4-123">Para obtener información sobre cómo establecer propiedades en el codificador, consulte [configuración del codificador](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="476b4-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="476b4-124">En la lista siguiente se muestran las propiedades que se deben establecer para este tipo de codificación:</span><span class="sxs-lookup"><span data-stu-id="476b4-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="476b4-125">Especifique el modo de codificación VBR estableciendo la propiedad **MFPKEY \_ VBRENABLED** en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="476b4-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="476b4-126">Establezca **MFPKEY \_ PASSESUSED** en 1 porque este modo VBR usa un paso de codificación.</span><span class="sxs-lookup"><span data-stu-id="476b4-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="476b4-127">Establezca el nivel de calidad deseado (de 0 a 100) mediante el establecimiento de la propiedad **\_ \_ VBRQUALITY deseada de MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="476b4-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="476b4-128">VBR basada en la calidad no codifica el contenido en ningún parámetro de búfer predefinido.</span><span class="sxs-lookup"><span data-stu-id="476b4-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="476b4-129">Este nivel de calidad que se mantendrá para todo el flujo, independientemente de los requisitos de velocidad de bits que resulten.</span><span class="sxs-lookup"><span data-stu-id="476b4-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="476b4-130">En el caso de las secuencias de vídeo, establezca la velocidad de bits promedio en un valor distinto de cero en el atributo [**MF \_ MT \_ AVG \_ bitrate**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio de salida del codificador.</span><span class="sxs-lookup"><span data-stu-id="476b4-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="476b4-131">La velocidad de bits precisa se actualiza una vez completada la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="476b4-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="476b4-132">En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="476b4-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="476b4-133">Esta función establece las propiedades de codificación de nivel de secuencia para CBR y VBR.</span><span class="sxs-lookup"><span data-stu-id="476b4-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="476b4-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="476b4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="476b4-135">Tipos de codificación ASF</span><span class="sxs-lookup"><span data-stu-id="476b4-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



