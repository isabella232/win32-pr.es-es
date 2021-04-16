---
description: Escribir el archivo
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Escribir el archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687153"
---
# <a name="writing-the-file"></a>Escribir el archivo

Para escribir el archivo, simplemente ejecute el gráfico de filtro llamando al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Espere a que se complete la reproducción y detenga explícitamente el gráfico mediante una llamada a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); de lo contrario, el archivo no se escribirá correctamente.

Para mostrar el progreso de la operación de escritura de archivos, consulte el filtro MUX de la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Llame al método [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) para recuperar la duración del archivo. Periódicamente mientras se ejecuta el gráfico, llame al método [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar la posición actual del gráfico en la secuencia. La posición actual dividida por la duración proporciona el porcentaje completado.

> [!Note]  
> Una aplicación normalmente consulta el administrador de gráficos de filtro para **IMediaSeeking**, pero la escritura de archivos es una excepción a esta regla. El administrador de gráficos de filtro calcula la posición actual a partir de la posición inicial y cuánto tiempo se ha estado ejecutando el gráfico, lo cual es preciso para la reproducción de archivos, pero no para la escritura de archivos. Por lo tanto, para obtener un resultado preciso, debe recuperar la posición del filtro MUX.

 

En el código siguiente se obtiene la duración del archivo, se inicia un temporizador para actualizar la interfaz de usuario de la aplicación y se ejecuta el gráfico de filtro. (La comprobación de errores se omite para mayor claridad).


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



Cuando la aplicación recibe un evento de temporizador, puede actualizar la interfaz de usuario con la posición actual:


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



Cuando la aplicación recibe un evento de finalización de DirectShow, debe detener el gráfico, tal y como se muestra en el código siguiente:


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



