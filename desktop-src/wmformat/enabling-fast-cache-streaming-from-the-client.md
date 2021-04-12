---
title: Habilitación del streaming de caché rápido desde el cliente
description: Habilitación del streaming de caché rápido desde el cliente
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- SDK de Windows Media Format, que permite el streaming de caché rápido
- SDK de Windows Media Format, streaming de caché rápido
- Advanced Systems Format (ASF), que permite el streaming de caché rápido
- ASF (formato de sistemas avanzados), habilitación del streaming de caché rápido
- Advanced Systems Format (ASF), streaming de caché rápido
- ASF (formato de sistemas avanzados), streaming de caché rápido
- flujos, habilitar el streaming de caché rápido
- Transmisión por secuencias de caché rápida, habilitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420258"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="8a446-111">Habilitación del streaming de caché rápido desde el cliente</span><span class="sxs-lookup"><span data-stu-id="8a446-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="8a446-112">Caché rápida es una tecnología de streaming en la que el servidor transmite el contenido de forma oportunista a una velocidad de bits más alta que la que se necesita para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8a446-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="8a446-113">Si el ancho de banda disponible es mayor que la velocidad de bits del contenido, las secuencias de caché rápidas tienen una velocidad mayor y almacenan en búfer el contenido.</span><span class="sxs-lookup"><span data-stu-id="8a446-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="8a446-114">Esto ayuda a reducir las interrupciones más adelante si la red se congestiona.</span><span class="sxs-lookup"><span data-stu-id="8a446-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="8a446-115">Si el ancho de banda de red es inferior a la velocidad de bits del contenido, la caché rápida almacena en búfer una parte de los datos antes de que se inicie la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8a446-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="8a446-116">La memoria caché rápida se recomienda para redes no confiables, como redes inalámbricas, o redes que experimentan grandes fluctuaciones en el tráfico de red, como los módems por cable.</span><span class="sxs-lookup"><span data-stu-id="8a446-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="8a446-117">También se recomienda para el contenido de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="8a446-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="8a446-118">Los requisitos de ancho de banda para el contenido de VBR no son constantes y la memoria caché rápida permite al lector almacenar en búfer la secuencia durante las partes de velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="8a446-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="8a446-119">La transmisión por secuencias de caché rápida solo se admite para el contenido a petición.</span><span class="sxs-lookup"><span data-stu-id="8a446-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="8a446-120">Además, el servidor debe estar configurado para usar el streaming de caché rápido.</span><span class="sxs-lookup"><span data-stu-id="8a446-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="8a446-121">Para habilitar la memoria caché rápida en el objeto lector, llame a los métodos [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) y [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="8a446-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="8a446-122">El primer método permite al lector almacenar en caché el contenido transmitido por secuencias.</span><span class="sxs-lookup"><span data-stu-id="8a446-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="8a446-123">El segundo habilita el uso de caché rápida en concreto.</span><span class="sxs-lookup"><span data-stu-id="8a446-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="8a446-124">Con esta configuración, el lector activará la caché rápida de forma predeterminada si el ancho de banda de red es significativamente mayor o menor que la velocidad de bits del contenido, y si el servidor lo admite.</span><span class="sxs-lookup"><span data-stu-id="8a446-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="8a446-125">El usuario también puede controlar si el objeto lector utiliza la memoria caché rápida agregando uno o varios de los siguientes modificadores a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8a446-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="8a446-126">Modificador</span><span class="sxs-lookup"><span data-stu-id="8a446-126">Modifier</span></span>         | <span data-ttu-id="8a446-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a446-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a446-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="8a446-128">WMCache</span></span>          | <span data-ttu-id="8a446-129">Si este modificador está presente, el valor ' 0 ' deshabilita explícitamente la memoria caché rápida, mientras que el valor ' 1 ' lo habilita explícitamente.</span><span class="sxs-lookup"><span data-stu-id="8a446-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="8a446-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="8a446-130">WMBitrate</span></span>        | <span data-ttu-id="8a446-131">Este modificador especifica la velocidad de bits máxima del servidor.</span><span class="sxs-lookup"><span data-stu-id="8a446-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="8a446-132">Este modificador se puede usar para restringir la memoria caché rápida a un determinado límite de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="8a446-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="8a446-133">Se omite este modificador si ya se ha establecido un ancho de banda de conexión explícita con una llamada a [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span><span class="sxs-lookup"><span data-stu-id="8a446-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="8a446-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="8a446-134">WMContentBitrate</span></span> | <span data-ttu-id="8a446-135">Este modificador especifica la velocidad de bits para el contenido.</span><span class="sxs-lookup"><span data-stu-id="8a446-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="8a446-136">El lector usa este modificador, si está presente, cuando selecciona secuencias desde un archivo de velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="8a446-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="8a446-137">Esto puede hacer que el lector reciba contenido de alta velocidad de bits a través de una conexión lenta, lo que resulta en tiempos de búfer y retrasos muy largos.</span><span class="sxs-lookup"><span data-stu-id="8a446-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="8a446-138">El modificador WMCache = 1 obliga al lector a usar el streaming de caché rápido, independientemente de la banda de red o la velocidad de bits del contenido y sin tener en consideración las llamadas anteriores a **SetEnableFastCache**.</span><span class="sxs-lookup"><span data-stu-id="8a446-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="8a446-139">Sin embargo, no invalida el valor **SetEnableContentCaching** en el lector; tampoco invalida la configuración del servidor.</span><span class="sxs-lookup"><span data-stu-id="8a446-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="8a446-140">Los modificadores de dirección URL tienen el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="8a446-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="8a446-141">¿ *dirección URL*? *modificador* = *valor* de</span><span class="sxs-lookup"><span data-stu-id="8a446-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="8a446-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8a446-142">For example:</span></span>

<span data-ttu-id="8a446-143">mms://MyServer/MyVideo.wmv? WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="8a446-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="8a446-144">Se puede especificar más de un modificador; Use una y comercial (&) para separarlos:</span><span class="sxs-lookup"><span data-stu-id="8a446-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="8a446-145">mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000</span><span class="sxs-lookup"><span data-stu-id="8a446-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




