---
description: Resumen de subprocesos de filtro
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Resumen de subprocesos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c151ed5fe69eea4cb0c81d01f43e97790b7223970791d3717adb9e15bea41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951744"
---
# <a name="summary-of-filter-threading"></a>Resumen de subprocesos de filtro

Se llama a los métodos siguientes en el subproceso de streaming:

-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

Se llama a los métodos siguientes en el subproceso de aplicación:

-   Cambios de estado: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).
-   Reloj de referencia: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).
-   Operaciones de anclar: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Conectar**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).
-   Funciones de asignador: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).
-   Vaciado: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).

Esta lista no es exhaustiva. Al implementar un filtro, debe tener en cuenta qué métodos cambian el estado del filtro y qué métodos realizan operaciones de streaming.

 

 



