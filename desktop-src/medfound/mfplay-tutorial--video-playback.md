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
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="50b66-103">Tutorial de MFPlay: reproducción de vídeo</span><span class="sxs-lookup"><span data-stu-id="50b66-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="50b66-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="50b66-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50b66-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="50b66-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="50b66-106">\]</span><span class="sxs-lookup"><span data-stu-id="50b66-106">\]</span></span>

<span data-ttu-id="50b66-107">En este tutorial se presenta una aplicación completa que reproduce vídeo mediante MFPlay.</span><span class="sxs-lookup"><span data-stu-id="50b66-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="50b66-108">Se basa en el ejemplo de SDK de [SimplePlay](simpleplay-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="50b66-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="50b66-109">Este tutorial contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="50b66-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="50b66-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b66-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="50b66-111">Archivos de encabezado y de biblioteca</span><span class="sxs-lookup"><span data-stu-id="50b66-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="50b66-112">Variables globales</span><span class="sxs-lookup"><span data-stu-id="50b66-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="50b66-113">Declarar la clase de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="50b66-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="50b66-114">Declarar la función SafeRelease</span><span class="sxs-lookup"><span data-stu-id="50b66-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="50b66-115">Abrir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="50b66-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="50b66-116">Controladores de mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="50b66-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="50b66-117">Implementar el método de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="50b66-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="50b66-118">Implementar WinMain</span><span class="sxs-lookup"><span data-stu-id="50b66-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="50b66-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50b66-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="50b66-120">Para obtener una explicación más detallada de la API de MFPlay, consulte [Introducción con MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="50b66-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50b66-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b66-121">Requirements</span></span>

<span data-ttu-id="50b66-122">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50b66-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="50b66-123">Archivos de encabezado y de biblioteca</span><span class="sxs-lookup"><span data-stu-id="50b66-123">Header and Library Files</span></span>

<span data-ttu-id="50b66-124">Incluya los siguientes archivos de encabezado en el proyecto:</span><span class="sxs-lookup"><span data-stu-id="50b66-124">Include the following header files in your project:</span></span>


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



<span data-ttu-id="50b66-125">Vínculo a las siguientes bibliotecas de código:</span><span class="sxs-lookup"><span data-stu-id="50b66-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="50b66-126">mfplay. lib</span><span class="sxs-lookup"><span data-stu-id="50b66-126">mfplay.lib</span></span>
-   <span data-ttu-id="50b66-127">shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="50b66-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="50b66-128">Variables globales</span><span class="sxs-lookup"><span data-stu-id="50b66-128">Global Variables</span></span>

<span data-ttu-id="50b66-129">Declare las variables globales siguientes:</span><span class="sxs-lookup"><span data-stu-id="50b66-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="50b66-130">Estas variables se utilizarán de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="50b66-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="50b66-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ hWnd*</span><span class="sxs-lookup"><span data-stu-id="50b66-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="50b66-132">Identificador de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b66-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="50b66-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*</span><span class="sxs-lookup"><span data-stu-id="50b66-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="50b66-134">Un valor booleano que realiza un seguimiento de si el vídeo se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="50b66-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="50b66-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*</span><span class="sxs-lookup"><span data-stu-id="50b66-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="50b66-136">Puntero a la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="50b66-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="50b66-137">Esta interfaz se utiliza para controlar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="50b66-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="50b66-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*</span><span class="sxs-lookup"><span data-stu-id="50b66-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="50b66-139">Puntero a la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="50b66-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="50b66-140">La aplicación implementa esta interfaz de devolución de llamada para obtener notificaciones del objeto de reproductor.</span><span class="sxs-lookup"><span data-stu-id="50b66-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="50b66-141">Declarar la clase de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="50b66-141">Declare the Callback Class</span></span>

<span data-ttu-id="50b66-142">Para obtener notificaciones de eventos del objeto Player, la aplicación debe implementar la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="50b66-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="50b66-143">El código siguiente declara una clase que implementa la interfaz.</span><span class="sxs-lookup"><span data-stu-id="50b66-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="50b66-144">La única variable miembro es *m \_ cRef*, que almacena el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="50b66-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="50b66-145">Los métodos **IUnknown** se implementan en línea.</span><span class="sxs-lookup"><span data-stu-id="50b66-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="50b66-146">La implementación del método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) se muestra más adelante. vea [implementar el método de devolución de llamada](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="50b66-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


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



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="50b66-147">Declarar la función SafeRelease</span><span class="sxs-lookup"><span data-stu-id="50b66-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="50b66-148">En este tutorial, la función [SafeRelease](saferelease.md) se usa para liberar punteros de interfaz:</span><span class="sxs-lookup"><span data-stu-id="50b66-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


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



## <a name="open-a-media-file"></a><span data-ttu-id="50b66-149">Abrir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="50b66-149">Open a Media File</span></span>

<span data-ttu-id="50b66-150">La `PlayMediaFile` función abre un archivo multimedia, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50b66-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="50b66-151">Si *g \_ PPlayer* es **null**, la función llama a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para crear una nueva instancia del objeto del reproductor de media.</span><span class="sxs-lookup"><span data-stu-id="50b66-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="50b66-152">Los parámetros de entrada para **MFPCreateMediaPlayer** incluyen un puntero a la interfaz de devolución de llamada y un identificador a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50b66-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="50b66-153">Para abrir el archivo multimedia, la función llama a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), pasando la dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="50b66-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="50b66-154">Este método se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="50b66-154">This method completes asynchronously.</span></span> <span data-ttu-id="50b66-155">Cuando se completa, se llama al método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b66-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


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



<span data-ttu-id="50b66-156">La `OnFileOpen` función muestra el cuadro de diálogo de archivo común, que permite al usuario seleccionar un archivo para su reproducción.</span><span class="sxs-lookup"><span data-stu-id="50b66-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="50b66-157">La interfaz **IFileOpenDialog** se usa para mostrar el cuadro de diálogo de archivo común.</span><span class="sxs-lookup"><span data-stu-id="50b66-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="50b66-158">Esta interfaz forma parte de las API del shell de Windows; se presentó en Windows Vista como un sustituto de la función **GetOpenFileName** anterior.</span><span class="sxs-lookup"><span data-stu-id="50b66-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="50b66-159">Una vez que el usuario selecciona un archivo, `OnFileOpen` llama `PlayMediaFile` a para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="50b66-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


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



## <a name="window-message-handlers"></a><span data-ttu-id="50b66-160">Controladores de mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="50b66-160">Window Message Handlers</span></span>

<span data-ttu-id="50b66-161">A continuación, declare los controladores de mensajes para los siguientes mensajes de ventana:</span><span class="sxs-lookup"><span data-stu-id="50b66-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="50b66-162">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="50b66-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="50b66-163">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="50b66-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="50b66-164">**cierre de WM \_**</span><span class="sxs-lookup"><span data-stu-id="50b66-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="50b66-165">En el caso del mensaje de **\_ Paint de WM** , debe realizar un seguimiento de si el vídeo se está reproduciendo actualmente.</span><span class="sxs-lookup"><span data-stu-id="50b66-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="50b66-166">En ese caso, llame al método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) .</span><span class="sxs-lookup"><span data-stu-id="50b66-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="50b66-167">Este método hace que el objeto Player vuelva a dibujar el fotograma de vídeo más reciente.</span><span class="sxs-lookup"><span data-stu-id="50b66-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="50b66-168">Si no hay ningún vídeo, la aplicación es responsable de pintar la ventana.</span><span class="sxs-lookup"><span data-stu-id="50b66-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="50b66-169">En este tutorial, la aplicación simplemente llama a la función GDI **FillRect** para rellenar el área de cliente completa.</span><span class="sxs-lookup"><span data-stu-id="50b66-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


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



<span data-ttu-id="50b66-170">Para el mensaje de **\_ tamaño de WM** , llame a [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="50b66-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="50b66-171">Este método hace que el objeto Player reajuste el vídeo para que coincida con el tamaño actual de la ventana.</span><span class="sxs-lookup"><span data-stu-id="50b66-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="50b66-172">Tenga en cuenta que **UpdateVideo** se usa para la **\_ pintura de WM** y **\_ el tamaño de WM**.</span><span class="sxs-lookup"><span data-stu-id="50b66-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


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



<span data-ttu-id="50b66-173">Para el mensaje de **\_ cierre de WM** , libere los punteros [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) y [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="50b66-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="50b66-174">Implementar el método de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="50b66-174">Implement the Callback Method</span></span>

<span data-ttu-id="50b66-175">La interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) define un método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="50b66-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="50b66-176">Este método notifica a la aplicación cada vez que se produce un evento durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="50b66-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="50b66-177">El método toma un parámetro, un puntero a una estructura de [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="50b66-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="50b66-178">El miembro **eEventType** de la estructura especifica el evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="50b66-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="50b66-179">La estructura del [**\_ \_ encabezado del evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) puede ir seguida de datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="50b66-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="50b66-180">Para cada tipo de evento, se define una macro que convierte el puntero del **\_ \_ encabezado de evento MFP** en una estructura específica del evento.</span><span class="sxs-lookup"><span data-stu-id="50b66-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="50b66-181">(Consulte [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)).</span><span class="sxs-lookup"><span data-stu-id="50b66-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="50b66-182">En este tutorial, dos eventos son significativos:</span><span class="sxs-lookup"><span data-stu-id="50b66-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="50b66-183">Evento</span><span class="sxs-lookup"><span data-stu-id="50b66-183">Event</span></span>                                    | <span data-ttu-id="50b66-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="50b66-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b66-185">**\_tipo de evento MFP \_ \_ MEDIAITEM \_ creado**</span><span class="sxs-lookup"><span data-stu-id="50b66-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="50b66-186">Se envía cuando se completa la [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="50b66-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="50b66-187">**\_tipo de evento MFP \_ \_ MEDIAITEM \_ establecido**</span><span class="sxs-lookup"><span data-stu-id="50b66-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="50b66-188">Se envía cuando se completa [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="50b66-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="50b66-189">En el código siguiente se muestra cómo convertir el puntero del [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) en la estructura específica del evento.</span><span class="sxs-lookup"><span data-stu-id="50b66-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


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



<span data-ttu-id="50b66-190">El evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ creado** notifica a la aplicación que el método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) se ha completado.</span><span class="sxs-lookup"><span data-stu-id="50b66-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="50b66-191">La estructura de eventos contiene un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que representa el elemento multimedia creado a partir de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="50b66-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="50b66-192">Para poner en cola el elemento para la reproducción, pase este puntero al método [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :</span><span class="sxs-lookup"><span data-stu-id="50b66-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


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



<span data-ttu-id="50b66-193">El evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** notifica a la aplicación que [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) se ha completado.</span><span class="sxs-lookup"><span data-stu-id="50b66-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="50b66-194">Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar la reproducción:</span><span class="sxs-lookup"><span data-stu-id="50b66-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


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



## <a name="implement-winmain"></a><span data-ttu-id="50b66-195">Implementar WinMain</span><span class="sxs-lookup"><span data-stu-id="50b66-195">Implement WinMain</span></span>

<span data-ttu-id="50b66-196">En el resto de este tutorial, no hay ninguna llamada a Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="50b66-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="50b66-197">En el código siguiente se muestra el procedimiento de ventana:</span><span class="sxs-lookup"><span data-stu-id="50b66-197">The following code shows the window procedure:</span></span>


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



<span data-ttu-id="50b66-198">La `InitializeWindow` función registra la clase de ventana de la aplicación y crea la ventana.</span><span class="sxs-lookup"><span data-stu-id="50b66-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


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



<span data-ttu-id="50b66-199">Por último, implemente el punto de entrada de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="50b66-199">Finally, implement the application entry point:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="50b66-200">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50b66-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b66-201">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="50b66-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



