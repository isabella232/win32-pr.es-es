---
description: Filtro de tee de pin infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de tee de pin infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28edb67da9d6aae01786cece43b45dfcd33d571b82bdbab21ecf82a2473ff0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818790"
---
# <a name="infinite-pin-tee-filter"></a>Filtro de tee de pin infinito

Este filtro entrega ejemplos entregados a su pin de entrada a un número variable de pines de salida. Cuando se crea una instancia del filtro, tiene un pin de salida. Cada vez que se conecta un pin de salida, el filtro crea otro pin de salida. Todos los pines de salida comparten el mismo tipo de medio que el pin de entrada.

También se proporciona una versión de este filtro como ejemplo de SDK. Vea InfTee Filter Sample (Ejemplo [de filtro inftee).](inftee-filter-sample.md)



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de pin de entrada                    | Cualquier tipo de medio                                                                                                                                     |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de pin de salida                   | Cualquier tipo de medio. El tipo de salida siempre coincide con el tipo de entrada, para todas las patillas de salida                                                                 |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                           |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



