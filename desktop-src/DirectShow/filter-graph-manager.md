---
description: Filtrar el administrador de gráficos
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Filtrar el administrador de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906353"
---
# <a name="filter-graph-manager"></a>Filtrar el administrador de gráficos

El administrador de gráficos de filtros genera y controla los gráficos de filtros. Este objeto es el componente central de DirectShow. Las aplicaciones lo utilizan para compilar y controlar gráficos de filtros. El administrador de gráficos de filtro también controla la sincronización, la notificación de eventos y otros aspectos del control del gráfico de filtro. Cree este objeto llamando a **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Hay dos CLSID para crear el administrador de gráficos de filtro:



| CLSID                      | Descripción                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | Crea el administrador de gráficos de filtro en un subproceso de trabajo compartido. |
| CLSID \_ FilterGraphNoThread | Crea el administrador de gráficos de filtro en el subproceso de la aplicación. |



 

Por lo general, las aplicaciones deben usar CLSID \_ FilterGraph. Ambos CLSID crean el mismo objeto, pero usan diferentes modelos de subprocesos:

-   CLSID \_ FilterGraph crea el administrador de gráficos de filtro en un subproceso de trabajo, que comparten todas \_ las instancias de FILTERGRAPH de CLSID dentro del mismo proceso. El subproceso envía los mensajes enviados por los filtros y controla la duración de las ventanas creadas por los filtros.
-   CLSID \_ FilterGraphNoThread crea el administrador de gráficos de filtro en el subproceso de la aplicación. Si usa este CLSID, el subproceso que llama a **CoCreateInstance** debe tener un bucle de mensajes que envíe los mensajes; de lo contrario, pueden producirse interbloqueos. Además, antes de que el subproceso de la aplicación salga, debe liberar el administrador de gráficos de filtro y todos los objetos de gráfico (como filtros, PIN, relojes de referencia, etc.).

### <a name="interfaces"></a>Interfaces

El administrador de gráficos de filtro expone las siguientes interfaces:

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de DirectShow](directshow-objects.md)
</dt> </dl>

 

 



