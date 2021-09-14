---
description: Este tema es el paso 1 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Paso 1: Declarar la clase DShowPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127275087"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>Paso 1: Declarar la clase DShowPlayer

Este tema es el paso 1 del tutorial [Reproducción de audio](audio-video-playback-in-directshow.md)y vídeo en DirectShow . El código completo se muestra en el tema DirectShow [Ejemplo de reproducción](directshow-playback-example.md).

En este tutorial, la `DShowPlayer` clase administra todas las DirectShow funcionalidad. Esta clase se declara como folows.


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





Notas:

-   La `PlaybackState` enumeración describe el estado actual del `DShowPlayer` objeto .
-   La constante WM \_ GRAPH EVENT define un mensaje de ventana \_ privada. Este mensaje se usa para notificar a la aplicación sobre eventos de gráfico de filtro. Vea [Step 6: Handle Graph Events](step-6--handle-graph-events.md).
-   `GraphEventFN` es un puntero a una función de devolución de llamada para controlar eventos de gráfico de filtro. La aplicación implementa esta función de devolución de llamada.
-   La *variable miembro m \_ pVideo* proporciona un contenedor para los distintos DirectShow de vídeo. Vea [Paso 2: Declarar CVideoRenderer y clases derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).
-   A lo largo de este tutorial, se usa la función [SafeRelease](../medfound/saferelease.md) para liberar punteros de interfaz COM.

Siguiente: [Paso 2: Declarar CVideoRenderer y clases derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 
