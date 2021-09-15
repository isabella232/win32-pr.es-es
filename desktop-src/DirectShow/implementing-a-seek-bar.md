---
description: Implementar una barra de búsqueda
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementar una barra de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473977"
---
# <a name="implementing-a-seek-bar"></a>Implementar una barra de búsqueda

En esta sección se describe cómo implementar una barra de búsqueda para una aplicación de reproductor multimedia. La barra de búsqueda se implementa como un control trackbar. Para obtener información general sobre la búsqueda en DirectShow, vea [Buscar el filtro Graph](seeking-the-filter-graph.md).

Cuando se inicie la aplicación, inicialice la barra de seguimiento:


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



La barra de seguimiento se deshabilita hasta que el usuario abre un archivo multimedia. El intervalo de la barra de seguimiento se establece entre 0 y 100. Durante la reproducción de archivos, la aplicación calculará la posición de reproducción como porcentaje de la duración del archivo y actualizará la barra de seguimiento en consecuencia. Por ejemplo, la posición de la barra de seguimiento "50" siempre se corresponde con el centro del archivo.

Cuando el usuario abra un archivo, compile un gráfico de reproducción de archivos mediante **RenderFile.** El código para esto se muestra en [Cómo reproducir un archivo](how-to-play-a-file.md). A continuación, consulte filter Graph Manager para la **interfaz IMediaSeeking** y almacene el puntero de interfaz:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Para determinar si el archivo es buscable, llame al método [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o al método [**IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) Estos métodos hacen casi lo mismo, pero su semántica es ligeramente diferente. En el ejemplo siguiente se **usa CheckCapabilites**:


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



La marca \_ CanSeekAbsolute de AM SEEKING comprueba si el archivo de origen es buscable y la marca \_ \_ CanGetDuration de AM SEEKING comprueba si la duración del archivo se puede determinar \_ de antemano. Si se admiten ambas funcionalidades, la aplicación habilita la barra de seguimiento y recupera la duración del archivo.

Si el gráfico es buscable, la aplicación usará un temporizador para actualizar la posición de la barra de seguimiento durante la reproducción. Al ejecutar el gráfico de filtros para reproducir el archivo, inicie el evento de temporizador llamando a una de las funciones de temporizador Windows, como **SetTimer**. Para obtener más información sobre los temporizadores, vea el tema "Temporizadores" en el SDK de plataforma.


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



Use el evento de temporizador para actualizar la posición de la barra de seguimiento. Llame [**a IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar la posición de reproducción currant y, a continuación, calcule la posición como un porcentaje de la duración del archivo:


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



El usuario también puede mover la barra de seguimiento para buscar el archivo. Cuando el usuario arrastra o hace clic en el control trackbar, la aplicación recibe un evento \_ WM HSCROLL. La palabra baja del parámetro *wParam* es el mensaje de notificación de la barra de seguimiento. Por ejemplo, ENDTRACK de TB se envía al final de la acción de la barra de seguimiento y TB THUMBTRACK se envía continuamente mientras el usuario arrastra \_ \_ la barra de seguimiento. El código siguiente muestra una manera de controlar el mensaje \_ HSCROLL de WM:


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



Si el usuario arrastra la barra de seguimiento, la aplicación emite una serie de comandos seek, uno para cada mensaje THUMBTRACK de TB \_ que recibe. Para que las operaciones de búsqueda se realicen lo más fluidas posible, la aplicación pausa el gráfico. Al pausar el gráfico se detiene la reproducción, pero se garantiza que la ventana de vídeo se actualiza. Cuando la aplicación recibe el mensaje \_ ENDTRACK de TB, restaura el gráfico a su estado original.

 

 



