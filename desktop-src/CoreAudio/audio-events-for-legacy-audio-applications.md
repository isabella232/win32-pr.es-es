---
description: Eventos de audio para aplicaciones de audio heredadas
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Eventos de audio para aplicaciones de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165149"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Eventos de audio para aplicaciones de audio heredadas

Las API de audio heredadas, como Direct Sound, DirectShow y las funciones **waveOutXxx,** permiten a las aplicaciones obtener y establecer los niveles de volumen de las secuencias de audio. Las aplicaciones pueden usar las funcionalidades de control de volumen de estas API para mostrar controles deslizantes de volumen en sus ventanas de aplicación.

En Windows Vista, el programa de control de volumen del sistema, Sndvol, permite a los usuarios controlar los niveles de volumen de audio para aplicaciones individuales. Los controles deslizantes de volumen que muestran las aplicaciones deben vincularse a los controles deslizantes de volumen correspondientes en Sndvol. Si un usuario ajusta el volumen de la aplicación a través de un control deslizante de volumen en una ventana de la aplicación, el control deslizante de volumen correspondiente en Sndvol se mueve inmediatamente para indicar el nuevo nivel de volumen. Por el contrario, si el usuario ajusta el volumen de la aplicación a través de Sndvol, los controles deslizantes del volumen de la ventana de la aplicación deben moverse para indicar el nuevo nivel de volumen.

En Windows Vista, Sndvol refleja inmediatamente los cambios de volumen que realiza una aplicación a través de llamadas al método **IDirectSoundBuffer::SetVolume** o a la función **waveOutSetVolume.** Sin embargo, una API de audio heredada como Direct Sound o las funciones **waveOutXxx** no proporciona ningún medio para notificar a una aplicación cuando el usuario cambia el volumen de la aplicación a través de Sndvol. Si una aplicación muestra un control deslizante de volumen pero no recibe notificaciones de cambios de volumen, el control deslizante no reflejará los cambios realizados por el usuario en Sndvol. Para implementar el comportamiento adecuado, el diseñador de aplicaciones debe compensar de algún modo la falta de notificaciones por parte de la API de audio heredada.

Una solución podría ser que la aplicación establezca un temporizador para recordarle periódicamente que compruebe el nivel de volumen para ver si ha cambiado.

Una solución más elegante es que la aplicación use las funcionalidades de notificación de eventos de las API de audio principales. En concreto, la aplicación puede registrar una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para recibir devoluciones de llamada cuando se producen cambios de volumen u otros tipos de eventos de audio. Cuando cambia el volumen, la rutina de devolución de llamada de cambio de volumen puede actualizar inmediatamente el control deslizante del volumen de la aplicación para reflejar el cambio.

En el ejemplo de código siguiente se muestra cómo se puede registrar una aplicación para recibir notificaciones de cambios de volumen y otros eventos de audio:


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



En el ejemplo de código anterior se implementa una clase denominada AudioVolumeEvents. Durante la inicialización del programa, la aplicación de audio habilita las notificaciones de eventos de audio mediante la creación de un objeto AudioVolumeEvents. El constructor de esta clase toma tres parámetros de entrada:

-   *flow:* la dirección del flujo de datos del dispositivo de punto de [conexión de audio](audio-endpoint-devices.md) (un valor de [**enumeración EDataFlow).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)
-   *role:* el rol de [dispositivo actual](device-roles.md) del dispositivo de punto de conexión (un valor [**de enumeración ERole).**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)
-   *pAudioEvents*: puntero a un objeto (una instancia de interfaz [**IAudioSessionEvents)**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) que contiene un conjunto de rutinas de devolución de llamada implementadas por la aplicación.

El constructor proporciona los valores de flujo y rol como parámetros de entrada al [**método IMMDeviceEnumerator::GetDefaultAudioEndpoint.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) El método crea un [**objeto IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que encapsula el dispositivo de punto de conexión de audio con la dirección de flujo de datos y el rol de dispositivo especificados.

La aplicación implementa el objeto al que apunta *pAudioEvents*. (La implementación no se muestra en el ejemplo de código anterior. Para obtener un ejemplo de código que implementa una **interfaz IAudioSessionEvents,** vea [Eventos de sesión de audio).](audio-session-events.md) Cada método de esta interfaz recibe notificaciones de un tipo determinado de evento de audio. Si la aplicación no está interesada en un tipo de evento determinado, el método para ese tipo de evento no debe hacer nada más que devolver S \_ OK.

El [**método IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) recibe notificaciones de cambios de volumen. Normalmente, este método actualiza el control deslizante del volumen de la aplicación.

En el ejemplo de código anterior, el constructor de la clase AudioVolumeEvents registra las notificaciones en la sesión de [audio](audio-sessions.md) específica del proceso identificada por el valor GUID de sesión \_ GUID NULL. De forma predeterminada, las API de audio heredadas, como DirectSound, DirectShow y las funciones **waveOutXxx,** asignan sus secuencias a esta sesión. Sin embargo, una aplicación Direct Sound o DirectShow puede, como opción, invalidar el comportamiento predeterminado y asignar sus secuencias a una sesión entre procesos o a una sesión identificada por un valor GUID distinto de GUID \_ NULL. (Actualmente no se proporciona ningún mecanismo para que una **aplicación waveOutXxx** invalide el comportamiento predeterminado de una manera similar). Para obtener un ejemplo de código de una aplicación DirectShow con este comportamiento, vea Roles de dispositivo [para DirectShow aplicaciones](device-roles-for-directshow-applications.md). Para dar cabida a este tipo de aplicación, puede modificar el constructor en el ejemplo de código anterior para aceptar dos parámetros de entrada adicionales: un GUID de sesión y una marca para indicar si la sesión que se va a supervisar es una sesión entre procesos o específica del proceso. Pase estos parámetros a la llamada al [**método IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) en el constructor.

Después de que el constructor llame al método [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrarse para recibir notificaciones, la aplicación sigue recibiendo notificaciones solo mientras exista la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) El objeto AudioVolumeEvents del ejemplo de código anterior contiene referencias a estas interfaces hasta que se llama a su destructor. Este comportamiento garantiza que la aplicación seguirá recibiendo notificaciones durante la vigencia del objeto AudioVolumeEvents.

En lugar de seleccionar implícitamente un dispositivo de audio en función de su rol de dispositivo, una aplicación multimedia Windows direct Sound o heredada podría permitir al usuario seleccionar explícitamente un dispositivo de una lista de dispositivos disponibles identificados por sus nombres descriptivos. Para admitir este comportamiento, se debe modificar el ejemplo de código anterior para generar notificaciones de eventos de audio para el dispositivo seleccionado. Se requieren dos modificaciones. En primer lugar, cambie [](endpoint-id-strings.md) la definición del constructor para aceptar una cadena de identificador de punto de conexión como parámetro de entrada (en lugar de los parámetros de flujo y rol en el ejemplo de código). Esta cadena identifica el dispositivo de punto de conexión de audio que corresponde al dispositivo Direct Sound o de forma de onda heredado seleccionado. En segundo lugar, reemplace la llamada al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) por una llamada al método [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) La **llamada GetDevice** toma la cadena de identificador de punto de conexión como parámetro de entrada y crea una instancia del dispositivo de punto de conexión identificado por la cadena.

La técnica para obtener la cadena de identificador de punto de conexión para un dispositivo Direct Sound o un dispositivo de forma de onda heredada es la siguiente.

En primer lugar, durante la enumeración de dispositivos, Direct Sound proporciona la cadena de identificador de punto de conexión para cada dispositivo enumerado. Para comenzar la enumeración de dispositivos, la aplicación pasa un puntero de función de devolución de llamada como parámetro de entrada a las funciones **DirectSoundCreate** o **DirectCaptureCaptureCreate.** La definición de la función de devolución de llamada es:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



En Windows Vista, el *parámetro lpcstrModule* apunta a la cadena de identificador de punto de conexión. (En versiones anteriores de Windows, incluidos Windows Server 2003, Windows XP y Windows 2000, el parámetro *lpcstrModule* apunta al nombre del módulo de controladores para el dispositivo). El *parámetro lpcstrDescription* apunta a una cadena que contiene el nombre descriptivo del dispositivo. Para más información sobre la enumeración de dispositivos Direct Sound, consulte la documentación Windows SDK.

En segundo lugar, para obtener la cadena de identificador de punto de conexión para un dispositivo de forma de onda heredada, use la función **waveOutMessage** o **waveInMessage** para enviar un mensaje \_ DRV QUERYFUNCTIONINSTANCEID al controlador de dispositivo de forma de onda. Para obtener un ejemplo de código que muestra el uso de este mensaje, vea Roles de dispositivo para aplicaciones [Windows multimedia heredadas.](device-roles-for-legacy-windows-multimedia-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



