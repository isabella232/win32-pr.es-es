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
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="32b01-103">Implementar una barra de búsqueda</span><span class="sxs-lookup"><span data-stu-id="32b01-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="32b01-104">En esta sección se describe cómo implementar una barra de búsqueda para una aplicación de reproductor de media.</span><span class="sxs-lookup"><span data-stu-id="32b01-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="32b01-105">La barra de búsqueda se implementa como un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32b01-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="32b01-106">Para obtener información general sobre la búsqueda en DirectShow, consulte [búsqueda del gráfico de filtro](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="32b01-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="32b01-107">Cuando se inicie la aplicación, inicialice el TrackBar:</span><span class="sxs-lookup"><span data-stu-id="32b01-107">When the application starts, initialize the trackbar:</span></span>


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



<span data-ttu-id="32b01-108">El elemento TrackBar se deshabilita hasta que el usuario abre un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="32b01-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="32b01-109">El intervalo de TrackBar se establece de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="32b01-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="32b01-110">Durante la reproducción de archivos, la aplicación calculará la posición de reproducción como un porcentaje de la duración del archivo y actualizará la barra de la barra en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="32b01-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="32b01-111">Por ejemplo, la posición de TrackBar "50" siempre corresponde a la mitad del archivo.</span><span class="sxs-lookup"><span data-stu-id="32b01-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="32b01-112">Cuando el usuario abre un archivo, cree un gráfico de reproducción de archivos con **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="32b01-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="32b01-113">El código para esto se muestra en [Cómo reproducir un archivo](how-to-play-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="32b01-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="32b01-114">A continuación, consulte el administrador de gráficos de filtro para la interfaz **IMediaSeeking** y almacene el puntero de interfaz:</span><span class="sxs-lookup"><span data-stu-id="32b01-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="32b01-115">Para determinar si se puede buscar en el archivo, llame al método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) o al método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="32b01-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="32b01-116">Estos métodos hacen casi lo mismo, pero su semántica es ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="32b01-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="32b01-117">En el ejemplo siguiente se usa **CheckCapabilites**:</span><span class="sxs-lookup"><span data-stu-id="32b01-117">The following example uses **CheckCapabilites**:</span></span>


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



<span data-ttu-id="32b01-118">La \_ marca de CanSeekAbsolute de búsqueda de búsquedas \_ comprueba si se puede buscar en el archivo de origen y la \_ marca AM Seek \_ CanGetDuration comprueba si la duración del archivo se puede determinar de antemano.</span><span class="sxs-lookup"><span data-stu-id="32b01-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="32b01-119">Si se admiten las dos funciones, la aplicación habilita la barra de opciones y recupera la duración del archivo.</span><span class="sxs-lookup"><span data-stu-id="32b01-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="32b01-120">Si se realiza búsquedas en el gráfico, la aplicación usará un temporizador para actualizar la posición de TrackBar durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="32b01-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="32b01-121">Al ejecutar el gráfico de filtro para reproducir el archivo, inicie el evento de temporizador llamando a una de las funciones de temporizador de Windows, como **SetTimer**.</span><span class="sxs-lookup"><span data-stu-id="32b01-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="32b01-122">Para obtener más información sobre los temporizadores, vea el tema sobre temporizadores en Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="32b01-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


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



<span data-ttu-id="32b01-123">Utilice el evento de temporizador para actualizar la posición de la barra de la barra.</span><span class="sxs-lookup"><span data-stu-id="32b01-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="32b01-124">Llame a [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar la posición de reproducción Currant y, a continuación, calcule la posición como un porcentaje de la duración del archivo:</span><span class="sxs-lookup"><span data-stu-id="32b01-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


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



<span data-ttu-id="32b01-125">El usuario también puede trasladar la barra de desplazamiento para buscar el archivo.</span><span class="sxs-lookup"><span data-stu-id="32b01-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="32b01-126">Cuando el usuario arrastra o hace clic en el control TrackBar, la aplicación recibe un \_ evento HSCROLL de WM.</span><span class="sxs-lookup"><span data-stu-id="32b01-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="32b01-127">La palabra baja del parámetro *wParam* es el mensaje de notificación de TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32b01-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="32b01-128">Por ejemplo, TB \_ ENDTRACK se envía al final de la acción TrackBar y TB \_ THUMBTRACK se envía continuamente mientras el usuario arrastra la barra de información.</span><span class="sxs-lookup"><span data-stu-id="32b01-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="32b01-129">En el código siguiente se muestra una manera de controlar el mensaje de HSCROLL de WM \_ :</span><span class="sxs-lookup"><span data-stu-id="32b01-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


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



<span data-ttu-id="32b01-130">Si el usuario arrastra la barra de comandos, la aplicación emite una serie de comandos de búsqueda, uno para cada mensaje de TB \_ THUMBTRACK que recibe.</span><span class="sxs-lookup"><span data-stu-id="32b01-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="32b01-131">Para que las operaciones de búsqueda sean lo más suaves posible, la aplicación pausa el gráfico.</span><span class="sxs-lookup"><span data-stu-id="32b01-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="32b01-132">Al pausar el gráfico se detiene la reproducción pero se asegura de que se actualiza la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="32b01-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="32b01-133">Cuando la aplicación recibe el mensaje de TB \_ ENDTRACK, restaura el gráfico a su estado original.</span><span class="sxs-lookup"><span data-stu-id="32b01-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



