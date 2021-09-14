---
description: Administrador de Graph filtros
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Administrador de Graph filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169973"
---
# <a name="filter-graph-manager"></a>Administrador de Graph filtros

Filter Graph Manager compila y controla los gráficos de filtro. Este objeto es el componente central de DirectShow. Las aplicaciones lo usan para compilar y controlar gráficos de filtro. Filter Graph Manager también controla la sincronización, la notificación de eventos y otros aspectos del control del gráfico de filtros. Cree este objeto mediante una llamada **a CoCreateInstance**.

### <a name="clsid"></a>CLSID

Hay dos CLSID para crear el Administrador de filtros Graph Manager:



| CLSID                      | Descripción                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | Crea el Administrador de Graph en un subproceso de trabajo compartido. |
| CLSID \_ FilterGraphNoThread | Crea el Administrador de Graph en el subproceso de aplicación. |



 

Por lo general, las aplicaciones deben usar CLSID \_ FilterGraph. Ambos CLSID crean el mismo objeto, pero usan diferentes modelos de subprocesos:

-   CLSID FilterGraph crea el Administrador de Graph en un subproceso de trabajo, que comparten todas las instancias de \_ CLSID FilterGraph dentro \_ del mismo proceso. El subproceso envía mensajes enviados por filtros y controla la duración de las ventanas creadas por filtros.
-   CLSID \_ FilterGraphNoThread crea el Administrador de Graph en el subproceso de la aplicación. Si usa este CLSID, el subproceso que llama a **CoCreateInstance** debe tener un bucle de mensajes que envíe mensajes; De lo contrario, pueden producirse interbloqueos. Además, antes de que se cierre el subproceso de aplicación, debe liberar el Administrador de filtros Graph y todos los objetos de grafo (como filtros, pasadores, relojes de referencia, etc.).

### <a name="interfaces"></a>Interfaces

El Administrador Graph filtros expone las interfaces siguientes:

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

[DirectShow Objetos](directshow-objects.md)
</dt> </dl>

 

 



