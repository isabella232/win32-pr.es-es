---
description: Interfaces para generar gráficos de filtros
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces para generar gráficos de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805659"
---
# <a name="interfaces-for-building-filter-graphs"></a>Interfaces para generar gráficos de filtros

Las aplicaciones usan estas interfaces para crear varios tipos de gráficos de filtros.



| Interfaz                                                  | Descripción                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Recibir notificaciones de devolución de llamada si no se puede representar un PIN. |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Proporciona un mecanismo de devolución de llamada durante la creación del gráfico.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Cree gráficos de filtro para la captura de vídeo.                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Enumerar dispositivos del sistema, como dispositivos de captura.          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Cree gráficos de filtros para la reproducción y la navegación de DVD.        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Enumera los filtros del gráfico.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Agregar, quitar o conectar filtros.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Enumera los filtros registrados en el sistema del usuario.      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Cree gráficos de filtro para la reproducción de archivos o para usos personalizados.   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Reconfigure dinámicamente un gráfico de filtro.                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Determine cuándo cambia el gráfico.                           |



 

 

 



