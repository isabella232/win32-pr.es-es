---
description: Este artículo contiene código para el archivo playback.h del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 8cf0f281-3680-4329-80d0-8282d1051c1a
title: playback.h
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52dc50cd14b26bcd26284a62c96400706d8aa8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405118"
---
# <a name="playbackh"></a><span data-ttu-id="0aad7-103">playback.h</span><span class="sxs-lookup"><span data-stu-id="0aad7-103">playback.h</span></span>

<span data-ttu-id="0aad7-104">Este tema contiene código para el tutorial [Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0aad7-104">This topic contains code for the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0aad7-105">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aad7-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aad7-106">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="0aad7-106">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0aad7-107">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0aad7-107">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> </dl>

 

 



