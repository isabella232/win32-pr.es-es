---
description: Un usuario puede deshabilitar la experiencia predeterminada de la forma predeterminada que proporciona el sistema mediante las opciones que están disponibles en la pestaña comunicaciones del panel de control multimedia de Windows, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Deshabilitación de la experiencia de patos predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153521"
---
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="74cc9-103">Deshabilitación de la experiencia de patos predeterminada</span><span class="sxs-lookup"><span data-stu-id="74cc9-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="74cc9-104">Un usuario puede deshabilitar la [experiencia predeterminada](stream-attenuation.md) de la forma predeterminada que proporciona el sistema mediante las opciones que están disponibles en la pestaña **comunicaciones** del panel de control multimedia de Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="74cc9-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="74cc9-105">Cuando se aplica la pato, se usa un efecto de fundido y fundido para un período de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="74cc9-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="74cc9-106">Es posible que una aplicación de juego no quiera que la secuencia de comunicación interfiera con el audio del juego.</span><span class="sxs-lookup"><span data-stu-id="74cc9-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="74cc9-107">Es posible que algunas aplicaciones multimedia descubran que la experiencia de reproducción es discordante cuando la música se vuelve a atenuar.</span><span class="sxs-lookup"><span data-stu-id="74cc9-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="74cc9-108">Estos tipos de aplicaciones pueden optar por no participar en la experiencia de los patos.</span><span class="sxs-lookup"><span data-stu-id="74cc9-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="74cc9-109">Mediante programación, un cliente de WASAPI directo puede optar por usar el administrador de sesión para la sesión de audio que proporciona control de volumen para las secuencias que no son de comunicación.</span><span class="sxs-lookup"><span data-stu-id="74cc9-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="74cc9-110">Tenga en cuenta que, incluso si un cliente no se puede utilizar, sigue recibiendo notificaciones de patos del sistema.</span><span class="sxs-lookup"><span data-stu-id="74cc9-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="74cc9-111">Para no participar, el cliente debe obtener una referencia a la interfaz [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) del administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="74cc9-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="74cc9-112">Para no participar en la experiencia de los patos, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="74cc9-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="74cc9-113">Cree una instancia del enumerador de dispositivos y Úsela para obtener una referencia al punto de conexión del dispositivo que usa la aplicación multimedia para representar la secuencia que no es de comunicación.</span><span class="sxs-lookup"><span data-stu-id="74cc9-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="74cc9-114">Active el administrador de sesión desde el punto de conexión del dispositivo y obtenga una referencia a la interfaz [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) del administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="74cc9-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="74cc9-115">Mediante el puntero [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , obtenga una referencia a la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) del administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="74cc9-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="74cc9-116">Consulte el [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) de la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="74cc9-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="74cc9-117">Llame a [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) y pase **true** o **false** para especificar la preferencia de pato.</span><span class="sxs-lookup"><span data-stu-id="74cc9-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="74cc9-118">La preferencia especificada se puede cambiar dinámicamente durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="74cc9-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="74cc9-119">Tenga en cuenta que el cambio de cancelación no surte efecto hasta que la secuencia se detiene y se inicia de nuevo.</span><span class="sxs-lookup"><span data-stu-id="74cc9-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="74cc9-120">En el código siguiente se muestra cómo una aplicación puede especificar su preferencia de pato.</span><span class="sxs-lookup"><span data-stu-id="74cc9-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="74cc9-121">El autor de la llamada de la función debe pasar **true** o **false** en el parámetro DuckingOptOutChecked.</span><span class="sxs-lookup"><span data-stu-id="74cc9-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="74cc9-122">En función del valor que se pase, se habilitará o deshabilitará la función de pato a través de [**IAudioSessionControl2:: SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span><span class="sxs-lookup"><span data-stu-id="74cc9-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="74cc9-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74cc9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74cc9-124">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="74cc9-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="74cc9-125">Experiencia predeterminada de los patos</span><span class="sxs-lookup"><span data-stu-id="74cc9-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="74cc9-126">Proporcionar un comportamiento personalizado de patos</span><span class="sxs-lookup"><span data-stu-id="74cc9-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="74cc9-127">Consideraciones de implementación para las notificaciones de patos</span><span class="sxs-lookup"><span data-stu-id="74cc9-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="74cc9-128">Obtención de eventos de pato</span><span class="sxs-lookup"><span data-stu-id="74cc9-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



