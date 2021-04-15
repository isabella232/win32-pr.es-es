---
description: Filtro tee de anclaje infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro tee de anclaje infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423007"
---
# <a name="infinite-pin-tee-filter"></a>Filtro tee de anclaje infinito

Este filtro proporciona ejemplos entregados a su PIN de entrada a un número variable de clavijas de salida. Cuando se crea una instancia del filtro, tiene un PIN de salida. Cada vez que se conecta un PIN de salida, el filtro crea otro PIN de salida. Todos los pin de salida comparten el mismo tipo de medio que el PIN de entrada.

También se proporciona una versión de este filtro como ejemplo de SDK. Vea [ejemplo de filtro InfTee](inftee-filter-sample.md).



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de anclaje de entrada                    | Cualquier tipo de medio                                                                                                                                     |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de anclaje de salida                   | Cualquier tipo de medio. El tipo de salida siempre coincide con el tipo de entrada para todos los pin de salida                                                                 |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



