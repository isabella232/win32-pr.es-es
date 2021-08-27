---
description: Este tema es el paso 2 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Paso 2: Declarar CVideoRenderer y clases derivadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae4c9c391a13acd0ede06b9a74c3b09bd264a6b74c42d7f6c7ca5e9dbb17051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050365"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Paso 2: Declarar CVideoRenderer y clases derivadas

Este tema es el paso 2 del tutorial [Reproducción de audio y](audio-video-playback-in-directshow.md)vídeo en DirectShow . El código completo se muestra en el tema DirectShow [Ejemplo de reproducción](directshow-playback-example.md).

DirectShow proporciona varios filtros diferentes que representan vídeo:

-   [**Filtro de representador de vídeo**](enhanced-video-renderer-filter.md) mejorado (EVR)
-   [Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Para obtener más información sobre las diferencias entre estos filtros, vea [Elección del representador de vídeo correcto.](choosing-the-right-renderer.md)

En este tutorial, se usa la siguiente clase abstracta para encapsular el filtro del representador de vídeo.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Notas:

-   El `HasVideo` método devuelve TRUE **si** se ha creado el representador de vídeo.
-   El `AddToGraph` método agrega el representador de vídeo al gráfico de filtro.
-   El `FinalizeGraph` método completa el paso de creación de grafos.
-   El `UpdateVideoWindow` método actualiza el rectángulo de destino del vídeo.
-   El `Repaint` método vuelve a dibujar el fotograma de vídeo actual.
-   El `DisplayModeChanged` método controla los cambios en modo de presentación.

Cada uno de estos métodos se describe en detalle más adelante en este tutorial.

A continuación, declare una clase derivada para encapsular cada uno de los tres representadores de vídeo: EVR, VMR-9 y VMR-7.

### <a name="cevr-class"></a>CEVR (clase)

La `CEVR` clase administra la EVR. Contiene un puntero a las interfaces [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**y IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) de la EVR.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>CVMR9 (clase)

La `CVMR9` clase administra vmr-9. Contiene un puntero a la [**interfaz IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>CVMR7 (clase)

La `CVMR7` clase administra vmr-7. Contiene un puntero a la [**interfaz IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



Siguiente: [Paso 3: Compilar el filtro Graph](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Uso del representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> <dt>

[Representación de vídeo](video-rendering.md)
</dt> </dl>

 

 
