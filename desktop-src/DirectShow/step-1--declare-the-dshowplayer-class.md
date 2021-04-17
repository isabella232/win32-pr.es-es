---
description: En este tema se trata el paso 1 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Paso 1: declarar la clase DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678089"
---
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="7b7da-103">Paso 1: declarar la clase DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="7b7da-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="7b7da-104">En este tema se trata el paso 1 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="7b7da-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="7b7da-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="7b7da-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="7b7da-106">En este tutorial, la `DShowPlayer` clase administra toda la funcionalidad de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b7da-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="7b7da-107">Esta clase se declara como folows.</span><span class="sxs-lookup"><span data-stu-id="7b7da-107">This class is declared as folows.</span></span>


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





<span data-ttu-id="7b7da-108">Notas:</span><span class="sxs-lookup"><span data-stu-id="7b7da-108">Notes:</span></span>

-   <span data-ttu-id="7b7da-109">La `PlaybackState` enumeración describe el estado actual del `DShowPlayer` objeto.</span><span class="sxs-lookup"><span data-stu-id="7b7da-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="7b7da-110">El evento de gráfico de WM constante \_ \_ define un mensaje de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="7b7da-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="7b7da-111">Este mensaje se utiliza para notificar a la aplicación sobre los eventos de gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="7b7da-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="7b7da-112">Vea [paso 6: controlar eventos de gráfico](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="7b7da-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="7b7da-113">`GraphEventFN` es un puntero a una función de devolución de llamada para controlar los eventos de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7b7da-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="7b7da-114">La aplicación implementa esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="7b7da-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="7b7da-115">La variable miembro *m \_ pVideo* proporciona un contenedor para los distintos representadores de vídeo de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b7da-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="7b7da-116">Vea [Step 2: declare CVideoRenderer and derived classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7b7da-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="7b7da-117">En este tutorial, la función [SafeRelease](../medfound/saferelease.md) se usa para liberar punteros de interfaz com.</span><span class="sxs-lookup"><span data-stu-id="7b7da-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="7b7da-118">Siguiente: [paso 2: declarar CVideoRenderer y las clases derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7b7da-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b7da-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b7da-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7da-120">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7b7da-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
