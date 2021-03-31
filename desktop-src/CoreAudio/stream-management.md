---
description: Administración de flujos
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Administración de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153212"
---
# <a name="stream-management"></a><span data-ttu-id="d5535-103">Administración de flujos</span><span class="sxs-lookup"><span data-stu-id="d5535-103">Stream Management</span></span>

<span data-ttu-id="d5535-104">Después de enumerar los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en el sistema e identificar un dispositivo de representación o captura adecuado, la siguiente tarea para una aplicación cliente de audio es abrir una conexión con el dispositivo de extremo y administrar el flujo de datos de audio a través de esa conexión.</span><span class="sxs-lookup"><span data-stu-id="d5535-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="d5535-105">[WASAPI](wasapi.md) permite a los clientes crear y administrar secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="d5535-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="d5535-106">WASAPI implementa varias interfaces para proporcionar servicios de administración de secuencias a los clientes de audio.</span><span class="sxs-lookup"><span data-stu-id="d5535-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="d5535-107">La interfaz principal es [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="d5535-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="d5535-108">Un cliente obtiene la interfaz **IAudioClient** para un dispositivo de punto de conexión de audio llamando al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con el *IID* de parámetro establecido en **REFIID** IID \_ IAudioClient) en el objeto de extremo.</span><span class="sxs-lookup"><span data-stu-id="d5535-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="d5535-109">El cliente llama a los métodos de la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5535-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="d5535-110">Descubra qué formatos de audio admite el dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="d5535-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="d5535-111">Obtiene el tamaño del búfer del extremo.</span><span class="sxs-lookup"><span data-stu-id="d5535-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="d5535-112">Obtiene el formato de flujo y la latencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="d5535-113">Iniciar, detener y restablecer la secuencia que fluye a través del dispositivo de extremo.</span><span class="sxs-lookup"><span data-stu-id="d5535-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="d5535-114">Acceder a servicios de audio adicionales.</span><span class="sxs-lookup"><span data-stu-id="d5535-114">Access additional audio services.</span></span>

<span data-ttu-id="d5535-115">Para crear una secuencia, un cliente llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="d5535-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="d5535-116">A través de este método, el cliente especifica el formato de los datos de la secuencia, el tamaño del búfer del extremo y si la secuencia funciona en modo compartido o exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d5535-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="d5535-117">Los métodos restantes de la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se dividen en dos grupos:</span><span class="sxs-lookup"><span data-stu-id="d5535-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="d5535-118">Métodos a los que se puede llamar solo después de que [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)haya abierto la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="d5535-119">Métodos a los que se puede llamar en cualquier momento antes o después de la llamada de [**inicialización**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="d5535-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="d5535-120">Solo se puede llamar a los métodos siguientes después de la llamada a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span><span class="sxs-lookup"><span data-stu-id="d5535-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="d5535-121">**IAudioClient::GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="d5535-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="d5535-122">**IAudioClient::GetCurrentPadding**</span><span class="sxs-lookup"><span data-stu-id="d5535-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="d5535-123">**IAudioClient:: GetService**</span><span class="sxs-lookup"><span data-stu-id="d5535-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="d5535-124">**IAudioClient::GetStreamLatency**</span><span class="sxs-lookup"><span data-stu-id="d5535-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="d5535-125">**IAudioClient:: RESET**</span><span class="sxs-lookup"><span data-stu-id="d5535-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="d5535-126">**IAudioClient:: Start**</span><span class="sxs-lookup"><span data-stu-id="d5535-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="d5535-127">**IAudioClient:: Stop**</span><span class="sxs-lookup"><span data-stu-id="d5535-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="d5535-128">Se puede llamar a los métodos siguientes antes o después de la llamada a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :</span><span class="sxs-lookup"><span data-stu-id="d5535-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="d5535-129">**IAudioClient::GetDevicePeriod**</span><span class="sxs-lookup"><span data-stu-id="d5535-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="d5535-130">**IAudioClient::GetMixFormat**</span><span class="sxs-lookup"><span data-stu-id="d5535-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="d5535-131">**IAudioClient::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="d5535-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="d5535-132">Para tener acceso a los servicios de cliente de audio adicionales, el cliente llama al método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="d5535-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="d5535-133">A través de este método, el cliente puede obtener referencias a las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="d5535-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="d5535-134">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="d5535-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="d5535-135">Escribe los datos de representación en un búfer de punto de conexión de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="d5535-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="d5535-136">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="d5535-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="d5535-137">Lee los datos capturados de un búfer de extremo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="d5535-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="d5535-138">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="d5535-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="d5535-139">Se comunica con el administrador de sesiones de audio para configurar y administrar la sesión de audio que está asociada a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d5535-140">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="d5535-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="d5535-141">Controla el nivel de volumen de la sesión de audio que está asociada a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d5535-142">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="d5535-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="d5535-143">Controla los niveles de volumen de los canales individuales en la sesión de audio que está asociada a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="d5535-144">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="d5535-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="d5535-145">Supervisa la velocidad de flujo de datos y la posición de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="d5535-146">Además, los clientes de WASAPI que requieren la notificación de eventos relacionados con la sesión deben implementar la siguiente interfaz:</span><span class="sxs-lookup"><span data-stu-id="d5535-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="d5535-147">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="d5535-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="d5535-148">Para recibir notificaciones de eventos, el cliente pasa un puntero a su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) como parámetro de llamada.</span><span class="sxs-lookup"><span data-stu-id="d5535-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="d5535-149">Por último, un cliente puede usar una API de nivel superior para crear una secuencia de audio, pero también requiere acceso a los controles de sesión y a los controles de volumen de la sesión que contiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5535-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="d5535-150">Normalmente, una API de nivel superior no proporciona este acceso.</span><span class="sxs-lookup"><span data-stu-id="d5535-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="d5535-151">El cliente puede obtener los controles para una sesión determinada a través de la interfaz [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="d5535-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="d5535-152">Esta interfaz permite al cliente obtener las interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) y [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) para una sesión sin necesidad de que el cliente use la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para crear una secuencia y asignar la secuencia a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d5535-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="d5535-153">Un cliente obtiene la interfaz **IAudioSessionManager** para un dispositivo de punto de conexión de audio llamando al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con el *IID* de parámetro establecido en **REFIID** IID \_ IAudioSessionManager) en el objeto de extremo.</span><span class="sxs-lookup"><span data-stu-id="d5535-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="d5535-154">Las interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)y [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) se definen en el archivo de encabezado Audiopolicy. h.</span><span class="sxs-lookup"><span data-stu-id="d5535-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="d5535-155">Todas las demás interfaces WASAPI se definen en el archivo de encabezado Audioclient. h.</span><span class="sxs-lookup"><span data-stu-id="d5535-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="d5535-156">En las secciones siguientes se describe cómo usar WASAPI para administrar secuencias de audio:</span><span class="sxs-lookup"><span data-stu-id="d5535-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="d5535-157">Acerca de WASAPI</span><span class="sxs-lookup"><span data-stu-id="d5535-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="d5535-158">Representar una secuencia</span><span class="sxs-lookup"><span data-stu-id="d5535-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="d5535-159">Capturar una secuencia</span><span class="sxs-lookup"><span data-stu-id="d5535-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="d5535-160">Grabación de bucle invertido</span><span class="sxs-lookup"><span data-stu-id="d5535-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="d5535-161">Flujos de modo exclusivo</span><span class="sxs-lookup"><span data-stu-id="d5535-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="d5535-162">Recuperación de un error de Invalid-Device</span><span class="sxs-lookup"><span data-stu-id="d5535-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="d5535-163">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="d5535-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="d5535-164">Enrutamiento de flujos</span><span class="sxs-lookup"><span data-stu-id="d5535-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="d5535-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5535-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5535-166">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="d5535-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



