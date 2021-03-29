---
description: API de EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API de EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807562"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="71268-103">API de EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="71268-103">EndpointVolume API</span></span>

<span data-ttu-id="71268-104">La API de EndpointVolume permite a los clientes especializados controlar y supervisar los niveles de volumen de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="71268-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="71268-105">Un cliente obtiene las referencias a las interfaces de la API de EndpointVolume mediante la obtención de la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un dispositivo de punto de conexión de audio y la llamada al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .</span><span class="sxs-lookup"><span data-stu-id="71268-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="71268-106">El archivo de encabezado Endpointvolume. h define las interfaces de la API de EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="71268-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="71268-107">Las aplicaciones de audio que usan la [API MMDevice](mmdevice-api.md) y [WASAPI](wasapi.md) suelen usar la interfaz [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para controlar los niveles de volumen por sesión.</span><span class="sxs-lookup"><span data-stu-id="71268-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="71268-108">Solo dos tipos de aplicaciones de audio requieren el uso de la API de EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="71268-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="71268-109">Estos tipos de aplicaciones son:</span><span class="sxs-lookup"><span data-stu-id="71268-109">These application types are:</span></span>

-   <span data-ttu-id="71268-110">Las aplicaciones que administran los niveles de volumen maestro de los dispositivos de punto de conexión de audio, de forma similar al programa de control de volumen de Windows, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="71268-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="71268-111">Aplicaciones de audio profesional ("Audio Pro") que requieren acceso en modo exclusivo a los dispositivos de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="71268-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="71268-112">El uso inadecuado de la API de EndpointVolume puede interferir con la Directiva de audio de Windows e interrumpir la configuración del volumen del sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="71268-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="71268-113">Si un dispositivo de punto de conexión de audio implementa controles de volumen y silenciado de hardware, la API de EndpointVolume usa esos controles para administrar el volumen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71268-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="71268-114">De lo contrario, la API EndpointVolume implementa los controles del software de forma transparente en el cliente.</span><span class="sxs-lookup"><span data-stu-id="71268-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="71268-115">Si un dispositivo tiene controles de volumen y silenciado de hardware, los cambios realizados en el volumen del dispositivo y silenciar la configuración a través de la API de EndpointVolume afectan al nivel de volumen en modo compartido y en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="71268-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="71268-116">Si un dispositivo no tiene controles de silencio y volumen de hardware, los cambios realizados en el volumen de software y los controles de silencio a través de la API de EndpointVolume afectan al nivel de volumen en modo compartido, pero no en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="71268-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="71268-117">En el modo exclusivo, el cliente y el dispositivo intercambian datos de audio directamente, omitiendo los controles de software.</span><span class="sxs-lookup"><span data-stu-id="71268-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="71268-118">En el caso de las aplicaciones que deben administrar controles de volumen y silenciado de hardware, la API de EndpointVolume ofrece dos ventajas potenciales sobre la [API de DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="71268-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="71268-119">En primer lugar, varios dispositivos de adaptador de audio carecen de controles de volumen de hardware.</span><span class="sxs-lookup"><span data-stu-id="71268-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="71268-120">Si un dispositivo no tiene un control de volumen de hardware, la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de la API de EndpointVolume implementa automáticamente un control de volumen de software en el flujo hacia o desde ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71268-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="71268-121">Para un cliente de la API de EndpointVolume, el resultado es el mismo si el dispositivo o el software de la interfaz de la API de EndpointVolume implementan el control de volumen en el hardware.</span><span class="sxs-lookup"><span data-stu-id="71268-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="71268-122">En segundo lugar, incluso si el dispositivo adaptador implementa controles de volumen de hardware, una aplicación que use la API DeviceTopology para implementar un algoritmo de recorrido de topología podría no encontrar el control que está buscando.</span><span class="sxs-lookup"><span data-stu-id="71268-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="71268-123">Normalmente, este tipo de aplicación está diseñado para atravesar la topología de hardware de un dispositivo o un conjunto de dispositivos relacionados.</span><span class="sxs-lookup"><span data-stu-id="71268-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="71268-124">La aplicación corre un error si intenta atravesar la topología de un dispositivo para el que no se ha diseñado o probado específicamente.</span><span class="sxs-lookup"><span data-stu-id="71268-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="71268-125">Solo las aplicaciones especializadas que deben tener acceso a funciones de hardware que no sean controles de volumen y silencio requieren el uso de la API de DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="71268-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="71268-126">En el caso de las aplicaciones que requieren el control solo del nivel de volumen de una secuencia en modo exclusivo, la API EndpointVolume es más fácil de usar y funciona de forma confiable con una gama más amplia de dispositivos de hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="71268-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="71268-127">Para obtener ejemplos de código que usan las interfaces de la API de EndpointVolume, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="71268-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="71268-128">Controles de volumen de extremo</span><span class="sxs-lookup"><span data-stu-id="71268-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="71268-129">Medidores de pico</span><span class="sxs-lookup"><span data-stu-id="71268-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="71268-130">Para ver un ejemplo que usa la API de EndpointVolume, consulte [EndpointVolume](endpointvolume.md) en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="71268-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="71268-131">La API de EndpointVolume implementa las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="71268-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="71268-132">Interfaz</span><span class="sxs-lookup"><span data-stu-id="71268-132">Interface</span></span>                                                | <span data-ttu-id="71268-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="71268-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="71268-134">**IAudioEndpointVolume**</span><span class="sxs-lookup"><span data-stu-id="71268-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="71268-135">Representa los controles de volumen en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="71268-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="71268-136">**IAudioMeterInformation**</span><span class="sxs-lookup"><span data-stu-id="71268-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="71268-137">Representa un medidor de picos en la secuencia de audio hacia o desde un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="71268-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="71268-138">Además, los clientes de la API de EndpointVolume que requieren notificación de cambios de volumen y de silencio en los dispositivos de punto de conexión de audio deben implementar la siguiente interfaz.</span><span class="sxs-lookup"><span data-stu-id="71268-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="71268-139">Interfaz</span><span class="sxs-lookup"><span data-stu-id="71268-139">Interface</span></span>                                                            | <span data-ttu-id="71268-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="71268-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71268-141">**IAudioEndpointVolumeCallback**</span><span class="sxs-lookup"><span data-stu-id="71268-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="71268-142">Proporciona notificaciones cuando cambia el nivel de volumen o el estado de silenciación de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="71268-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="71268-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71268-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71268-144">Controles de volumen</span><span class="sxs-lookup"><span data-stu-id="71268-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="71268-145">**Interfaz IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="71268-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="71268-146">**IMMDevice:: Activate**</span><span class="sxs-lookup"><span data-stu-id="71268-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="71268-147">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="71268-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="71268-148">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="71268-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



