---
description: Trabajar con tipos de medios DMO
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: Trabajar con tipos de medios DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003339"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="04f0b-103">Trabajar con tipos de medios DMO</span><span class="sxs-lookup"><span data-stu-id="04f0b-103">Working with DMO Media Types</span></span>

<span data-ttu-id="04f0b-104">Los tipos de medios de entrada y salida utilizados por el códec DMOs se definen mediante la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="04f0b-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="04f0b-105">Esta estructura es idéntica a la de ambos [**\_ \_ tipos de medios de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), que se define en el SDK de Windows Media Format y el [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type), que se define en Microsoft DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="04f0b-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="04f0b-106">Dependiendo de la aplicación, puede usar variables definidas como cualquiera de estos tres tipos.</span><span class="sxs-lookup"><span data-stu-id="04f0b-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="04f0b-107">Es seguro convertir un puntero a una de las estructuras de tipo de medio como otro.</span><span class="sxs-lookup"><span data-stu-id="04f0b-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="04f0b-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="04f0b-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="04f0b-109">Los tipos de formato que usan los códecs generalmente se limitan a los descritos por las estructuras **VIDEOINFOHEADER** y **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="04f0b-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="04f0b-110">Para mayor comodidad, las constantes para estos tipos de formato se incluyen en el archivo de encabezado wmcodecconst. h.</span><span class="sxs-lookup"><span data-stu-id="04f0b-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="04f0b-111">Los nombres de constantes son WMCFORMAT \_ videoinfo y WMCFORMAT \_ WaveFormatEx, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="04f0b-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="04f0b-112">Los códecs de audio pueden trabajar con la estructura **WAVEFORMATEXTENSIBLE** en algunas circunstancias y deben usarlo en otras personas.</span><span class="sxs-lookup"><span data-stu-id="04f0b-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="04f0b-113">Sin embargo, el **\_ tipo de medios DMO \_ . FormatType** se establece en el mismo valor que para **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="04f0b-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="04f0b-114">Para obtener más información sobre el uso de **WAVEFORMATEXTENSIBLE**, consulte [uso de High-Definition audio](usinghighdefinitionaudio.md).</span><span class="sxs-lookup"><span data-stu-id="04f0b-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="04f0b-115">Debe incluir la estructura de tipo de formato utilizada como salida del codificador en cualquier contenedor que use para almacenar los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="04f0b-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="04f0b-116">Los descodificadores requieren la estructura de formato original para descomprimir el contenido.</span><span class="sxs-lookup"><span data-stu-id="04f0b-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="04f0b-117">Además de los miembros de la estructura, los tipos de vídeo y Windows Media Audio comprimidos requieren información de formato adicional, que se anexa a la estructura.</span><span class="sxs-lookup"><span data-stu-id="04f0b-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="04f0b-118">Para obtener más información, consulte [trabajar con audio](workingwithaudio.md) y [trabajar con vídeo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="04f0b-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="04f0b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04f0b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04f0b-120">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="04f0b-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
