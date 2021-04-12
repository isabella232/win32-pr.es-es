---
description: Enumeración de los tipos de audio para los modos de codificación específicos
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumeración de los tipos de audio para los modos de codificación específicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423536"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="89009-103">Enumeración de los tipos de audio para los modos de codificación específicos (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="89009-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="89009-104">Los tipos de medios de entrada y salida aceptados por el codificador de audio están muy estructurados.</span><span class="sxs-lookup"><span data-stu-id="89009-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="89009-105">Debe obtener los tipos de salida admitidos mediante una llamada al método **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="89009-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="89009-106">Después de obtener un tipo de salida, no debe modificarlo.</span><span class="sxs-lookup"><span data-stu-id="89009-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="89009-107">Si desea utilizar un modo de codificación que no sea un CBR de un paso, debe establecer el modo y, a continuación, enumerar los tipos de salida para ese modo. el codificador cambia los tipos de salida admitidos en función del conjunto de modos.</span><span class="sxs-lookup"><span data-stu-id="89009-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="89009-108">Las propiedades que controlan el modo de codificación son [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) y [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="89009-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="89009-109">Cuando el modo se establece en el codificador, debe enumerar y seleccionar un tipo de salida, y usarlo sin alteración, al igual que con CBR.</span><span class="sxs-lookup"><span data-stu-id="89009-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="89009-110">Identificar tipos VBR basados en calidad</span><span class="sxs-lookup"><span data-stu-id="89009-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="89009-111">El procedimiento para identificar tipos VBR basados en la calidad depende de si el codificador actúa como un objeto multimedia de DirectX (DMO) o actúa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="89009-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="89009-112">Para obtener información sobre cuándo un codificador actúa como DMO o MFT, consulte las páginas de referencia de códecs individuales en [objetos de códec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="89009-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="89009-113">Cuando un codificador de audio actúa como DMO y configura el codificador para usar VBR de un paso, enumera todos los tipos de salida admitidos.</span><span class="sxs-lookup"><span data-stu-id="89009-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="89009-114">Sin embargo, normalmente querrá seleccionar un tipo VBR de una sola fase basándose en el parámetro Quality.</span><span class="sxs-lookup"><span data-stu-id="89009-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="89009-115">El codificador coloca el valor de calidad de los tipos de salida VBR de una sola fase en el miembro **nAvgBytesPerSec** de la estructura **WAVEFORMATEX** señalada por el **tipo de \_ medio DMO \_ . pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="89009-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="89009-116">Este valor se almacena en el siguiente formato: 0x7FFFFFXX, donde XX es el valor de calidad (de 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="89009-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="89009-117">Por ejemplo, el valor **nAvgBytesPerSec** de 0x7FFFFF62 especifica el nivel de calidad 98 (0x62 = 98).</span><span class="sxs-lookup"><span data-stu-id="89009-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="89009-118">En el ejemplo siguiente se muestra cómo comprobar el nivel de calidad de un formato cuando el codificador actúa como DMO.</span><span class="sxs-lookup"><span data-stu-id="89009-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="89009-119">Cuando el codificador actúa como MFT y enumera un tipo de salida en una llamada a **GetAvailableOutputType**, puede consultar la MFT para la propiedad **\_ \_ \_ \_ VBRQUALITY enumerada más recientemente MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="89009-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="89009-120">El valor devuelto indica la calidad VBR del tipo de medio de salida devuelto más recientemente.</span><span class="sxs-lookup"><span data-stu-id="89009-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="89009-121">Después, puede usar ese valor para establecer la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificador.</span><span class="sxs-lookup"><span data-stu-id="89009-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="89009-122">Establecer restricciones de pico</span><span class="sxs-lookup"><span data-stu-id="89009-122">Setting Peak Constraints</span></span>

<span data-ttu-id="89009-123">En el caso de VBR basada en la calidad (un paso) y una VBR de dos pasos sin restricciones, no se requiere ninguna configuración adicional después de recuperar el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="89009-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="89009-124">Para usar VBR máxima restringida, recupere un tipo de salida con VBR habilitada y dos pasos establecidos.</span><span class="sxs-lookup"><span data-stu-id="89009-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="89009-125">Este tipo, sin modificación, describe la configuración de VBR no restringida.</span><span class="sxs-lookup"><span data-stu-id="89009-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="89009-126">Para establecer las restricciones de pico, establezca las propiedades [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) y [MFPKEY \_ Bmax](mfpkey-bmaxproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="89009-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89009-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89009-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89009-128">Configuración de la codificación de audio</span><span class="sxs-lookup"><span data-stu-id="89009-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="89009-129">Búsqueda de tipos de salida del codificador de audio</span><span class="sxs-lookup"><span data-stu-id="89009-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="89009-130">Uso de la codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="89009-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="89009-131">Usar la codificación VBR</span><span class="sxs-lookup"><span data-stu-id="89009-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



