---
description: Medidores máximos
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Medidores máximos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04a15ddd2e5fd91cf60845f2a939715e7a4a992f36aea3b9129e69c30d05961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077509"
---
# <a name="peak-meters"></a>Medidores máximos

Para admitir Windows que muestran medidores máximos, [la API EndpointVolume](endpointvolume-api.md) incluye una [**interfaz IAudioMeterInformation.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) Esta interfaz representa un medidor máximo en un dispositivo [de punto de conexión de audio.](audio-endpoint-devices.md) Para un dispositivo de representación, el valor recuperado del medidor máximo representa el valor de muestra máximo encontrado en el flujo de salida al dispositivo durante el período de medición anterior. Para un dispositivo de captura, el valor recuperado del medidor máximo representa el valor de muestra máximo encontrado en el flujo de entrada del dispositivo.

Los valores de medidor máximo obtenidos de los métodos de la interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) son números de punto flotante en el intervalo normalizado de 0,0 a 1,0. Por ejemplo, si una secuencia PCM contiene muestras de 16 bits y el valor máximo de la muestra durante un período de medición determinado es —8914, el valor absoluto registrado por el medidor máximo es 8914 y el valor máximo normalizado notificado por la interfaz **IAudioMeterInformation** es 8914/32768 = 0,272.

Si el dispositivo de punto de conexión de audio implementa el medidor máximo en hardware, la [**interfaz IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) usa el medidor máximo de hardware. De lo contrario, la interfaz implementa el medidor máximo en el software.

Si un dispositivo tiene un medidor máximo de hardware, el medidor máximo está activo tanto en modo compartido como en modo exclusivo. Si un dispositivo carece de medidor máximo de hardware, el medidor máximo está activo en modo compartido, pero no en modo exclusivo. En modo exclusivo, la aplicación y el hardware de audio intercambian datos de audio directamente, omitiendo el medidor máximo de software (que siempre informa de un valor máximo de 0,0).

El siguiente ejemplo de código de C++ es una Windows que muestra un medidor máximo para el dispositivo de representación predeterminado:


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



En el ejemplo de código anterior, la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) y llama al método [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de representación predeterminado. **WinMain** llama al método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obtener la interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) del dispositivo y abre un cuadro de diálogo para mostrar un medidor máximo para el dispositivo. Para obtener más información sobre **WinMain** y **CoCreateInstance,** consulte la documentación Windows SDK. Para obtener más información sobre **IMMDeviceEnumerator** **e IMMDevice**, vea [Enumerating Audio Devices](enumerating-audio-devices.md).

En el ejemplo de código anterior, la función DlgProc muestra el medidor máximo en el cuadro de diálogo. Durante el procesamiento del mensaje WM INITDIALOG, DlgProc llama a la función SetTimer para configurar un temporizador que generará mensajes WM TIMER a intervalos \_ de tiempo [](/windows/win32/api/winuser/nf-winuser-settimer) \_ regulares. Cuando DlgProc recibe un mensaje DE TEMPORIZADOR DE WM, llama a \_ [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) para obtener la lectura más reciente del medidor máximo de la secuencia. A continuación, DlgProc llama a la función DrawPeakMeter para dibujar el medidor máximo actualizado en el cuadro de diálogo. Para obtener más información sobre **SetTimer y** los mensajes WM INITDIALOG y WM TIMER, consulte la \_ documentación Windows \_ SDK.

Puede modificar fácilmente el ejemplo de código anterior para mostrar un medidor máximo para el dispositivo de captura predeterminado. En la [**función WinMain,**](/windows/win32/api/winbase/nf-winbase-winmain) cambie el valor del primer parámetro de la llamada a [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender a eCapture.

El ejemplo de código siguiente es el script de recursos que define los controles que aparecen en el ejemplo de código anterior:


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



El ejemplo de código siguiente es el archivo de encabezado de recursos que define los identificadores de control que aparecen en los ejemplos de código anteriores:


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de volumen](volume-controls.md)
</dt> </dl>

 

 
