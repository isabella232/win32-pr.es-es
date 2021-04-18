---
description: Implementar una barra de búsqueda
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementar una barra de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537810"
---
# <a name="implementing-a-seek-bar"></a>Implementar una barra de búsqueda

En esta sección se describe cómo implementar una barra de búsqueda para una aplicación de reproductor de media. La barra de búsqueda se implementa como un control TrackBar. Para obtener información general sobre la búsqueda en DirectShow, consulte [búsqueda del gráfico de filtro](seeking-the-filter-graph.md).

Cuando se inicie la aplicación, inicialice el TrackBar:


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



El elemento TrackBar se deshabilita hasta que el usuario abre un archivo multimedia. El intervalo de TrackBar se establece de 0 a 100. Durante la reproducción de archivos, la aplicación calculará la posición de reproducción como un porcentaje de la duración del archivo y actualizará la barra de la barra en consecuencia. Por ejemplo, la posición de TrackBar "50" siempre corresponde a la mitad del archivo.

Cuando el usuario abre un archivo, cree un gráfico de reproducción de archivos con **RenderFile**. El código para esto se muestra en [Cómo reproducir un archivo](how-to-play-a-file.md). A continuación, consulte el administrador de gráficos de filtro para la interfaz **IMediaSeeking** y almacene el puntero de interfaz:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Para determinar si se puede buscar en el archivo, llame al método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o al método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Estos métodos hacen casi lo mismo, pero su semántica es ligeramente diferente. En el ejemplo siguiente se usa **CheckCapabilites**:


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



La \_ marca de CanSeekAbsolute de búsqueda de búsquedas \_ comprueba si se puede buscar en el archivo de origen y la \_ marca AM Seek \_ CanGetDuration comprueba si la duración del archivo se puede determinar de antemano. Si se admiten las dos funciones, la aplicación habilita la barra de opciones y recupera la duración del archivo.

Si se realiza búsquedas en el gráfico, la aplicación usará un temporizador para actualizar la posición de TrackBar durante la reproducción. Al ejecutar el gráfico de filtro para reproducir el archivo, inicie el evento de temporizador llamando a una de las funciones de temporizador de Windows, como **SetTimer**. Para obtener más información sobre los temporizadores, vea el tema sobre temporizadores en Platform SDK.


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



Utilice el evento de temporizador para actualizar la posición de la barra de la barra. Llame a [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar la posición de reproducción Currant y, a continuación, calcule la posición como un porcentaje de la duración del archivo:


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



El usuario también puede trasladar la barra de desplazamiento para buscar el archivo. Cuando el usuario arrastra o hace clic en el control TrackBar, la aplicación recibe un \_ evento HSCROLL de WM. La palabra baja del parámetro *wParam* es el mensaje de notificación de TrackBar. Por ejemplo, TB \_ ENDTRACK se envía al final de la acción TrackBar y TB \_ THUMBTRACK se envía continuamente mientras el usuario arrastra la barra de información. En el código siguiente se muestra una manera de controlar el mensaje de HSCROLL de WM \_ :


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



Si el usuario arrastra la barra de comandos, la aplicación emite una serie de comandos de búsqueda, uno para cada mensaje de TB \_ THUMBTRACK que recibe. Para que las operaciones de búsqueda sean lo más suaves posible, la aplicación pausa el gráfico. Al pausar el gráfico se detiene la reproducción pero se asegura de que se actualiza la ventana de vídeo. Cuando la aplicación recibe el mensaje de TB \_ ENDTRACK, restaura el gráfico a su estado original.

 

 



