---
description: Medidores de pico
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Medidores de pico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153234"
---
# <a name="peak-meters"></a><span data-ttu-id="15f28-103">Medidores de pico</span><span class="sxs-lookup"><span data-stu-id="15f28-103">Peak Meters</span></span>

<span data-ttu-id="15f28-104">Para admitir aplicaciones de Windows que muestran medidores de pico, la [API de EndpointVolume](endpointvolume-api.md) incluye una interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) .</span><span class="sxs-lookup"><span data-stu-id="15f28-104">To support Windows applications that display peak meters, the [EndpointVolume API](endpointvolume-api.md) includes an [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface.</span></span> <span data-ttu-id="15f28-105">Esta interfaz representa un medidor de picos en un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="15f28-105">This interface represents a peak meter on an [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="15f28-106">Para un dispositivo de representación, el valor recuperado del medidor de picos representa el valor de muestra máximo encontrado en el flujo de salida en el dispositivo durante el período de medición anterior.</span><span class="sxs-lookup"><span data-stu-id="15f28-106">For a rendering device, the value retrieved from the peak meter represents the maximum sample value encountered in the output stream to the device during the preceding metering period.</span></span> <span data-ttu-id="15f28-107">Para un dispositivo de captura, el valor recuperado del medidor de picos representa el valor de muestra máximo encontrado en el flujo de entrada desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15f28-107">For a capture device, the value retrieved from the peak meter represents the maximum sample value encountered in the input stream from the device.</span></span>

<span data-ttu-id="15f28-108">Los valores de medidor máximo obtenidos de los métodos de la interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) son números de punto flotante en el intervalo normalizado de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="15f28-108">The peak-meter values obtained from the methods in the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface are floating-point numbers in the normalized range from 0.0 to 1.0.</span></span> <span data-ttu-id="15f28-109">Por ejemplo, si una secuencia PCM contiene ejemplos de 16 bits, y el valor de ejemplo máximo durante un período de medición determinado es: 8914, el valor absoluto registrado por el medidor de pico es 8914 y el valor máximo normalizado indicado por la interfaz **IAudioMeterInformation** es 8914/32768 = 0,272.</span><span class="sxs-lookup"><span data-stu-id="15f28-109">For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is —8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the **IAudioMeterInformation** interface is 8914/32768 = 0.272.</span></span>

<span data-ttu-id="15f28-110">Si el dispositivo de punto de conexión de audio implementa el medidor de picos en el hardware, la interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) utiliza el medidor de picos de hardware.</span><span class="sxs-lookup"><span data-stu-id="15f28-110">If the audio endpoint device implements the peak meter in hardware, the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface uses the hardware peak meter.</span></span> <span data-ttu-id="15f28-111">De lo contrario, la interfaz implementa el medidor de picos en el software.</span><span class="sxs-lookup"><span data-stu-id="15f28-111">Otherwise, the interface implements the peak meter in software.</span></span>

<span data-ttu-id="15f28-112">Si un dispositivo tiene un medidor de picos de hardware, el medidor de picos está activo en modo compartido y en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="15f28-112">If a device has a hardware peak meter, the peak meter is active both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="15f28-113">Si un dispositivo no tiene medidor de picos de hardware, el medidor de picos está activo en modo compartido, pero no en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="15f28-113">If a device lacks hardware peak meter, the peak meter is active in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="15f28-114">En el modo exclusivo, la aplicación y el hardware de audio intercambian datos de audio directamente, omitiendo el medidor de picos de software (que siempre notifica un valor máximo de 0,0).</span><span class="sxs-lookup"><span data-stu-id="15f28-114">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software peak meter (which always reports a peak value of 0.0).</span></span>

<span data-ttu-id="15f28-115">El siguiente ejemplo de código C++ es una aplicación de Windows que muestra un medidor de picos para el dispositivo de representación predeterminado:</span><span class="sxs-lookup"><span data-stu-id="15f28-115">The following C++ code example is a Windows application that displays a peak meter for the default rendering device:</span></span>


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



<span data-ttu-id="15f28-116">En el ejemplo de código anterior, la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia de la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) y llama al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de representación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="15f28-116">In the preceding code example, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="15f28-117">**WinMain** llama al método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para obtener la interfaz [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) del dispositivo y abre un cuadro de diálogo para mostrar un medidor de picos para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15f28-117">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface, and it opens a dialog box to display a peak meter for the device.</span></span> <span data-ttu-id="15f28-118">Para obtener más información acerca de **WinMain** y **CoCreateInstance**, vea la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="15f28-118">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="15f28-119">Para obtener más información sobre **IMMDeviceEnumerator** y **IMMDevice**, consulte [enumeración de dispositivos de audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="15f28-119">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="15f28-120">En el ejemplo de código anterior, la función DlgProc muestra el medidor de picos en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15f28-120">In the preceding code example, the DlgProc function displays the peak meter in the dialog box.</span></span> <span data-ttu-id="15f28-121">Durante el procesamiento del mensaje de INITDIALOG de WM \_ , DlgProc llama a la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) para configurar un temporizador que generará \_ mensajes del temporizador de WM a intervalos de tiempo regulares.</span><span class="sxs-lookup"><span data-stu-id="15f28-121">During processing of the WM\_INITDIALOG message, DlgProc calls the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function to set up a timer that will generate WM\_TIMER messages at regular time intervals.</span></span> <span data-ttu-id="15f28-122">Cuando DlgProc recibe un \_ mensaje del temporizador de WM, llama a [**IAudioMeterInformation:: GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) para obtener la lectura más reciente del medidor máximo para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="15f28-122">When DlgProc receives a WM\_TIMER message, it calls [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) to obtain the latest peak-meter reading for the stream.</span></span> <span data-ttu-id="15f28-123">A continuación, DlgProc llama a la función DrawPeakMeter para dibujar el medidor de picos actualizado en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15f28-123">DlgProc then calls the DrawPeakMeter function to draw the updated peak meter in the dialog box.</span></span> <span data-ttu-id="15f28-124">Para obtener más información sobre **SetTimer** y los \_ mensajes de temporizador de INITDIALOG y WM \_ , consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="15f28-124">For more information about **SetTimer** and the WM\_INITDIALOG and WM\_TIMER messages, see the Windows SDK documentation.</span></span>

<span data-ttu-id="15f28-125">Puede modificar fácilmente el ejemplo de código anterior para mostrar un medidor de picos para el dispositivo de captura predeterminado.</span><span class="sxs-lookup"><span data-stu-id="15f28-125">You can easily modify the preceding code example to display a peak meter for the default capture device.</span></span> <span data-ttu-id="15f28-126">En la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , cambie el valor del primer parámetro de la llamada a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender a eCapture.</span><span class="sxs-lookup"><span data-stu-id="15f28-126">In the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) from eRender to eCapture.</span></span>

<span data-ttu-id="15f28-127">El siguiente ejemplo de código es el script de recursos que define los controles que aparecen en el ejemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="15f28-127">The following code example is the resource script that defines the controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="15f28-128">El ejemplo de código siguiente es el archivo de encabezado de recursos que define los identificadores de control que aparecen en los ejemplos de código anteriores:</span><span class="sxs-lookup"><span data-stu-id="15f28-128">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a><span data-ttu-id="15f28-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="15f28-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15f28-130">Controles de volumen</span><span class="sxs-lookup"><span data-stu-id="15f28-130">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
