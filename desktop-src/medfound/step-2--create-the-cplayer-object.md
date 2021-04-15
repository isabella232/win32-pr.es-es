---
description: En este tema se describe el paso 2 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Paso 2: crear el objeto CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715483"
---
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="03b78-103">Paso 2: crear el objeto CPlayer</span><span class="sxs-lookup"><span data-stu-id="03b78-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="03b78-104">En este tema se describe el paso 2 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="03b78-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="03b78-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="03b78-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="03b78-106">Para crear una instancia de la `CPlayer` clase, la aplicación llama al `CPlayer::CreateInstance` método estático.</span><span class="sxs-lookup"><span data-stu-id="03b78-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="03b78-107">Este método toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="03b78-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="03b78-108">*hVideo* especifica la ventana en la que se va a mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="03b78-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="03b78-109">*hEvent* especifica una ventana para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="03b78-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="03b78-110">Es válido pasar el mismo identificador para ambos identificadores de ventana.</span><span class="sxs-lookup"><span data-stu-id="03b78-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="03b78-111">*ppPlayer* recibe un puntero a una nueva `CPlayer` instancia de.</span><span class="sxs-lookup"><span data-stu-id="03b78-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="03b78-112">En el código siguiente se muestra el método `CreateInstance`:</span><span class="sxs-lookup"><span data-stu-id="03b78-112">The following code shows the `CreateInstance` method:</span></span>


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



<span data-ttu-id="03b78-113">En el código siguiente se muestra el `CPlayer` constructor:</span><span class="sxs-lookup"><span data-stu-id="03b78-113">The following code shows the `CPlayer` constructor:</span></span>


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



<span data-ttu-id="03b78-114">El constructor realiza lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="03b78-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="03b78-115">Llama a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="03b78-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="03b78-116">Crea un evento de restablecimiento automático.</span><span class="sxs-lookup"><span data-stu-id="03b78-116">Creates an auto-reset event.</span></span> <span data-ttu-id="03b78-117">Este evento se utiliza al cerrar la sesión multimedia; vea [paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="03b78-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="03b78-118">El destructor cierra la sesión multimedia, como se describe en [el paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="03b78-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



<span data-ttu-id="03b78-119">Tenga en cuenta que el constructor y el destructor son métodos de clase protegidos.</span><span class="sxs-lookup"><span data-stu-id="03b78-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="03b78-120">La aplicación crea el objeto mediante el `CreateInstance` método estático.</span><span class="sxs-lookup"><span data-stu-id="03b78-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="03b78-121">Destruye el objeto llamando a **IUnknown:: Release**, en lugar de usar explícitamente **Delete**.</span><span class="sxs-lookup"><span data-stu-id="03b78-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="03b78-122">Siguiente: [paso 3: abrir un archivo multimedia](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="03b78-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b78-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03b78-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b78-124">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="03b78-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="03b78-125">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03b78-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



