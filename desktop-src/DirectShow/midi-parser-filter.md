---
description: Filtro de analizador MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro de analizador MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997657"
---
# <a name="midi-parser-filter"></a>Filtro de analizador MIDI

El filtro del analizador MIDI Lee los datos MIDI que se encuentran en. MID y. Archivos RMI. El filtro acepta un flujo desde el [origen de archivo asincrónico](file-source--async--filter.md) o los filtros de origen de archivo de la [dirección URL](file-source--url--filter.md) , y envía muestras MIDI al [**representador MIDI**](midi-renderer-filter.md) para su reproducción.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de medios de anclaje de entrada                    | \_Secuencia de MEDIATYPE, MEDIASUBTYPE \_ MIDI                                                                    |
| Interfaces de PIN de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de clavija de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Identificador CLSID                             | CLSID \_ MIDIParser                                                                                        |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                         |
| Executable                               | quartz.dll                                                                                               |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                          |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Observaciones

Para obtener más información, vea [**representador MIDI**](midi-renderer-filter.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



