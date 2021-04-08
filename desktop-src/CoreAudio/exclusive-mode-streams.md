---
description: Flujos de Exclusive-Mode
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Flujos de Exclusive-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7722dd3463346e976f30a77949f56026a2425624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000600"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="38bdf-103">Flujos de Exclusive-Mode</span><span class="sxs-lookup"><span data-stu-id="38bdf-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="38bdf-104">Como se explicó anteriormente, si una aplicación abre un flujo en modo exclusivo, la aplicación tiene el uso exclusivo del dispositivo de extremo de audio que reproduce o registra la secuencia.</span><span class="sxs-lookup"><span data-stu-id="38bdf-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="38bdf-105">En cambio, varias aplicaciones pueden compartir un dispositivo de punto de conexión de audio abriendo secuencias en modo compartido en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="38bdf-106">El acceso en modo exclusivo a un dispositivo de audio puede bloquear sonidos cruciales del sistema, impedir la interoperabilidad con otras aplicaciones y, de lo contrario, degradar la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="38bdf-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="38bdf-107">Para mitigar estos problemas, una aplicación con una secuencia de modo exclusivo renuncia normalmente al control del dispositivo de audio cuando la aplicación no es el proceso en primer plano o no está en streaming activamente.</span><span class="sxs-lookup"><span data-stu-id="38bdf-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="38bdf-108">La latencia de flujo es el retraso inherente a la ruta de acceso de datos que conecta el búfer de punto de conexión de una aplicación con un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="38bdf-109">En el caso de una secuencia de representación, la latencia es el retraso máximo desde el momento en que una aplicación escribe un ejemplo en un búfer de extremo hasta el momento en que se oye el ejemplo a través de los altavoces.</span><span class="sxs-lookup"><span data-stu-id="38bdf-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="38bdf-110">En el caso de una secuencia de captura, la latencia es el retraso máximo desde el momento en que un sonido entra en el micrófono hasta el momento en que una aplicación puede leer el ejemplo de ese sonido desde el búfer del extremo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="38bdf-111">Las aplicaciones que usan secuencias en modo exclusivo suelen hacerlo porque requieren latencias bajas en las rutas de acceso de datos entre los dispositivos de punto de conexión de audio y los subprocesos de la aplicación que tienen acceso a los búferes del extremo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="38bdf-112">Normalmente, estos subprocesos se ejecutan con una prioridad relativamente alta y se programan para ejecutarse a intervalos periódicos cercanos o iguales que el intervalo periódico que separa los pasos de procesamiento sucesivos por el hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="38bdf-113">Durante cada paso, el hardware de audio procesa los nuevos datos en los búferes del extremo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="38bdf-114">Para lograr las latencias de flujo más pequeñas, una aplicación puede requerir tanto hardware de audio especial como un sistema de equipo que está ligeramente cargado.</span><span class="sxs-lookup"><span data-stu-id="38bdf-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="38bdf-115">La conducción del hardware de audio más allá de los límites de tiempo o la carga del sistema con tareas de alta prioridad que compiten podría producir un problema en una secuencia de audio de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="38bdf-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="38bdf-116">Por ejemplo, para un flujo de representación, se puede producir un problema si la aplicación no puede escribir en un búfer de extremo antes de que el hardware de audio Lea el búfer, o si el hardware no puede leer el búfer antes de que se programe la reproducción del búfer.</span><span class="sxs-lookup"><span data-stu-id="38bdf-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="38bdf-117">Normalmente, una aplicación que está diseñada para ejecutarse en una amplia variedad de hardware de audio y en una amplia gama de sistemas debe relajar los requisitos de control de tiempo suficientes para evitar problemas en todos los entornos de destino.</span><span class="sxs-lookup"><span data-stu-id="38bdf-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="38bdf-118">Windows Vista tiene varias características para admitir aplicaciones que requieren secuencias de audio de baja latencia.</span><span class="sxs-lookup"><span data-stu-id="38bdf-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="38bdf-119">Como se describe en [componentes de audio de modo de usuario](user-mode-audio-components.md), las aplicaciones que realizan operaciones críticas en el tiempo pueden llamar a las funciones del servicio Programador de clases multimedia (MMCSS) para aumentar la prioridad del subproceso sin denegar los recursos de CPU a las aplicaciones de menor prioridad.</span><span class="sxs-lookup"><span data-stu-id="38bdf-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="38bdf-120">Además, el método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) admite una marca AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK que permite que el subproceso de servicio de búfer de una aplicación Programe su ejecución para que se produzca cuando un nuevo búfer esté disponible en el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="38bdf-121">Mediante el uso de estas características, un subproceso de aplicación puede reducir la incertidumbre sobre cuándo se ejecutará, lo que reduce el riesgo de problemas en una secuencia de audio de latencia baja.</span><span class="sxs-lookup"><span data-stu-id="38bdf-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="38bdf-122">Es probable que los controladores de los adaptadores de audio anteriores usen la interfaz de controlador de dispositivo (DDI) de WaveCyclic o WavePci, mientras que los controladores para los adaptadores de audio más recientes tienen más probabilidades de admitir la DDI WaveRT.</span><span class="sxs-lookup"><span data-stu-id="38bdf-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="38bdf-123">En el caso de las aplicaciones en modo exclusivo, los controladores de WaveRT pueden proporcionar un mejor rendimiento que los controladores WaveCyclic o WavePci, pero los controladores WaveRT requieren capacidades de hardware adicionales.</span><span class="sxs-lookup"><span data-stu-id="38bdf-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="38bdf-124">Estas funcionalidades incluyen la capacidad de compartir búferes de hardware directamente con las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38bdf-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="38bdf-125">Con el uso compartido directo, no se requiere la intervención del sistema para transferir datos entre una aplicación en modo exclusivo y el hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="38bdf-126">Por el contrario, los controladores WaveCyclic y WavePci son adecuados para los adaptadores de audio menos compatibles y más antiguos.</span><span class="sxs-lookup"><span data-stu-id="38bdf-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="38bdf-127">Estos adaptadores dependen del software del sistema para transportar bloques de datos (adjuntados a paquetes de solicitud de e/s de sistema o IRP) entre búferes de aplicación y búferes de hardware.</span><span class="sxs-lookup"><span data-stu-id="38bdf-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="38bdf-128">Además, los dispositivos de audio USB dependen del software del sistema para transportar datos entre búferes de aplicación y búferes de hardware.</span><span class="sxs-lookup"><span data-stu-id="38bdf-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="38bdf-129">Para mejorar el rendimiento de las aplicaciones en modo exclusivo que se conectan a los dispositivos de audio que se basan en el sistema para el transporte de datos, WASAPI aumenta automáticamente la prioridad de los subprocesos del sistema que transfieren datos entre las aplicaciones y el hardware.</span><span class="sxs-lookup"><span data-stu-id="38bdf-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="38bdf-130">WASAPI usa MMCSS para aumentar la prioridad del subproceso.</span><span class="sxs-lookup"><span data-stu-id="38bdf-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="38bdf-131">En Windows Vista, si un subproceso del sistema administra el transporte de datos para una secuencia de reproducción de audio de modo exclusivo con un formato PCM y un período de dispositivo inferior a 10 milisegundos, WASAPI asigna el nombre de tarea de MMCSS "audio de Pro" al subproceso.</span><span class="sxs-lookup"><span data-stu-id="38bdf-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="38bdf-132">Si el período del dispositivo de la secuencia es mayor o igual que 10 milisegundos, WASAPI asigna el nombre de la tarea MMCSS "audio" al subproceso.</span><span class="sxs-lookup"><span data-stu-id="38bdf-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="38bdf-133">Para obtener más información acerca de WaveCyclic, WavePci y WaveRT DDIs, consulte la documentación de DDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="38bdf-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="38bdf-134">Para obtener información sobre cómo seleccionar un período de dispositivo adecuado, consulte [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="38bdf-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="38bdf-135">Como se describe [en controles de volumen de sesión](session-volume-controls.md), [WASAPI](wasapi.md) proporciona las interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)y [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para controlar los niveles de volumen de las secuencias de audio en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="38bdf-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="38bdf-136">Sin embargo, los controles de estas interfaces no tienen ningún efecto en los flujos de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="38bdf-137">En su lugar, las aplicaciones que administran secuencias en modo exclusivo usan normalmente la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) en la [API EndpointVolume](endpointvolume-api.md) para controlar los niveles de volumen de esas secuencias.</span><span class="sxs-lookup"><span data-stu-id="38bdf-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="38bdf-138">Para obtener información sobre esta interfaz, consulte [controles de volumen de extremo](endpoint-volume-controls.md).</span><span class="sxs-lookup"><span data-stu-id="38bdf-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="38bdf-139">Para cada dispositivo de reproducción y dispositivo de captura en el sistema, el usuario puede controlar si el dispositivo se puede usar en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="38bdf-140">Si el usuario deshabilita el uso de modo exclusivo del dispositivo, el dispositivo se puede usar para reproducir o grabar únicamente flujos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="38bdf-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="38bdf-141">Si el usuario habilita el uso de modo exclusivo del dispositivo, el usuario también puede controlar si una solicitud de la aplicación para usar el dispositivo en modo exclusivo tendrá preferencia sobre el uso del dispositivo por parte de las aplicaciones que puedan estar reproduciendo o grabando flujos en modo compartido a través del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="38bdf-142">Si se habilita el adelantado, una solicitud de una aplicación para tomar el control exclusivo del dispositivo se realiza correctamente si el dispositivo no está actualmente en uso, o si el dispositivo se usa en modo compartido, pero se produce un error en la solicitud si otra aplicación ya tiene el control exclusivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="38bdf-143">Si el adelantamiento está deshabilitado, una solicitud de una aplicación para tomar el control exclusivo del dispositivo se realiza correctamente si el dispositivo no está actualmente en uso, pero se produce un error en la solicitud si el dispositivo ya se está usando en modo compartido o en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="38bdf-144">En Windows Vista, la configuración predeterminada para un dispositivo de punto de conexión de audio es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="38bdf-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="38bdf-145">El dispositivo se puede usar para reproducir o grabar flujos de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="38bdf-146">Una solicitud para usar un dispositivo para reproducir o grabar un flujo en modo exclusivo tiene preferencia sobre cualquier flujo en modo compartido que se esté reproduciendo o grabando a través del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="38bdf-147">**Para cambiar la configuración de modo exclusivo de un dispositivo de reproducción o grabación**</span><span class="sxs-lookup"><span data-stu-id="38bdf-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="38bdf-148">Haga clic con el botón derecho en el icono de altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccione **dispositivos de reproducción** o **dispositivos de grabación**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="38bdf-149">(Como alternativa, ejecute el panel de control multimedia de Windows, Mmsys.cpl, desde una ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="38bdf-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="38bdf-150">Para obtener más información, vea la sección Comentarios en las [constantes de estado de dispositivo \_ \_ XXX](device-state-xxx-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="38bdf-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="38bdf-151">Después de que aparezca la ventana de **sonido** , seleccione **reproducción** o **grabación**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="38bdf-152">A continuación, seleccione una entrada en la lista de nombres de dispositivo y haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="38bdf-153">Después de que aparezca la ventana **propiedades** , haga clic en **avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="38bdf-154">Para permitir que las aplicaciones usen el dispositivo en modo exclusivo, active la casilla **permitir que las aplicaciones tomen el control exclusivo de este dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="38bdf-155">Para deshabilitar el uso de modo exclusivo del dispositivo, desactive la casilla.</span><span class="sxs-lookup"><span data-stu-id="38bdf-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="38bdf-156">Si está habilitado el uso de modo exclusivo del dispositivo, puede especificar si se realizará correctamente una solicitud de control exclusivo del dispositivo si el dispositivo está reproduciendo o grabando flujos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="38bdf-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="38bdf-157">Para dar prioridad a las aplicaciones en modo exclusivo sobre las aplicaciones en modo compartido, active la casilla **asignar prioridad a las aplicaciones en modo exclusivo**.</span><span class="sxs-lookup"><span data-stu-id="38bdf-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="38bdf-158">Para denegar la prioridad de las aplicaciones en modo exclusivo sobre las aplicaciones en modo compartido, desactive la casilla.</span><span class="sxs-lookup"><span data-stu-id="38bdf-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="38bdf-159">En el ejemplo de código siguiente se muestra cómo reproducir una secuencia de audio de baja latencia en un dispositivo de representación de audio configurado para su uso en modo exclusivo:</span><span class="sxs-lookup"><span data-stu-id="38bdf-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    DWORD taskIndex = 0;
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="38bdf-160">En el ejemplo de código anterior, la función PlayExclusiveStream se ejecuta en el subproceso de la aplicación que presta servicio a los búferes del extremo mientras se reproduce una secuencia de representación.</span><span class="sxs-lookup"><span data-stu-id="38bdf-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="38bdf-161">La función toma un único parámetro, pMySource, que es un puntero a un objeto que pertenece a una clase definida por el cliente, MyAudioSource.</span><span class="sxs-lookup"><span data-stu-id="38bdf-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="38bdf-162">Esta clase tiene dos funciones miembro, LoadData y SetFormat, a las que se llama en el ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="38bdf-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="38bdf-163">MyAudioSource se describe en [la representación de una secuencia](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="38bdf-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="38bdf-164">La función PlayExclusiveStream llama a una función auxiliar, GetStreamFormat, que negocia con el dispositivo de representación predeterminado para determinar si el dispositivo admite un formato de flujo de modo exclusivo que sea adecuado para su uso por parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38bdf-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="38bdf-165">El código de la función GetStreamFormat no aparece en el ejemplo de código; Esto se debe a que los detalles de su implementación dependen por completo de los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38bdf-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="38bdf-166">Sin embargo, el funcionamiento de la función GetStreamFormat se puede describir simplemente: llama al método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) una o varias veces para determinar si el dispositivo admite un formato adecuado.</span><span class="sxs-lookup"><span data-stu-id="38bdf-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="38bdf-167">Los requisitos de la aplicación determinan qué formatos GetStreamFormat presenta al método **IsFormatSupported** y el orden en que los presenta.</span><span class="sxs-lookup"><span data-stu-id="38bdf-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="38bdf-168">Para obtener más información sobre **IsFormatSupported**, consulte [formatos de dispositivo](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="38bdf-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="38bdf-169">Después de la llamada a GetStreamFormat, la función PlayExclusiveStream llama al método [**IAudioClient:: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) para obtener el período de dispositivo mínimo admitido por el hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="38bdf-170">A continuación, la función llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para solicitar una duración del búfer igual al período mínimo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="38bdf-171">Si la llamada se realiza correctamente, el método **Initialize** asigna dos búferes de punto de conexión, cada uno de los cuales tiene una duración igual al período mínimo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="38bdf-172">Más adelante, cuando se inicie la ejecución de la secuencia de audio, la aplicación y el hardware de audio compartirán los dos búferes en "ping-pong", es decir, mientras la aplicación escribe en un búfer, el hardware lee desde el otro búfer.</span><span class="sxs-lookup"><span data-stu-id="38bdf-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="38bdf-173">Antes de iniciar la secuencia, la función PlayExclusiveStream hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="38bdf-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="38bdf-174">Crea y registra el controlador de eventos a través del cual recibirá notificaciones cuando los búferes estén listos para rellenarse.</span><span class="sxs-lookup"><span data-stu-id="38bdf-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="38bdf-175">Rellena el primer búfer con datos del origen de audio para reducir el retraso desde el momento en que la secuencia comienza a ejecutarse hasta que se oye el sonido inicial.</span><span class="sxs-lookup"><span data-stu-id="38bdf-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="38bdf-176">Llama a la función **AvSetMmThreadCharacteristics** para solicitar que MMCSS aumente la prioridad del subproceso en el que se ejecuta PlayExclusiveStream.</span><span class="sxs-lookup"><span data-stu-id="38bdf-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="38bdf-177">(Cuando la secuencia deja de ejecutarse, la llamada a la función **AvRevertMmThreadCharacteristics** restaura la prioridad de subproceso original).</span><span class="sxs-lookup"><span data-stu-id="38bdf-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="38bdf-178">Para obtener más información sobre **AvSetMmThreadCharacteristics** y **AvRevertMmThreadCharacteristics**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="38bdf-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="38bdf-179">Mientras se ejecuta la secuencia, cada iteración del bucle **While** en el ejemplo de código anterior rellena un búfer de extremo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="38bdf-180">Entre iteraciones, la llamada a la función **WaitForSingleObject** espera a que se señale el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="38bdf-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="38bdf-181">Cuando se señala el identificador, el cuerpo del bucle hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="38bdf-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="38bdf-182">Llama al método [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) para obtener el siguiente búfer.</span><span class="sxs-lookup"><span data-stu-id="38bdf-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="38bdf-183">Rellena el búfer.</span><span class="sxs-lookup"><span data-stu-id="38bdf-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="38bdf-184">Llama al método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) para liberar el búfer.</span><span class="sxs-lookup"><span data-stu-id="38bdf-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="38bdf-185">Para obtener más información acerca de **WaitForSingleObject**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="38bdf-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="38bdf-186">Si el adaptador de audio está controlado por un controlador WaveRT, la señalización del controlador de eventos está ligada a las notificaciones de transferencia DMA del hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="38bdf-187">Para un dispositivo de audio USB, o para un dispositivo de audio controlado por un controlador WaveCyclic o WavePci, la señalización del identificador de evento está asociada a las finalizaciones de las IRP que transfieren datos del búfer de aplicación al búfer de hardware.</span><span class="sxs-lookup"><span data-stu-id="38bdf-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="38bdf-188">El ejemplo de código anterior envía el hardware de audio y el sistema al equipo a sus límites de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="38bdf-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="38bdf-189">En primer lugar, para reducir la latencia de flujo, la aplicación programa el subproceso de mantenimiento del búfer para que use el período de dispositivo mínimo admitido por el hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="38bdf-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="38bdf-190">En segundo lugar, para asegurarse de que el subproceso se ejecuta de forma confiable dentro de cada período de dispositivo, la llamada de función **AvSetMmThreadCharacteristics** establece el parámetro TASKNAME en "Audio Pro", que es, en Windows Vista, el nombre de tarea predeterminado con la prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="38bdf-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="38bdf-191">Considere si los requisitos de tiempo de la aplicación pueden ser relajados sin poner en peligro su utilidad.</span><span class="sxs-lookup"><span data-stu-id="38bdf-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="38bdf-192">Por ejemplo, la aplicación podría programar su subproceso de mantenimiento de búfer para que use un período que sea mayor que el mínimo.</span><span class="sxs-lookup"><span data-stu-id="38bdf-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="38bdf-193">Un período más largo podría permitir de forma segura el uso de una prioridad de subproceso inferior.</span><span class="sxs-lookup"><span data-stu-id="38bdf-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38bdf-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38bdf-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38bdf-195">Administración de flujos</span><span class="sxs-lookup"><span data-stu-id="38bdf-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



