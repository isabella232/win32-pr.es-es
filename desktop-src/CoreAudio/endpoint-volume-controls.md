---
description: Controles de volumen de punto de conexión
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Controles de volumen de punto de conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165002"
---
# <a name="endpoint-volume-controls"></a>Controles de volumen de punto de conexión

Las interfaces [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permiten a los clientes controlar los niveles de volumen de las sesiones de [audio](audio-sessions.md), que son colecciones de secuencias de audio en modo compartido. Estas interfaces no funcionan con secuencias de audio en modo exclusivo.

Las aplicaciones que administran secuencias en modo exclusivo pueden controlar los niveles de volumen de esas secuencias a través de la [**interfaz IAudioEndpointVolume.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) Esta interfaz controla el nivel de volumen del dispositivo de [punto de conexión de audio.](audio-endpoint-devices.md) Usa el control de volumen de hardware para el dispositivo de punto de conexión si el hardware de audio implementa este tipo de control. De lo contrario, **la interfaz IAudioEndpointVolume** implementa el control de volumen en el software.

Si un dispositivo tiene un control de volumen de hardware, los cambios realizados en el control a través de la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) afectan al nivel de volumen tanto en modo compartido como en modo exclusivo. Si un dispositivo carece de controles de volumen de hardware y exclusión mutua, los cambios realizados en el volumen de software y los controles de exclusión mutua a través de esta interfaz afectan al nivel de volumen en modo compartido, pero no en modo exclusivo. En modo exclusivo, la aplicación y el hardware de audio intercambian datos de audio directamente, omitiendo los controles de software.

Como regla general, las aplicaciones deben evitar el uso de la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar los niveles de volumen de las secuencias en modo compartido. En su lugar, las aplicaciones deben usar la [**interfaz ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)o [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para ese propósito.

Si una aplicación muestra un control de volumen que usa la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) para controlar el nivel de volumen de un dispositivo de punto de conexión de audio, ese control de volumen debe reflejar el control de volumen del punto de conexión mostrado por el programa de control de volumen del sistema, Sndvol. Como se explicó anteriormente, el control de volumen del punto de conexión aparece en el lado izquierdo de la ventana de Sndvol, en el cuadro de grupo con la etiqueta **Dispositivo**. Si el usuario cambia el volumen del punto de conexión de un dispositivo a través del control de volumen en Sndvol, el control de volumen de punto de conexión correspondiente de la aplicación debe moverse al unísono con el control en Sndvol. De forma similar, si el usuario cambia el nivel de volumen a través del control de volumen del punto de conexión en la ventana de la aplicación, el control de volumen correspondiente de Sndvol debe moverse al unísono con el control de volumen de la aplicación.

Para asegurarse de que el control de volumen del punto de conexión en una ventana de aplicación refleja el control de volumen del punto de conexión en Sndvol, la aplicación debe implementar una interfaz [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) y registrar esa interfaz para recibir notificaciones. Después, cada vez que el usuario cambia el nivel de volumen del punto de conexión en Sndvol, la aplicación recibe una llamada de notificación a través de su método [**IAudioEndpointVolumeCallback::OnNotify.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) Durante esta llamada, el **método OnNotify** puede actualizar el control de volumen del punto de conexión en la ventana de la aplicación para que coincida con la configuración de control que se muestra en Sndvol. De forma similar, cada vez que el usuario cambia el nivel de volumen del punto de conexión a través del control de volumen en la ventana de la aplicación, Sndvol recibe una notificación y actualiza inmediatamente su control de volumen de punto de conexión para mostrar el nuevo nivel de volumen.

El ejemplo de código siguiente es un archivo de encabezado que muestra una posible implementación de la [**interfaz IAudioEndpointVolumeCallback:**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)


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



La clase CAudioEndpointVolumeCallback del ejemplo de código anterior es una implementación de la [**interfaz IAudioEndpointVolumeCallback.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) Dado **que IAudioEndpointVolumeCallback** hereda de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definición de clase contiene implementaciones de los métodos **IUnknown** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Se [**llama al método OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la definición de clase cada vez que uno de los métodos siguientes cambia el nivel de volumen del punto de conexión:

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

La implementación del [**método OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) en el ejemplo de código anterior envía mensajes al control de volumen en la ventana de la aplicación para actualizar el nivel de volumen mostrado.

Una aplicación llama al método [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar su [**interfaz IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) para recibir notificaciones. Cuando la aplicación ya no requiere notificaciones, llama al método [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para eliminar el registro.

El ejemplo de código siguiente es una aplicación de Windows que llama a los métodos [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) y [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) para registrar y anular el registro de la clase CAudioEndpointVolumeCallback en el ejemplo de código anterior:


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



En el ejemplo de código anterior, la función [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) y llama al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de representación predeterminado. **WinMain** llama al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obtener la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) del dispositivo y llama a [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) para registrar la aplicación para recibir notificaciones de cambios en el volumen del punto de conexión. A continuación, **WinMain abre** un cuadro de diálogo para mostrar un control de volumen de punto de conexión para el dispositivo. El cuadro de diálogo también muestra una casilla que indica si el dispositivo está silenciado. La casilla control de volumen y exclusión mutua del cuadro de diálogo refleja la configuración del control de volumen del punto de conexión y la casilla de exclusión mutua mostrada por Sndvol. Para obtener más información sobre **WinMain** y **CoCreateInstance,** consulte la documentación Windows SDK. Para obtener más información sobre **IMMDeviceEnumerator** **e IMMDevice**, vea [Enumerating Audio Devices](enumerating-audio-devices.md).

El procedimiento del cuadro de diálogo DlgProc, en el ejemplo de código anterior, controla los cambios que el usuario realiza en la configuración de volumen y exclusión mutua a través de los controles del cuadro de diálogo. Cuando DlgProc llama a [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) o [**SetMute,**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)Sndvol recibe una notificación del cambio y actualiza el control correspondiente en su ventana para reflejar el nuevo volumen o la configuración de exclusión mutua. Si, en lugar de usar el cuadro de diálogo, el usuario actualiza la configuración de volumen y exclusión mutua a través de los controles de la ventana Sndvol, el método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la clase CAudioEndpointVolumeCallback actualiza los controles del cuadro de diálogo para mostrar la nueva configuración.

Si el usuario cambia el volumen a través de los controles del cuadro de diálogo, el método [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la clase CAudioEndpointVolumeCallback no envía mensajes para actualizar los controles en el cuadro de diálogo. Para ello, sería redundante. **OnNotify actualiza** los controles del cuadro de diálogo solo si el cambio de volumen se originó en Sndvol o en alguna otra aplicación. El segundo parámetro de las llamadas al método [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) y [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) en la función DlgProc es un puntero a un GUID de contexto de evento que cualquiera de los métodos pasa a **OnNotify.** **OnNotify comprueba** el valor del GUID del contexto de evento para determinar si el cuadro de diálogo es el origen del cambio de volumen. Para obtener más información sobre los GUID de contexto de evento, vea **IAudioEndpointVolumeCallback::OnNotify**.

Cuando el usuario sale del cuadro de diálogo, la llamada [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) del ejemplo de código anterior elimina el registro de la clase CAudioEndpointVolumeCallback antes de que finalice el programa.

Puede modificar fácilmente el ejemplo de código anterior para mostrar controles de volumen y exclusión mutua para el dispositivo de captura predeterminado. En la [**función WinMain,**](/windows/desktop/api/winbase/nf-winbase-winmain) cambie el valor del primer parámetro de la llamada al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender a eCapture.

El ejemplo de código siguiente es el script de recursos que define los controles de volumen y exclusión mutua que aparecen en el ejemplo de código anterior:


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



El ejemplo de código siguiente es el archivo de encabezado de recursos que define los identificadores de control que aparecen en los ejemplos de código anteriores:


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Los ejemplos de código anteriores se combinan para formar una aplicación sencilla para controlar y supervisar el volumen del punto de conexión del dispositivo de representación predeterminado. Una aplicación más útil también podría notificar al usuario cuándo cambia el estado del dispositivo. Por ejemplo, el dispositivo podría deshabilitarse, desconectarse o quitarse. Para obtener más información sobre cómo supervisar estos tipos de eventos, vea [Eventos de dispositivo.](device-events.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 
