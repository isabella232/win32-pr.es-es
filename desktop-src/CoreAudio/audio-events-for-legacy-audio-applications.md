---
description: Eventos de audio para aplicaciones de audio heredadas
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Eventos de audio para aplicaciones de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153525"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Eventos de audio para aplicaciones de audio heredadas

Las API de audio heredadas como DirectSound, DirectShow y las funciones **waveOutXxx** permiten a las aplicaciones obtener y establecer los niveles de volumen de las secuencias de audio. Las aplicaciones pueden usar las capacidades de control de volumen en estas API para mostrar los controles deslizantes de volumen en las ventanas de la aplicación.

En Windows Vista, el programa de control de volumen del sistema, Sndvol, permite a los usuarios controlar los niveles de volumen de audio de las aplicaciones individuales. Los controles deslizantes de volumen que muestran las aplicaciones deben estar vinculados a los controles deslizantes de volumen correspondientes en Sndvol. Si un usuario ajusta el volumen de la aplicación a través de un control deslizante de volumen en una ventana de la aplicación, el control deslizante de volumen correspondiente en Sndvol se mueve inmediatamente para indicar el nuevo nivel de volumen. Por el contrario, si el usuario ajusta el volumen de la aplicación a través de Sndvol, los controles deslizantes de volumen de la ventana de la aplicación deben moverse para indicar el nuevo nivel de volumen.

En Windows Vista, Sndvol refleja inmediatamente los cambios de volumen que realiza una aplicación mediante llamadas al método **IDirectSoundBuffer:: SetVolume** o a la función **waveOutSetVolume** . Sin embargo, una API de audio heredada como DirectSound o las funciones de **waveOutXxx** no proporciona ningún medio para notificar a una aplicación cuando el usuario cambia el volumen de la aplicación a través de Sndvol. Si una aplicación muestra un control deslizante de volumen pero no recibe notificaciones de cambios de volumen, el control deslizante no podrá reflejar los cambios realizados por el usuario en Sndvol. Para implementar el comportamiento adecuado, el diseñador de aplicaciones debe compensar de algún modo la falta de notificaciones por parte de la API de audio heredada.

Una solución podría ser que la aplicación establezca un temporizador para recordar periódicamente que compruebe el nivel de volumen para ver si ha cambiado.

Una solución más elegante es que la aplicación use las capacidades de notificación de eventos de las API de audio principales. En concreto, la aplicación puede registrar una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para recibir devoluciones de llamada cuando se producen cambios de volumen u otros tipos de eventos de audio. Cuando el volumen cambia, la rutina de devolución de llamada de cambio por volumen puede actualizar inmediatamente el control deslizante de volumen de la aplicación para reflejar el cambio.

En el ejemplo de código siguiente se muestra cómo una aplicación se puede registrar para recibir notificaciones de cambios de volumen y otros eventos de audio:


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

-   *Flow*: la dirección del flujo de datos del [dispositivo de punto de conexión de audio](audio-endpoint-devices.md) (un valor de enumeración [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).
-   *rol*: el [rol de dispositivo](device-roles.md) actual del dispositivo de punto de conexión (un valor de enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *pAudioEvents*: puntero a un objeto (una instancia de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) que contiene un conjunto de rutinas de devolución de llamada implementadas por la aplicación.

El constructor proporciona los valores de flujo y de rol como parámetros de entrada para el método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) . El método crea un objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que encapsula el dispositivo de punto de conexión de audio con la dirección de flujo de datos y el rol de dispositivo especificados.

La aplicación implementa el objeto al que apunta *pAudioEvents*. (La implementación no se muestra en el ejemplo de código anterior. Para obtener un ejemplo de código que implementa una interfaz **IAudioSessionEvents** , vea [eventos de sesión de audio](audio-session-events.md)). Cada método de esta interfaz recibe notificaciones de un tipo determinado de evento de audio. Si la aplicación no está interesada en un tipo de evento determinado, el método para ese tipo de evento no debe hacer nada, pero devuelve S \_ correcto.

El método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) recibe notificaciones de cambios de volumen. Normalmente, este método actualiza el control deslizante de volumen de la aplicación.

En el ejemplo de código anterior, el constructor de la clase AudioVolumeEvents se registra para las notificaciones en la [sesión de audio](audio-sessions.md) específica del proceso identificada por el GUID del valor GUID de la sesión \_ . De forma predeterminada, las API de audio heredadas como DirectSound, DirectShow y las funciones **waveOutXxx** asignan sus flujos a esta sesión. Sin embargo, una aplicación DirectSound o DirectShow puede, opcionalmente, invalidar el comportamiento predeterminado y asignar sus secuencias a una sesión entre procesos o a una sesión identificada por un valor GUID distinto de GUID \_ null. (Actualmente no se proporciona ningún mecanismo para que una aplicación **waveOutXxx** invalide el comportamiento predeterminado de una manera similar). Para obtener un ejemplo de código de una aplicación de DirectShow con este comportamiento, vea [roles de dispositivo para aplicaciones de DirectShow](device-roles-for-directshow-applications.md). Para dar cabida a este tipo de aplicación, puede modificar el constructor en el ejemplo de código anterior para aceptar dos parámetros de entrada adicionales: un GUID de sesión y una marca para indicar si la sesión que se va a supervisar es una sesión de proceso cruzado o específica del proceso. Pase estos parámetros a la llamada al método [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) en el constructor.

Una vez que el constructor llama al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrarse para recibir notificaciones, la aplicación continúa recibiendo notificaciones solo mientras exista la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . El objeto AudioVolumeEvents del ejemplo de código anterior contiene referencias a estas interfaces hasta que se llama a su destructor. Este comportamiento garantiza que la aplicación seguirá recibiendo notificaciones durante el período de duración del objeto AudioVolumeEvents.

En lugar de seleccionar implícitamente un dispositivo de audio en función de su rol de dispositivo, una aplicación de DirectSound o multimedia de Windows heredada podría permitir al usuario seleccionar explícitamente un dispositivo de una lista de dispositivos disponibles que se identifican por sus nombres descriptivos. Para admitir este comportamiento, el ejemplo de código anterior debe modificarse para generar notificaciones de eventos de audio para el dispositivo seleccionado. Se requieren dos modificaciones. En primer lugar, cambie la definición del constructor para que acepte una [cadena de identificador de punto de conexión](endpoint-id-strings.md) como parámetro de entrada (en lugar de los parámetros Flow y role en el ejemplo de código). Esta cadena identifica el dispositivo de punto de conexión de audio que corresponde al dispositivo DirectSound o a un dispositivo de onda heredado seleccionado. En segundo lugar, reemplace la llamada al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) por una llamada al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . La llamada a **GetDevice** toma la cadena del identificador de punto de conexión como parámetro de entrada y crea una instancia del dispositivo de extremo que se identifica mediante la cadena.

La técnica para obtener la cadena de identificador de punto de conexión para un dispositivo DirectSound o un dispositivo de forma de onda heredada es la siguiente.

En primer lugar, durante la enumeración de dispositivos, DirectSound proporciona la cadena de identificador de punto de conexión para cada dispositivo enumerado. Para comenzar la enumeración de dispositivos, la aplicación pasa un puntero de función de devolución de llamada como parámetro de entrada a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** . La definición de la función de devolución de llamada es:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



En Windows Vista, el parámetro *lpcstrModule* apunta a la cadena de identificador de punto de conexión. (En versiones anteriores de Windows, incluidos Windows Server 2003, Windows XP y Windows 2000, el parámetro *lpcstrModule* apunta al nombre del módulo del controlador del dispositivo). El parámetro *lpcstrDescription* apunta a una cadena que contiene el nombre descriptivo del dispositivo. Para obtener más información acerca de la enumeración de dispositivos DirectSound, consulte la documentación de Windows SDK.

En segundo lugar, para obtener la cadena de identificador de punto de conexión para un dispositivo de onda de onda heredado, utilice la función **waveOutMessage** o **waveInMessage** para enviar un \_ mensaje DRV QUERYFUNCTIONINSTANCEID al controlador de dispositivo de onda. Para ver un ejemplo de código que muestra el uso de este mensaje, consulte [roles de dispositivo para aplicaciones multimedia heredadas de Windows](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



