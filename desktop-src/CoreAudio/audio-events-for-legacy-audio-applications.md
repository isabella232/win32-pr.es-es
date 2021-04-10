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
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="4d520-103">Eventos de audio para aplicaciones de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="4d520-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="4d520-104">Las API de audio heredadas como DirectSound, DirectShow y las funciones **waveOutXxx** permiten a las aplicaciones obtener y establecer los niveles de volumen de las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="4d520-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="4d520-105">Las aplicaciones pueden usar las capacidades de control de volumen en estas API para mostrar los controles deslizantes de volumen en las ventanas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d520-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="4d520-106">En Windows Vista, el programa de control de volumen del sistema, Sndvol, permite a los usuarios controlar los niveles de volumen de audio de las aplicaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="4d520-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="4d520-107">Los controles deslizantes de volumen que muestran las aplicaciones deben estar vinculados a los controles deslizantes de volumen correspondientes en Sndvol.</span><span class="sxs-lookup"><span data-stu-id="4d520-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="4d520-108">Si un usuario ajusta el volumen de la aplicación a través de un control deslizante de volumen en una ventana de la aplicación, el control deslizante de volumen correspondiente en Sndvol se mueve inmediatamente para indicar el nuevo nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="4d520-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="4d520-109">Por el contrario, si el usuario ajusta el volumen de la aplicación a través de Sndvol, los controles deslizantes de volumen de la ventana de la aplicación deben moverse para indicar el nuevo nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="4d520-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="4d520-110">En Windows Vista, Sndvol refleja inmediatamente los cambios de volumen que realiza una aplicación mediante llamadas al método **IDirectSoundBuffer:: SetVolume** o a la función **waveOutSetVolume** .</span><span class="sxs-lookup"><span data-stu-id="4d520-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="4d520-111">Sin embargo, una API de audio heredada como DirectSound o las funciones de **waveOutXxx** no proporciona ningún medio para notificar a una aplicación cuando el usuario cambia el volumen de la aplicación a través de Sndvol.</span><span class="sxs-lookup"><span data-stu-id="4d520-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="4d520-112">Si una aplicación muestra un control deslizante de volumen pero no recibe notificaciones de cambios de volumen, el control deslizante no podrá reflejar los cambios realizados por el usuario en Sndvol.</span><span class="sxs-lookup"><span data-stu-id="4d520-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="4d520-113">Para implementar el comportamiento adecuado, el diseñador de aplicaciones debe compensar de algún modo la falta de notificaciones por parte de la API de audio heredada.</span><span class="sxs-lookup"><span data-stu-id="4d520-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="4d520-114">Una solución podría ser que la aplicación establezca un temporizador para recordar periódicamente que compruebe el nivel de volumen para ver si ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4d520-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="4d520-115">Una solución más elegante es que la aplicación use las capacidades de notificación de eventos de las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="4d520-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="4d520-116">En concreto, la aplicación puede registrar una interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para recibir devoluciones de llamada cuando se producen cambios de volumen u otros tipos de eventos de audio.</span><span class="sxs-lookup"><span data-stu-id="4d520-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="4d520-117">Cuando el volumen cambia, la rutina de devolución de llamada de cambio por volumen puede actualizar inmediatamente el control deslizante de volumen de la aplicación para reflejar el cambio.</span><span class="sxs-lookup"><span data-stu-id="4d520-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="4d520-118">En el ejemplo de código siguiente se muestra cómo una aplicación se puede registrar para recibir notificaciones de cambios de volumen y otros eventos de audio:</span><span class="sxs-lookup"><span data-stu-id="4d520-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


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



<span data-ttu-id="4d520-119">En el ejemplo de código anterior se implementa una clase denominada AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="4d520-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="4d520-120">Durante la inicialización del programa, la aplicación de audio habilita las notificaciones de eventos de audio mediante la creación de un objeto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="4d520-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="4d520-121">El constructor de esta clase toma tres parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="4d520-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="4d520-122">*Flow*: la dirección del flujo de datos del [dispositivo de punto de conexión de audio](audio-endpoint-devices.md) (un valor de enumeración [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).</span><span class="sxs-lookup"><span data-stu-id="4d520-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="4d520-123">*rol*: el [rol de dispositivo](device-roles.md) actual del dispositivo de punto de conexión (un valor de enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="4d520-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="4d520-124">*pAudioEvents*: puntero a un objeto (una instancia de la interfaz [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) que contiene un conjunto de rutinas de devolución de llamada implementadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d520-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="4d520-125">El constructor proporciona los valores de flujo y de rol como parámetros de entrada para el método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) .</span><span class="sxs-lookup"><span data-stu-id="4d520-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="4d520-126">El método crea un objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) que encapsula el dispositivo de punto de conexión de audio con la dirección de flujo de datos y el rol de dispositivo especificados.</span><span class="sxs-lookup"><span data-stu-id="4d520-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="4d520-127">La aplicación implementa el objeto al que apunta *pAudioEvents*.</span><span class="sxs-lookup"><span data-stu-id="4d520-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="4d520-128">(La implementación no se muestra en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="4d520-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="4d520-129">Para obtener un ejemplo de código que implementa una interfaz **IAudioSessionEvents** , vea [eventos de sesión de audio](audio-session-events.md)). Cada método de esta interfaz recibe notificaciones de un tipo determinado de evento de audio.</span><span class="sxs-lookup"><span data-stu-id="4d520-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="4d520-130">Si la aplicación no está interesada en un tipo de evento determinado, el método para ese tipo de evento no debe hacer nada, pero devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4d520-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="4d520-131">El método [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) recibe notificaciones de cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="4d520-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="4d520-132">Normalmente, este método actualiza el control deslizante de volumen de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4d520-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="4d520-133">En el ejemplo de código anterior, el constructor de la clase AudioVolumeEvents se registra para las notificaciones en la [sesión de audio](audio-sessions.md) específica del proceso identificada por el GUID del valor GUID de la sesión \_ .</span><span class="sxs-lookup"><span data-stu-id="4d520-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="4d520-134">De forma predeterminada, las API de audio heredadas como DirectSound, DirectShow y las funciones **waveOutXxx** asignan sus flujos a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="4d520-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="4d520-135">Sin embargo, una aplicación DirectSound o DirectShow puede, opcionalmente, invalidar el comportamiento predeterminado y asignar sus secuencias a una sesión entre procesos o a una sesión identificada por un valor GUID distinto de GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="4d520-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="4d520-136">(Actualmente no se proporciona ningún mecanismo para que una aplicación **waveOutXxx** invalide el comportamiento predeterminado de una manera similar). Para obtener un ejemplo de código de una aplicación de DirectShow con este comportamiento, vea [roles de dispositivo para aplicaciones de DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="4d520-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="4d520-137">Para dar cabida a este tipo de aplicación, puede modificar el constructor en el ejemplo de código anterior para aceptar dos parámetros de entrada adicionales: un GUID de sesión y una marca para indicar si la sesión que se va a supervisar es una sesión de proceso cruzado o específica del proceso.</span><span class="sxs-lookup"><span data-stu-id="4d520-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="4d520-138">Pase estos parámetros a la llamada al método [**IAudioSessionManager:: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) en el constructor.</span><span class="sxs-lookup"><span data-stu-id="4d520-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="4d520-139">Una vez que el constructor llama al método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrarse para recibir notificaciones, la aplicación continúa recibiendo notificaciones solo mientras exista la interfaz [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) o [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="4d520-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="4d520-140">El objeto AudioVolumeEvents del ejemplo de código anterior contiene referencias a estas interfaces hasta que se llama a su destructor.</span><span class="sxs-lookup"><span data-stu-id="4d520-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="4d520-141">Este comportamiento garantiza que la aplicación seguirá recibiendo notificaciones durante el período de duración del objeto AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="4d520-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="4d520-142">En lugar de seleccionar implícitamente un dispositivo de audio en función de su rol de dispositivo, una aplicación de DirectSound o multimedia de Windows heredada podría permitir al usuario seleccionar explícitamente un dispositivo de una lista de dispositivos disponibles que se identifican por sus nombres descriptivos.</span><span class="sxs-lookup"><span data-stu-id="4d520-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="4d520-143">Para admitir este comportamiento, el ejemplo de código anterior debe modificarse para generar notificaciones de eventos de audio para el dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4d520-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="4d520-144">Se requieren dos modificaciones.</span><span class="sxs-lookup"><span data-stu-id="4d520-144">Two modifications are required.</span></span> <span data-ttu-id="4d520-145">En primer lugar, cambie la definición del constructor para que acepte una [cadena de identificador de punto de conexión](endpoint-id-strings.md) como parámetro de entrada (en lugar de los parámetros Flow y role en el ejemplo de código).</span><span class="sxs-lookup"><span data-stu-id="4d520-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="4d520-146">Esta cadena identifica el dispositivo de punto de conexión de audio que corresponde al dispositivo DirectSound o a un dispositivo de onda heredado seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4d520-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="4d520-147">En segundo lugar, reemplace la llamada al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) por una llamada al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="4d520-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="4d520-148">La llamada a **GetDevice** toma la cadena del identificador de punto de conexión como parámetro de entrada y crea una instancia del dispositivo de extremo que se identifica mediante la cadena.</span><span class="sxs-lookup"><span data-stu-id="4d520-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="4d520-149">La técnica para obtener la cadena de identificador de punto de conexión para un dispositivo DirectSound o un dispositivo de forma de onda heredada es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d520-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="4d520-150">En primer lugar, durante la enumeración de dispositivos, DirectSound proporciona la cadena de identificador de punto de conexión para cada dispositivo enumerado.</span><span class="sxs-lookup"><span data-stu-id="4d520-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="4d520-151">Para comenzar la enumeración de dispositivos, la aplicación pasa un puntero de función de devolución de llamada como parámetro de entrada a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="4d520-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="4d520-152">La definición de la función de devolución de llamada es:</span><span class="sxs-lookup"><span data-stu-id="4d520-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="4d520-153">En Windows Vista, el parámetro *lpcstrModule* apunta a la cadena de identificador de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4d520-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="4d520-154">(En versiones anteriores de Windows, incluidos Windows Server 2003, Windows XP y Windows 2000, el parámetro *lpcstrModule* apunta al nombre del módulo del controlador del dispositivo). El parámetro *lpcstrDescription* apunta a una cadena que contiene el nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4d520-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="4d520-155">Para obtener más información acerca de la enumeración de dispositivos DirectSound, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4d520-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="4d520-156">En segundo lugar, para obtener la cadena de identificador de punto de conexión para un dispositivo de onda de onda heredado, utilice la función **waveOutMessage** o **waveInMessage** para enviar un \_ mensaje DRV QUERYFUNCTIONINSTANCEID al controlador de dispositivo de onda.</span><span class="sxs-lookup"><span data-stu-id="4d520-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="4d520-157">Para ver un ejemplo de código que muestra el uso de este mensaje, consulte [roles de dispositivo para aplicaciones multimedia heredadas de Windows](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="4d520-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d520-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d520-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d520-159">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="4d520-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



