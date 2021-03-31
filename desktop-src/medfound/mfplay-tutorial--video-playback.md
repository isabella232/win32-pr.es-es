---
description: En este tutorial se presenta una aplicación completa que reproduce vídeo mediante MFPlay.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Tutorial de MFPlay: reproducción de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812620"
---
# <a name="mfplay-tutorial-video-playback"></a>Tutorial de MFPlay: reproducción de vídeo

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tutorial se presenta una aplicación completa que reproduce vídeo mediante MFPlay. Se basa en el ejemplo de SDK de [SimplePlay](simpleplay-sample.md) .

Este tutorial contiene las siguientes secciones:

-   [Requisitos](#requirements)
-   [Archivos de encabezado y de biblioteca](#header-and-library-files)
-   [Variables globales](#global-variables)
-   [Declarar la clase de devolución de llamada](#declare-the-callback-class)
-   [Declarar la función SafeRelease](#declare-the-saferelease-function)
-   [Abrir un archivo multimedia](#open-a-media-file)
-   [Controladores de mensajes de ventana](#window-message-handlers)
-   [Implementar el método de devolución de llamada](#implement-the-callback-method)
-   [Implementar WinMain](#implement-winmain)
-   [Temas relacionados](#related-topics)

Para obtener una explicación más detallada de la API de MFPlay, consulte [Introducción con MFPlay](getting-started-with-mfplay.md).

## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="header-and-library-files"></a>Archivos de encabezado y de biblioteca

Incluya los siguientes archivos de encabezado en el proyecto:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



Vínculo a las siguientes bibliotecas de código:

-   mfplay. lib
-   shlwapi. lib

## <a name="global-variables"></a>Variables globales

Declare las variables globales siguientes:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Estas variables se utilizarán de la siguiente manera:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ hWnd*
</dt> <dd>

Identificador de la ventana de la aplicación.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*
</dt> <dd>

Un valor booleano que realiza un seguimiento de si el vídeo se está reproduciendo.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*
</dt> <dd>

Puntero a la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Esta interfaz se utiliza para controlar la reproducción.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

Puntero a la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . La aplicación implementa esta interfaz de devolución de llamada para obtener notificaciones del objeto de reproductor.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Declarar la clase de devolución de llamada

Para obtener notificaciones de eventos del objeto Player, la aplicación debe implementar la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . El código siguiente declara una clase que implementa la interfaz. La única variable miembro es *m \_ cRef*, que almacena el recuento de referencias.

Los métodos **IUnknown** se implementan en línea. La implementación del método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) se muestra más adelante. vea [implementar el método de devolución de llamada](#implement-the-callback-method).


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a>Declarar la función SafeRelease

En este tutorial, la función [SafeRelease](saferelease.md) se usa para liberar punteros de interfaz:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a>Abrir un archivo multimedia

La `PlayMediaFile` función abre un archivo multimedia, como se indica a continuación:

1.  Si *g \_ PPlayer* es **null**, la función llama a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para crear una nueva instancia del objeto del reproductor de media. Los parámetros de entrada para **MFPCreateMediaPlayer** incluyen un puntero a la interfaz de devolución de llamada y un identificador a la ventana de vídeo.
2.  Para abrir el archivo multimedia, la función llama a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), pasando la dirección URL del archivo. Este método se completa de forma asincrónica. Cuando se completa, se llama al método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) de la aplicación.


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



La `OnFileOpen` función muestra el cuadro de diálogo de archivo común, que permite al usuario seleccionar un archivo para su reproducción. La interfaz **IFileOpenDialog** se usa para mostrar el cuadro de diálogo de archivo común. Esta interfaz forma parte de las API del shell de Windows; se presentó en Windows Vista como un sustituto de la función **GetOpenFileName** anterior. Una vez que el usuario selecciona un archivo, `OnFileOpen` llama `PlayMediaFile` a para iniciar la reproducción.


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a>Controladores de mensajes de ventana

A continuación, declare los controladores de mensajes para los siguientes mensajes de ventana:

-   **pintura de WM \_**
-   **tamaño de WM \_**
-   **cierre de WM \_**

En el caso del mensaje de **\_ Paint de WM** , debe realizar un seguimiento de si el vídeo se está reproduciendo actualmente. En ese caso, llame al método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) . Este método hace que el objeto Player vuelva a dibujar el fotograma de vídeo más reciente.

Si no hay ningún vídeo, la aplicación es responsable de pintar la ventana. En este tutorial, la aplicación simplemente llama a la función GDI **FillRect** para rellenar el área de cliente completa.


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



Para el mensaje de **\_ tamaño de WM** , llame a [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo). Este método hace que el objeto Player reajuste el vídeo para que coincida con el tamaño actual de la ventana. Tenga en cuenta que **UpdateVideo** se usa para la **\_ pintura de WM** y **\_ el tamaño de WM**.


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



Para el mensaje de **\_ cierre de WM** , libere los punteros [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) y [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implementar el método de devolución de llamada

La interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) define un método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Este método notifica a la aplicación cada vez que se produce un evento durante la reproducción. El método toma un parámetro, un puntero a una estructura de [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . El miembro **eEventType** de la estructura especifica el evento que se ha producido.

La estructura del [**\_ \_ encabezado del evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) puede ir seguida de datos adicionales. Para cada tipo de evento, se define una macro que convierte el puntero del **\_ \_ encabezado de evento MFP** en una estructura específica del evento. (Consulte [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)).

En este tutorial, dos eventos son significativos:



| Evento                                    | Descripción                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_tipo de evento MFP \_ \_ MEDIAITEM \_ creado** | Se envía cuando se completa la [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . |
| **\_tipo de evento MFP \_ \_ MEDIAITEM \_ establecido**     | Se envía cuando se completa [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) .                         |



 

En el código siguiente se muestra cómo convertir el puntero del [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en la estructura específica del evento.


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



El evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ creado** notifica a la aplicación que el método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) se ha completado. La estructura de eventos contiene un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que representa el elemento multimedia creado a partir de la dirección URL. Para poner en cola el elemento para la reproducción, pase este puntero al método [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



El evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** notifica a la aplicación que [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) se ha completado. Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar la reproducción:


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a>Implementar WinMain

En el resto de este tutorial, no hay ninguna llamada a Media Foundation API. En el código siguiente se muestra el procedimiento de ventana:


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



La `InitializeWindow` función registra la clase de ventana de la aplicación y crea la ventana.


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



Por último, implemente el punto de entrada de la aplicación:


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



