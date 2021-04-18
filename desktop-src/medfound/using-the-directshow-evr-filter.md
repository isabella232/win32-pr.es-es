---
description: Usar el filtro EVR de DirectShow
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Usar el filtro EVR de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687306"
---
# <a name="using-the-directshow-evr-filter"></a>Usar el filtro EVR de DirectShow

Para crear el filtro de representador de vídeo mejorado (EVR), llame a **CoCreateInstance**. El CLSID es CLSID \_ EnhancedVideoRenderer, definido en UUID. h. No es necesario llamar a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para usar el filtro EVR.

Para obtener más información sobre el uso del filtro EVR en una aplicación de DirectShow, vea [reproducción de audio y vídeo en DirectShow](../directshow/audio-video-playback-in-directshow.md).

El filtro EVR se inicia con un PIN de entrada, que corresponde a la secuencia de referencia. Para agregar PIN para subflujos, consulte el filtro de la interfaz [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) y llame a [**IEVRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams). Llame a este método antes de conectar cualquier clavija de entrada. El pin 0 siempre es el flujo de referencia. Conecte este PIN antes de cualquier otro PIN, ya que el formato del flujo de referencia puede limitar los formatos de subsecuencia que están disponibles.

Antes de iniciar el gráfico, establezca la ventana de recorte de vídeo y el rectángulo de destino. Para obtener más información, vea [usar los controles de presentación de vídeo](using-the-video-display-controls.md).

A diferencia del representador de mezcla de vídeo (VMR), EVR no tiene modos operativos (windowed, Windowless, etc.). En concreto:

-   EVR no admite el modo de ventana. La aplicación debe proporcionar la ventana de recorte.
-   EVR no tiene un modo sin procesar. Para reemplazar el presentador predeterminado, llame a [**IMFVideoRenderer:: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).
-   El EVR no tiene un modo de mezcla. EVR siempre crea el mezclador. Si tiene un flujo de entrada, no es necesario llamar a [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) para obligar a EVR a usar el mezclador.

## <a name="filter-interfaces"></a>Interfaces de filtro

El filtro EVR expone las siguientes interfaces. Algunas de estas interfaces se documentan en el SDK de DirectShow. Use **QueryInterface** para recuperar punteros a estas interfaces:

-   [**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)
-   [**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)
-   [**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)
-   [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   [**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)
-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   **IPersistStream**
-   [**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)
-   [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)
-   **ISpecifyPropertyPages**

## <a name="input-pin-interfaces"></a>Interfaces de PIN de entrada

Los pin de entrada del filtro EVR exponen las interfaces siguientes. Use **QueryInterface** para recuperar punteros a estas interfaces:

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

 

 
