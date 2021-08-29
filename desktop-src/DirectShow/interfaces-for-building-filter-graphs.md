---
description: Interfaces para crear gráficos de filtro
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces para crear gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ca539672f39e855d891a5a3c534a8ac3cfcec35bb933034bad2621fa5339d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154133"
---
# <a name="interfaces-for-building-filter-graphs"></a>Interfaces para crear gráficos de filtro

Las aplicaciones usan estas interfaces para crear varios tipos de gráficos de filtro.



| Interfaz                                                  | Descripción                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Recibir notificaciones de devolución de llamada si no se puede representar un pin. |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Proporciona un mecanismo de devolución de llamada durante la creación del grafo.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Cree gráficos de filtro para la captura de vídeo.                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Enumerar los dispositivos del sistema, como los dispositivos de captura.          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Cree gráficos de filtro para la navegación y reproducción de DVD.        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Enumerar los filtros en el gráfico.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Agregar, quitar o conectar filtros.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Enumerar los filtros registrados en el sistema del usuario.      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Cree gráficos de filtro para la reproducción de archivos o para usos personalizados.   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Vuelva a configurar dinámicamente un gráfico de filtros.                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Determine cuándo cambia el gráfico.                           |



 

 

 



