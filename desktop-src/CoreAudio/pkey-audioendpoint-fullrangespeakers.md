---
description: La \_ propiedad FullRangeSpeakers de AudioEndpoint de PKEY \_ especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de extremo de audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153408"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="f1908-103">PKEY \_ AudioEndpoint \_ FullRangeSpeakers</span><span class="sxs-lookup"><span data-stu-id="f1908-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="f1908-104">La **propiedad \_ \_ FullRangeSpeakers de AudioEndpoint de PKEY** especifica la máscara de configuración de canal para los altavoces de intervalo completo que están conectados al dispositivo de extremo de audio.</span><span class="sxs-lookup"><span data-stu-id="f1908-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="f1908-105">La máscara indica la configuración física de los altavoces de alcance completo y especifica la asignación de canales a esos altavoces.</span><span class="sxs-lookup"><span data-stu-id="f1908-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="f1908-106">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="f1908-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="f1908-107">El miembro **uintVal** de la estructura **PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="f1908-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="f1908-108">Un altavoz completo puede reproducir sonidos en todo el intervalo, desde graves hasta agudos.</span><span class="sxs-lookup"><span data-stu-id="f1908-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="f1908-109">Normalmente, los altavoces más grandes son de intervalo completo, pero los altavoces más pequeños son significativamente menos capaces de reproducir sonidos graves.</span><span class="sxs-lookup"><span data-stu-id="f1908-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="f1908-110">En Windows Vista, el motor de audio usa esta propiedad para administrar los niveles de graves en el flujo de salida de audio que reproduce el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="f1908-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="f1908-111">La máscara de configuración de canal para esta propiedad está en el mismo formato que la máscara de configuración de canal para la propiedad [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) .</span><span class="sxs-lookup"><span data-stu-id="f1908-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="f1908-112">Para obtener más información acerca de las máscaras de configuración de canal, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f1908-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="f1908-113">La descripción de la \_ propiedad de configuración de canal de audio KSPROPERTY \_ \_ en la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="f1908-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="f1908-114">Las notas del producto titulada "compatibilidad con controladores de audio para las configuraciones de altavoz de Home Theater" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="f1908-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="f1908-115">El sistema obtiene la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FullRangeSpeakers del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1908-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="f1908-116">El usuario especifica esta información a través del panel de control multimedia de Windows Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="f1908-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="f1908-117">Para obtener más información acerca de Mmsys.cpl, consulte la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="f1908-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="f1908-118">La máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FullRangeSpeakers de un dispositivo de punto de conexión de audio es un subconjunto de la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ PhysicalSpeakers del mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1908-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="f1908-119">Por ejemplo, si un dispositivo de punto de conexión de audio impulsa un conjunto de altavoces de sonido envolvente 5,1, la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ PHYSICALSPEAKERS es KSAUDIO \_ Speaker \_ 5POINT1.</span><span class="sxs-lookup"><span data-stu-id="f1908-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="f1908-120">Esta máscara indica la presencia de los oradores frontal-izquierdo, frontal-derecho, frontal, lateral y derecho, y un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="f1908-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="f1908-121">Si los altavoces delantero-izquierdo y delantero derecho son lo suficientemente grandes como para producir sonidos graves, pero no son los oradores más pequeños del centro y el lado del centro, la máscara de configuración de canal para la \_ propiedad PKEY AudioEndpoint \_ FULLRANGESPEAKERS es KSAUDIO \_ Speaker \_ estéreo, que indica solo los hablantes frontal y derecho.</span><span class="sxs-lookup"><span data-stu-id="f1908-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="f1908-122">Channel-Configuration masks KSAUDIO \_ Speaker \_ 5POINT1 y KSAUDIO \_ Speaker \_ estéreo se definen en el archivo de encabezado Ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="f1908-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1908-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1908-123">Requirements</span></span>



| <span data-ttu-id="f1908-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1908-124">Requirement</span></span> | <span data-ttu-id="f1908-125">Value</span><span class="sxs-lookup"><span data-stu-id="f1908-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1908-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1908-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1908-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1908-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f1908-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1908-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1908-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1908-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1908-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1908-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1908-131"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1908-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1908-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1908-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1908-133">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="f1908-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="f1908-134">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="f1908-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="f1908-135">**\_ \_ Propiedad PHYSICALSPEAKERS de PKEY AudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f1908-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




