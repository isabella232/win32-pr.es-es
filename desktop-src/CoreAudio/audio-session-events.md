---
description: Eventos de sesión de audio
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Eventos de sesión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000604"
---
# <a name="audio-session-events"></a><span data-ttu-id="0bb3d-103">Eventos de sesión de audio</span><span class="sxs-lookup"><span data-stu-id="0bb3d-103">Audio Session Events</span></span>

<span data-ttu-id="0bb3d-104">Una aplicación que administra secuencias de audio en modo compartido puede registrarse para recibir notificaciones cuando se producen eventos de sesión.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="0bb3d-105">Como se explicó anteriormente, cada flujo pertenece a una [sesión de audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="0bb3d-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="0bb3d-106">Un evento de sesión se inicia con un cambio en el estado de una sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="0bb3d-107">Una aplicación cliente puede registrarse para recibir notificaciones de los siguientes tipos de eventos de sesión:</span><span class="sxs-lookup"><span data-stu-id="0bb3d-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="0bb3d-108">El nivel de volumen maestro o el estado de silencio de la submezcla de sesión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="0bb3d-109">El nivel de volumen de uno o más canales de la submezcla de la sesión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="0bb3d-110">La sesión se ha desconectado.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="0bb3d-111">El estado de actividad de la sesión ha cambiado a activo, inactivo o expirado.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="0bb3d-112">Se ha asignado un nuevo parámetro de agrupación a la sesión.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="0bb3d-113">Ha cambiado una propiedad de interfaz de usuario de la sesión (icono o nombre para mostrar).</span><span class="sxs-lookup"><span data-stu-id="0bb3d-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="0bb3d-114">El cliente recibe notificaciones de estos eventos a través de los métodos en su implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="0bb3d-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="0bb3d-115">A diferencia de las otras interfaces de WASAPI, que se implementan mediante el módulo de sistema WASAPI, el cliente implementa **IAudioSessionEvents**.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="0bb3d-116">Los métodos de esta interfaz reciben devoluciones de llamada del módulo del sistema WASAPI cuando se producen eventos de sesión.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="0bb3d-117">Para empezar a recibir notificaciones, el cliente llama al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="0bb3d-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="0bb3d-118">Cuando el cliente ya no requiere notificaciones, llama al método [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) para eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="0bb3d-119">En el ejemplo de código siguiente se muestra una posible implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :</span><span class="sxs-lookup"><span data-stu-id="0bb3d-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="0bb3d-120">La clase CAudioSessionEvents del ejemplo de código anterior es una implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="0bb3d-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="0bb3d-121">Esta implementación concreta podría formar parte de una aplicación de consola que imprime información acerca de los eventos de sesión en una ventana del símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="0bb3d-122">Dado **que IAudioSessionEvents** se hereda [**de IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definición de clase contiene implementaciones de los métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="0bb3d-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="0bb3d-123">Los métodos públicos restantes en la definición de clase son específicos de la interfaz **IAudioSessionEvents** .</span><span class="sxs-lookup"><span data-stu-id="0bb3d-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="0bb3d-124">Es posible que algunos clientes no estén interesados en supervisar todos los tipos de eventos de sesión.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="0bb3d-125">En el ejemplo de código anterior, varios métodos de notificación de la clase CAudioSessionEvents no hacen nada.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="0bb3d-126">Por ejemplo, el método [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) no hace nada excepto para devolver el código de estado S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="0bb3d-127">Esta aplicación no supervisa los volúmenes del canal porque no cambia los volúmenes del canal (llamando a los métodos de la interfaz [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) y no comparte la sesión con otras aplicaciones que podrían cambiar los volúmenes del canal.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="0bb3d-128">Los únicos tres métodos de la clase CAudioSessionEvents que notifican al usuario los eventos de sesión son [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)y [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="0bb3d-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="0bb3d-129">Por ejemplo, si el usuario ejecuta el programa de control de volumen del sistema, Sndvol, y usa el control de volumen en Sndvol para cambiar el nivel de volumen de la aplicación, `OnSimpleVolumeChanged` imprime inmediatamente el nuevo nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="0bb3d-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="0bb3d-130">Para ver un ejemplo de código que registra y anula el registro de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) de un cliente, consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0bb3d-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bb3d-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb3d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bb3d-132">Sesiones de audio</span><span class="sxs-lookup"><span data-stu-id="0bb3d-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
