---
description: Controles de volumen de punto de conexión
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Controles de volumen de punto de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481890"
---
# <a name="endpoint-volume-controls"></a><span data-ttu-id="ca1de-103">Controles de volumen de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="ca1de-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="ca1de-104">Las interfaces [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permiten a los clientes controlar los niveles de volumen de las sesiones de [audio](audio-sessions.md), que son colecciones de secuencias de audio en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="ca1de-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="ca1de-105">Estas interfaces no funcionan con secuencias de audio en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="ca1de-106">Las aplicaciones que administran secuencias en modo exclusivo pueden controlar los niveles de volumen de esas secuencias a través de la [**interfaz IAudioEndpointVolume.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)</span><span class="sxs-lookup"><span data-stu-id="ca1de-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="ca1de-107">Esta interfaz controla el nivel de volumen del dispositivo de [punto de conexión de audio.](audio-endpoint-devices.md)</span><span class="sxs-lookup"><span data-stu-id="ca1de-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="ca1de-108">Usa el control de volumen de hardware para el dispositivo de punto de conexión si el hardware de audio implementa este tipo de control.</span><span class="sxs-lookup"><span data-stu-id="ca1de-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="ca1de-109">De lo contrario, **la interfaz IAudioEndpointVolume** implementa el control de volumen en el software.</span><span class="sxs-lookup"><span data-stu-id="ca1de-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="ca1de-110">Si un dispositivo tiene un control de volumen de hardware, los cambios realizados en el control a través de la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) afectan al nivel de volumen tanto en modo compartido como en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="ca1de-111">Si un dispositivo no tiene controles de volumen y exclusión de hardware, los cambios realizados en el volumen de software y los controles de exclusión mutua a través de esta interfaz afectan al nivel de volumen en modo compartido, pero no en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="ca1de-112">En modo exclusivo, la aplicación y el hardware de audio intercambian datos de audio directamente, omitiendo los controles de software.</span><span class="sxs-lookup"><span data-stu-id="ca1de-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="ca1de-113">Como regla general, las aplicaciones deben evitar el uso de la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar los niveles de volumen de los flujos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="ca1de-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="ca1de-114">En su lugar, las aplicaciones deben usar la [**interfaz ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)o [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="ca1de-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="ca1de-115">Si una aplicación muestra un control de volumen que usa la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar el nivel de volumen de un dispositivo de punto de conexión de audio, ese control de volumen debe reflejar el control de volumen del punto de conexión mostrado por el programa de control de volumen del sistema, Sndvol.</span><span class="sxs-lookup"><span data-stu-id="ca1de-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="ca1de-116">Como se explicó anteriormente, el control de volumen del punto de conexión aparece en el lado izquierdo de la ventana de Sndvol, en el cuadro de grupo con la etiqueta **Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="ca1de-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="ca1de-117">Si el usuario cambia el volumen del punto de conexión de un dispositivo a través del control de volumen en Sndvol, el control de volumen de punto de conexión correspondiente de la aplicación debe moverse al unísono con el control en Sndvol.</span><span class="sxs-lookup"><span data-stu-id="ca1de-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="ca1de-118">De forma similar, si el usuario cambia el nivel de volumen a través del control de volumen del punto de conexión en la ventana de la aplicación, el control de volumen correspondiente de Sndvol debe moverse al unísono con el control de volumen de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ca1de-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="ca1de-119">Para asegurarse de que el control de volumen del punto de conexión en una ventana de aplicación refleja el control de volumen del punto de conexión en Sndvol, la aplicación debe implementar una interfaz [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) y registrar esa interfaz para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ca1de-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="ca1de-120">A partir de entonces, cada vez que el usuario cambia el nivel de volumen del punto de conexión en Sndvol, la aplicación recibe una llamada de notificación a través de su método [**IAudioEndpointVolumeCallback::OnNotify.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify)</span><span class="sxs-lookup"><span data-stu-id="ca1de-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="ca1de-121">Durante esta llamada, el **método OnNotify** puede actualizar el control de volumen del punto de conexión en la ventana de la aplicación para que coincida con la configuración de control que se muestra en Sndvol.</span><span class="sxs-lookup"><span data-stu-id="ca1de-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="ca1de-122">De forma similar, cada vez que el usuario cambia el nivel de volumen del punto de conexión a través del control de volumen en la ventana de la aplicación, Sndvol recibe una notificación y actualiza inmediatamente su control de volumen de punto de conexión para mostrar el nuevo nivel de volumen.</span><span class="sxs-lookup"><span data-stu-id="ca1de-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="ca1de-123">El ejemplo de código siguiente es un archivo de encabezado que muestra una posible implementación de la [**interfaz IAudioEndpointVolumeCallback:**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)</span><span class="sxs-lookup"><span data-stu-id="ca1de-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
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

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



<span data-ttu-id="ca1de-124">La clase CAudioEndpointVolumeCallback del ejemplo de código anterior es una implementación de la [**interfaz IAudioEndpointVolumeCallback.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)</span><span class="sxs-lookup"><span data-stu-id="ca1de-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="ca1de-125">Dado **que IAudioEndpointVolumeCallback** hereda de [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)la definición de clase contiene implementaciones de los métodos **IUnknown** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="ca1de-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="ca1de-126">Se [**llama al método OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) en la definición de clase cada vez que uno de los métodos siguientes cambia el nivel de volumen del punto de conexión:</span><span class="sxs-lookup"><span data-stu-id="ca1de-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="ca1de-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="ca1de-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="ca1de-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="ca1de-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="ca1de-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="ca1de-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="ca1de-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="ca1de-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="ca1de-131">**IAudioEndpointVolume::SetMute**</span><span class="sxs-lookup"><span data-stu-id="ca1de-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="ca1de-132">**IAudioEndpointVolume::VolumeStepDown**</span><span class="sxs-lookup"><span data-stu-id="ca1de-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="ca1de-133">**IAudioEndpointVolume::VolumeStepUp**</span><span class="sxs-lookup"><span data-stu-id="ca1de-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="ca1de-134">La implementación del [**método OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) en el ejemplo de código anterior envía mensajes al control de volumen en la ventana de la aplicación para actualizar el nivel de volumen mostrado.</span><span class="sxs-lookup"><span data-stu-id="ca1de-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="ca1de-135">Una aplicación llama al método [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar su interfaz [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ca1de-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="ca1de-136">Cuando la aplicación ya no requiere notificaciones, llama al método [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="ca1de-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="ca1de-137">El ejemplo de código siguiente es una aplicación Windows que llama a los métodos [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) y [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para registrar y anular el registro de la clase CAudioEndpointVolumeCallback en el ejemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="ca1de-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (g_pEndptVol != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



<span data-ttu-id="ca1de-138">En el ejemplo de código anterior, la función [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) y llama al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de representación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca1de-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="ca1de-139">**WinMain** llama al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obtener la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) del dispositivo y llama a [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar la aplicación para recibir notificaciones de cambios en el volumen del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="ca1de-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="ca1de-140">A continuación, **WinMain abre** un cuadro de diálogo para mostrar un control de volumen de punto de conexión para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="ca1de-141">El cuadro de diálogo también muestra una casilla que indica si el dispositivo está silenciado.</span><span class="sxs-lookup"><span data-stu-id="ca1de-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="ca1de-142">La casilla control de volumen y exclusión mutua del cuadro de diálogo refleja la configuración del control de volumen de punto de conexión y la casilla de exclusión mutua mostrada por Sndvol.</span><span class="sxs-lookup"><span data-stu-id="ca1de-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="ca1de-143">Para más información sobre **WinMain** y **CoCreateInstance,** consulte la documentación Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ca1de-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="ca1de-144">Para obtener más información **sobre IMMDeviceEnumerator** **e IMMDevice**, vea [Enumerating Audio Devices](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="ca1de-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="ca1de-145">El procedimiento del cuadro de diálogo DlgProc, en el ejemplo de código anterior, controla los cambios que el usuario realiza en la configuración de volumen y exclusión mediante los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="ca1de-146">Cuando DlgProc llama a [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) o [**SetMute,**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)Sndvol recibe la notificación del cambio y actualiza el control correspondiente en su ventana para reflejar la nueva configuración de volumen o exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="ca1de-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="ca1de-147">Si, en lugar de usar el cuadro de diálogo, el usuario actualiza la configuración de volumen y exclusión mutua a través de los controles de la ventana de Sndvol, el método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la clase CAudioEndpointVolumeCallback actualiza los controles del cuadro de diálogo para mostrar la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="ca1de-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="ca1de-148">Si el usuario cambia el volumen a través de los controles del cuadro de diálogo, el método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la clase CAudioEndpointVolumeCallback no envía mensajes para actualizar los controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="ca1de-149">Para ello, sería redundante.</span><span class="sxs-lookup"><span data-stu-id="ca1de-149">To do so would be redundant.</span></span> <span data-ttu-id="ca1de-150">**OnNotify actualiza** los controles del cuadro de diálogo solo si el cambio de volumen se originó en Sndvol o en alguna otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="ca1de-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="ca1de-151">El segundo parámetro de las llamadas al método [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) y [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) en la función DlgProc es un puntero a un GUID de contexto de evento que cualquiera de los métodos pasa a **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="ca1de-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="ca1de-152">**OnNotify comprueba** el valor del GUID del contexto de evento para determinar si el cuadro de diálogo es el origen del cambio de volumen.</span><span class="sxs-lookup"><span data-stu-id="ca1de-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="ca1de-153">Para obtener más información sobre los GUID de contexto de evento, vea **IAudioEndpointVolumeCallback::OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="ca1de-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="ca1de-154">Cuando el usuario sale del cuadro de diálogo, la llamada [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) del ejemplo de código anterior elimina el registro de la clase CAudioEndpointVolumeCallback antes de que finalice el programa.</span><span class="sxs-lookup"><span data-stu-id="ca1de-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="ca1de-155">Puede modificar fácilmente el ejemplo de código anterior para mostrar controles de volumen y exclusión mutua para el dispositivo de captura predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca1de-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="ca1de-156">En la [**función WinMain,**](/windows/desktop/api/winbase/nf-winbase-winmain) cambie el valor del primer parámetro de la llamada al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender a eCapture.</span><span class="sxs-lookup"><span data-stu-id="ca1de-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="ca1de-157">El ejemplo de código siguiente es el script de recursos que define los controles de volumen y exclusión mutua que aparecen en el ejemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="ca1de-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



<span data-ttu-id="ca1de-158">El ejemplo de código siguiente es el archivo de encabezado de recursos que define los identificadores de control que aparecen en los ejemplos de código anteriores:</span><span class="sxs-lookup"><span data-stu-id="ca1de-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="ca1de-159">Los ejemplos de código anteriores se combinan para formar una aplicación sencilla para controlar y supervisar el volumen del punto de conexión del dispositivo de representación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ca1de-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="ca1de-160">Una aplicación más útil también podría notificar al usuario cuándo cambia el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca1de-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="ca1de-161">Por ejemplo, el dispositivo podría deshabilitarse, desconectarse o quitarse.</span><span class="sxs-lookup"><span data-stu-id="ca1de-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="ca1de-162">Para obtener más información sobre la supervisión de estos tipos de eventos, vea [Eventos de dispositivo.](device-events.md)</span><span class="sxs-lookup"><span data-stu-id="ca1de-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca1de-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca1de-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca1de-164">Controles de volumen</span><span class="sxs-lookup"><span data-stu-id="ca1de-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
