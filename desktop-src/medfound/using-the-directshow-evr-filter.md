---
description: Uso del DirectShow EVR
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Uso del DirectShow EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468593"
---
# <a name="using-the-directshow-evr-filter"></a>Uso del DirectShow EVR

Para crear el filtro de representador de vídeo mejorado (EVR), llame **a CoCreateInstance**. CLSID es CLSID \_ EnhancedVideoRenderer, definido en uuids.h. No es necesario llamar a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ni [**MFShutdown para**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) usar el filtro EVR.

Para obtener más información sobre el uso del filtro EVR en una DirectShow, vea Reproducción de audio y vídeo [en DirectShow](../directshow/audio-video-playback-in-directshow.md).

El filtro EVR comienza con un pin de entrada, que corresponde a la secuencia de referencia. Para agregar pins para substreams, consulte el filtro de la interfaz [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) y llame a [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Llame a este método antes de conectar los pines de entrada. El pin 0 siempre es la secuencia de referencia. Conectar este pin antes que cualquier otro pin, ya que el formato de la secuencia de referencia puede limitar qué formatos de subtransmisión están disponibles.

Antes de iniciar el gráfico, establezca la ventana de recorte de vídeo y el rectángulo de destino. Para obtener más información, vea [Usar los controles de visualización de vídeo.](using-the-video-display-controls.md)

A diferencia del representador de mezcla de vídeo (VMR), el EVR no tiene modos operativos (ventanas, sin ventanas, etc.). En concreto:

-   EvR no admite el modo en ventanas. La aplicación debe proporcionar la ventana de recorte.
-   El EVR no tiene un modo sin representación. Para reemplazar el presentador predeterminado, llame [**a IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   La EVR no tiene un modo de combinación. La EVR siempre crea el mezclador. Si tiene un flujo de entrada, no es necesario llamar a [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para forzar al EVR a usar el mezclador.

## <a name="filter-interfaces"></a>Interfaces de filtro

El filtro EVR expone las interfaces siguientes. Algunas de estas interfaces se documentan en el SDK DirectShow. Use **QueryInterface para** recuperar punteros a estas interfaces:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**RENDERERVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **Ipersiststream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfaces de pin de entrada

Los pines de entrada del filtro EVR exponen las interfaces siguientes. Use **QueryInterface para** recuperar punteros a estas interfaces:

-   [**IEVRVideoStreamControl**](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   [**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)

Además, puede usar la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para recuperar la siguiente interfaz:

-   [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 
