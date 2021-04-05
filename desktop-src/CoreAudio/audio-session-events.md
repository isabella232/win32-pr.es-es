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
# <a name="audio-session-events"></a>Eventos de sesión de audio

Una aplicación que administra secuencias de audio en modo compartido puede registrarse para recibir notificaciones cuando se producen eventos de sesión. Como se explicó anteriormente, cada flujo pertenece a una [sesión de audio](audio-sessions.md). Un evento de sesión se inicia con un cambio en el estado de una sesión de audio.

Una aplicación cliente puede registrarse para recibir notificaciones de los siguientes tipos de eventos de sesión:

-   El nivel de volumen maestro o el estado de silencio de la submezcla de sesión ha cambiado.
-   El nivel de volumen de uno o más canales de la submezcla de la sesión ha cambiado.
-   La sesión se ha desconectado.
-   El estado de actividad de la sesión ha cambiado a activo, inactivo o expirado.
-   Se ha asignado un nuevo parámetro de agrupación a la sesión.
-   Ha cambiado una propiedad de interfaz de usuario de la sesión (icono o nombre para mostrar).

El cliente recibe notificaciones de estos eventos a través de los métodos en su implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . A diferencia de las otras interfaces de WASAPI, que se implementan mediante el módulo de sistema WASAPI, el cliente implementa **IAudioSessionEvents**. Los métodos de esta interfaz reciben devoluciones de llamada del módulo del sistema WASAPI cuando se producen eventos de sesión.

Para empezar a recibir notificaciones, el cliente llama al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar su interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Cuando el cliente ya no requiere notificaciones, llama al método [**IAudioSessionControl:: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) para eliminar el registro.

En el ejemplo de código siguiente se muestra una posible implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :


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



La clase CAudioSessionEvents del ejemplo de código anterior es una implementación de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Esta implementación concreta podría formar parte de una aplicación de consola que imprime información acerca de los eventos de sesión en una ventana del símbolo del sistema. Dado **que IAudioSessionEvents** se hereda [**de IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definición de clase contiene implementaciones de los métodos **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Los métodos públicos restantes en la definición de clase son específicos de la interfaz **IAudioSessionEvents** .

Es posible que algunos clientes no estén interesados en supervisar todos los tipos de eventos de sesión. En el ejemplo de código anterior, varios métodos de notificación de la clase CAudioSessionEvents no hacen nada. Por ejemplo, el método [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) no hace nada excepto para devolver el código de estado S \_ correcto. Esta aplicación no supervisa los volúmenes del canal porque no cambia los volúmenes del canal (llamando a los métodos de la interfaz [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) y no comparte la sesión con otras aplicaciones que podrían cambiar los volúmenes del canal.

Los únicos tres métodos de la clase CAudioSessionEvents que notifican al usuario los eventos de sesión son [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)y [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Por ejemplo, si el usuario ejecuta el programa de control de volumen del sistema, Sndvol, y usa el control de volumen en Sndvol para cambiar el nivel de volumen de la aplicación, `OnSimpleVolumeChanged` imprime inmediatamente el nuevo nivel de volumen.

Para ver un ejemplo de código que registra y anula el registro de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) de un cliente, consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesiones de audio](audio-sessions.md)
</dt> </dl>

 

 
