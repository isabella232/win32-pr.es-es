---
description: Filtro del analizador DE MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro del analizador DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072153"
---
# <a name="midi-parser-filter"></a>Filtro del analizador DE MIDI

El filtro Analizador DE MIDI lee los datos DE MIDI que se encuentran en . MID y . Archivos MID. El filtro acepta una secuencia de los filtros [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) o URL File Source (Origen de archivo [URL)](file-source--url--filter.md) y genera ejemplos de MIDI en [**el representador de MIDI**](midi-renderer-filter.md) para su reproducción.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Midi                                                                    |
| Interfaces de pin de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL                                                                      |
| Interfaces de pin de salida                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtrar CLSID                             | CLSID \_ MIDIParser                                                                                        |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                         |
| Executable                               | quartz.dll                                                                                               |
| [Mérito](merit.md)                       | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                          |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Observaciones

Para obtener más información, vea [**Representador de MIDI.**](midi-renderer-filter.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



