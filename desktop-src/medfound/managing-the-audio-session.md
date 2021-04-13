---
description: En este tema se describe cómo controlar el volumen de audio cuando se usa MFPlay para la reproducción de audio y vídeo.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Administrar la sesión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360130"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="f930c-103">Administrar la sesión de audio</span><span class="sxs-lookup"><span data-stu-id="f930c-103">Managing the Audio Session</span></span>

<span data-ttu-id="f930c-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f930c-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f930c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f930c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f930c-106">\]</span><span class="sxs-lookup"><span data-stu-id="f930c-106">\]</span></span>

<span data-ttu-id="f930c-107">En este tema se describe cómo controlar el volumen de audio cuando se usa MFPlay para la reproducción de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="f930c-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="f930c-108">MFPlay proporciona los siguientes métodos para controlar el volumen de audio durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="f930c-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="f930c-109">Método</span><span class="sxs-lookup"><span data-stu-id="f930c-109">Method</span></span>                                                            | <span data-ttu-id="f930c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f930c-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="f930c-111">**IMFPMediaPlayer::SetBalance**</span><span class="sxs-lookup"><span data-stu-id="f930c-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="f930c-112">Establece el equilibrio entre los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="f930c-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="f930c-113">**IMFPMediaPlayer::SetMute**</span><span class="sxs-lookup"><span data-stu-id="f930c-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="f930c-114">Silencia o desactiva el audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="f930c-115">**IMFPMediaPlayer::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="f930c-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="f930c-116">Establece el nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="f930c-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="f930c-117">Para comprender el comportamiento de estos métodos, debe conocer la terminología de la API de sesión de audio de Windows (WASAPI), que implementa la funcionalidad de audio de bajo nivel que usa MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f930c-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="f930c-118">En WASAPI, cada secuencia de audio pertenece a exactamente una *sesión de audio*, que es un grupo de secuencias de audio relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f930c-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="f930c-119">Normalmente, una aplicación mantiene una única sesión de audio, aunque las aplicaciones pueden crear más de una sesión.</span><span class="sxs-lookup"><span data-stu-id="f930c-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="f930c-120">El programa de control de volumen del sistema (Sndvol) muestra un control de volumen para cada sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="f930c-121">A través de Sndvol, un usuario puede ajustar el volumen de una sesión de audio desde fuera de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f930c-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="f930c-122">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="f930c-122">The following image illustrates this process.</span></span>

![diagrama que muestra secuencias de audio que pasan a través del control de volumen a los oradores; sndvol de aplicación y de punto a control de volumen](images/audio-session.gif)

<span data-ttu-id="f930c-124">En MFPlay, un elemento multimedia puede tener una o varias secuencias de audio activas (normalmente solo una).</span><span class="sxs-lookup"><span data-stu-id="f930c-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="f930c-125">Internamente, MFPlay usa el [representador de audio de streaming](streaming-audio-renderer.md) (SAR) para representar las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="f930c-126">A menos que lo configure de otro modo, el SAR se une a la sesión de audio predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f930c-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="f930c-127">Los métodos de audio MFPlay controlan solo las secuencias que pertenecen al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="f930c-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="f930c-128">No afectan al volumen de ningún otro flujo que pertenezca a la misma sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="f930c-129">En términos de WASAPI, los métodos de MFPlay controlan los niveles de volumen *por canal* , no el nivel de volumen maestro.</span><span class="sxs-lookup"><span data-stu-id="f930c-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="f930c-130">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="f930c-130">The following image illustrates this process.</span></span>

![diagrama similar al anterior, pero el segundo flujo comienza en el elemento multimedia, y la aplicación apunta a la segunda secuencia y al control de volumen.](images/audio-session02.gif)

<span data-ttu-id="f930c-132">Es importante comprender algunas implicaciones de esta característica de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f930c-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="f930c-133">En primer lugar, una aplicación puede ajustar el volumen de reproducción sin que afecte a otras secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="f930c-134">Puede usar esta característica si MFPlay para implementar el fundido cruzado de audio, creando dos instancias del objeto MFPlay y ajustando el volumen por separado.</span><span class="sxs-lookup"><span data-stu-id="f930c-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="f930c-135">Si usa métodos de MFPlay para cambiar el estado de volumen o silenciar, los cambios no aparecen en Sndvol.</span><span class="sxs-lookup"><span data-stu-id="f930c-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="f930c-136">Por ejemplo, puede llamar a [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) para silenciar el audio, pero Sndvol no mostrará la sesión como silenciada.</span><span class="sxs-lookup"><span data-stu-id="f930c-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="f930c-137">Por el contrario, si se usa SndVol para ajustar el volumen de sesión, los cambios no se reflejan en los valores devueltos por [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) o [**IMFPMediaPlayer:: GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span><span class="sxs-lookup"><span data-stu-id="f930c-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="f930c-138">Para cada instancia del objeto MFPlay Player, el nivel de volumen efectivo es igual a *fPlayerVolume* × *FSessionVolume*, donde *fPlayerVolume* es el valor devuelto por [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)y *fSessionVolume* es el volumen principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f930c-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="f930c-139">En el caso de escenarios de reproducción sencillos, podría ser preferible usar WASAPI para controlar el volumen de audio para toda la sesión, en lugar de usar los métodos MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f930c-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="f930c-140">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f930c-140">Example Code</span></span>

<span data-ttu-id="f930c-141">A continuación se muestra una clase de C++ que controla las tareas básicas de WASAPI:</span><span class="sxs-lookup"><span data-stu-id="f930c-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="f930c-142">Controlar el volumen y silenciar el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f930c-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="f930c-143">Recibir notificaciones cada vez que cambie el estado del volumen o silenciar.</span><span class="sxs-lookup"><span data-stu-id="f930c-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="f930c-144">Declaración de clase</span><span class="sxs-lookup"><span data-stu-id="f930c-144">Class Declaration</span></span>

<span data-ttu-id="f930c-145">La `CAudioSessionVolume` declaración de clase implementa la interfaz [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , que es la interfaz de devolución de llamada para los eventos de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="f930c-146">Cuando el `CAudioSessionVolume` objeto recibe un evento de sesión de audio, envía un mensaje de ventana privada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f930c-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="f930c-147">El identificador de ventana y el mensaje de ventana se proporcionan como parámetros para el `CAudioSessionVolume::CreateInstance` método estático.</span><span class="sxs-lookup"><span data-stu-id="f930c-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="f930c-148">Obtener los punteros de la interfaz WASAPI</span><span class="sxs-lookup"><span data-stu-id="f930c-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="f930c-149">`CAudioSessionVolume` usa dos interfaces WASAPI principales:</span><span class="sxs-lookup"><span data-stu-id="f930c-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="f930c-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) administra la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="f930c-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controla el nivel de volumen y el estado de silencio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f930c-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="f930c-152">Para obtener estas interfaces, debe enumerar el extremo de audio que utiliza el SAR.</span><span class="sxs-lookup"><span data-stu-id="f930c-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="f930c-153">Un *punto de conexión de audio* es un dispositivo de hardware que captura o usa datos de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="f930c-154">Para la reproducción de audio, un punto de conexión es simplemente un altavoz u otra salida de audio.</span><span class="sxs-lookup"><span data-stu-id="f930c-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="f930c-155">De forma predeterminada, el SAR usa el punto de conexión predeterminado para el rol de dispositivo **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="f930c-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="f930c-156">Un *rol de dispositivo* es un rol asignado para un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="f930c-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="f930c-157">Los roles de dispositivo se especifican mediante la enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , que está documentada en las [API de audio Core](../coreaudio/core-audio-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="f930c-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="f930c-158">En el código siguiente se muestra cómo enumerar el punto de conexión y obtener las interfaces de WASAPI.</span><span class="sxs-lookup"><span data-stu-id="f930c-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="f930c-159">Control del volumen</span><span class="sxs-lookup"><span data-stu-id="f930c-159">Controlling the Volume</span></span>

<span data-ttu-id="f930c-160">Los `CAudioSessionVolume` métodos que controlan el volumen de audio llaman a los métodos [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f930c-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="f930c-161">Por ejemplo, `CAudioSessionVolume::SetVolume` llama a [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="f930c-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="f930c-162">Código de CAudioSessionVolume completo</span><span class="sxs-lookup"><span data-stu-id="f930c-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="f930c-163">Esta es la lista completa de los métodos de la `CAudioSessionVolume` clase.</span><span class="sxs-lookup"><span data-stu-id="f930c-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="f930c-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f930c-164">Requirements</span></span>

<span data-ttu-id="f930c-165">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f930c-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f930c-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f930c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f930c-167">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="f930c-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
