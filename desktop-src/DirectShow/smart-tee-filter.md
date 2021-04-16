---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495478"
---
# <a name="smart-tee-filter"></a>Filtro Smart Tee

El filtro Smart Tee se usa en gráficos de captura de vídeo para dividir el flujo de vídeo en una secuencia de vista previa y en una secuencia de captura. Esto se hace sin copiar ningún dato adicional. Los pin de salida admiten los tipos de medios admitidos en la conexión de bajada.

El filtro Smart tee es útil cuando un filtro de captura de vídeo no proporciona PIN independientes para la captura y la vista previa. Los filtros Smart Tee ofrecen datos de vista previa solo si, de lo contrario, no perjudica el rendimiento de la captura. También quita las marcas de tiempo de la secuencia de vista previa. Cuando sea necesario, el generador de gráficos de captura insertará automáticamente el filtro de forma inteligente. Para obtener más información, consulte [combinar captura de vídeo y vista previa](combining-video-capture-and-preview.md).

En la ilustración siguiente se muestra un gráfico de captura típico que usa el filtro Smart tee.

![usar el filtro Smart Tee](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                           |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Tipos de medios de anclaje de salida                   | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                           |
| Interfaces de clavija de salida                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ SmartTee                                                                                                |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                              |
| Executable                               | qcap.dll                                                                                                       |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                            |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Observaciones

El PIN de captura es el PIN de salida 0 y el PIN de versión preliminar es el PIN de salida 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



