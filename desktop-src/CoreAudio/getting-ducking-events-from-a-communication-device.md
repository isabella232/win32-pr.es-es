---
description: Una aplicación multimedia que desea proporcionar una experiencia personalizada de pato debe escuchar las notificaciones de eventos cuando se abre o se cierra una secuencia de comunicación en el sistema.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtención de eventos de pato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538944"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="1e645-103">Obtención de eventos de pato</span><span class="sxs-lookup"><span data-stu-id="1e645-103">Getting Ducking Events</span></span>

<span data-ttu-id="1e645-104">Una aplicación multimedia que desea proporcionar una experiencia personalizada de pato debe escuchar las notificaciones de eventos cuando se abre o se cierra una secuencia de comunicación en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1e645-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="1e645-105">La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o DirectSound, que usan las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="1e645-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="1e645-106">Un cliente de WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="1e645-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="1e645-107">Para proporcionar una implementación personalizada, una aplicación multimedia necesita recibir notificaciones del sistema cuando una aplicación de comunicación inicia o finaliza una secuencia de comunicación.</span><span class="sxs-lookup"><span data-stu-id="1e645-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="1e645-108">La aplicación multimedia debe implementar la interfaz [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) y registrar la implementación con el sistema de audio.</span><span class="sxs-lookup"><span data-stu-id="1e645-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="1e645-109">Tras el registro correcto, la aplicación multimedia recibe notificaciones de eventos en forma de devoluciones de llamada a través de los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="1e645-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="1e645-110">Para obtener más información, consulte [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="1e645-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="1e645-111">Para enviar notificaciones de patos, el sistema de audio debe saber qué sesión de audio está escuchando los eventos de perdedor.</span><span class="sxs-lookup"><span data-stu-id="1e645-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="1e645-112">Cada sesión de audio se identifica de forma única con un GUID: identificador de instancia de sesión.</span><span class="sxs-lookup"><span data-stu-id="1e645-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="1e645-113">El administrador de sesión permite a una aplicación obtener información sobre la sesión, como el título de la sesión de audio, el estado de representación y el identificador de la instancia de sesión.</span><span class="sxs-lookup"><span data-stu-id="1e645-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="1e645-114">El identificador se puede recuperar mediante la interfaz de control de directivas, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span><span class="sxs-lookup"><span data-stu-id="1e645-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="1e645-115">En los pasos siguientes se resume el proceso de obtención del identificador de instancia de sesión de la aplicación multimedia:</span><span class="sxs-lookup"><span data-stu-id="1e645-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="1e645-116">Cree una instancia del enumerador de dispositivos y Úsela para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar la secuencia que no es de comunicación.</span><span class="sxs-lookup"><span data-stu-id="1e645-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="1e645-117">Active el administrador de sesión desde el punto de conexión del dispositivo y obtenga una referencia a la interfaz [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="1e645-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="1e645-118">Mediante el puntero [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenga una referencia a la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="1e645-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="1e645-119">Consulte el [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) de la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="1e645-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="1e645-120">Llame a [**IAudioSessionControl2:: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) y recupere una cadena que contenga el identificador de sesión para la sesión de audio actual.</span><span class="sxs-lookup"><span data-stu-id="1e645-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="1e645-121">Para obtener notificaciones de patos sobre las secuencias de comunicación, la aplicación multimedia llama a [**IAudioSessionManager2:: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span><span class="sxs-lookup"><span data-stu-id="1e645-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="1e645-122">La aplicación multimedia suministra su identificador de instancia de sesión al sistema de audio y un puntero a la implementación de [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="1e645-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="1e645-123">La aplicación ahora puede recibir notificaciones de eventos cuando se abre una secuencia en el dispositivo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="1e645-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="1e645-124">Para dejar de recibir notificaciones, la aplicación multimedia debe llamar a [**IAudioSessionManager2:: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span><span class="sxs-lookup"><span data-stu-id="1e645-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="1e645-125">En el código siguiente se muestra cómo se puede registrar una aplicación para obtener notificaciones de patos.</span><span class="sxs-lookup"><span data-stu-id="1e645-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="1e645-126">La clase CMediaPlayer se define en [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="1e645-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="1e645-127">En el ejemplo [DuckingMediaPlayer](duckingmediaplayer.md) se implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="1e645-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1e645-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e645-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e645-129">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="1e645-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="1e645-130">Experiencia predeterminada de los patos</span><span class="sxs-lookup"><span data-stu-id="1e645-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="1e645-131">Deshabilitación de la experiencia de patos predeterminada</span><span class="sxs-lookup"><span data-stu-id="1e645-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="1e645-132">Proporcionar un comportamiento personalizado de patos</span><span class="sxs-lookup"><span data-stu-id="1e645-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="1e645-133">Consideraciones de implementación para las notificaciones de patos</span><span class="sxs-lookup"><span data-stu-id="1e645-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



