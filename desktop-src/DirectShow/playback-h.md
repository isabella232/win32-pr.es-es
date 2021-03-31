---
description: Este tema contiene código para la reproducción de audio y vídeo del tutorial en DirectShow.
ms.assetid: 8cf0f281-3680-4329-80d0-8282d1051c1a
title: reproducción. h
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03bd6ebd1d0b37c0351fbbe1b4e7906b243ffc7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805228"
---
# <a name="playbackh"></a><span data-ttu-id="4ce0e-103">reproducción. h</span><span class="sxs-lookup"><span data-stu-id="4ce0e-103">playback.h</span></span>

<span data-ttu-id="4ce0e-104">Este tema contiene código para la [reproducción de audio y vídeo del tutorial en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="4ce0e-104">This topic contains code for the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.

#pragma once

class CVideoRenderer;

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



## <a name="related-topics"></a><span data-ttu-id="4ce0e-105">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ce0e-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ce0e-106">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ce0e-106">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="4ce0e-107">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="4ce0e-107">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> </dl>

 

 



