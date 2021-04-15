---
description: Filtro de divisor DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro de divisor DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ada4f18a107f8e1b07571f3907aed5ddf50f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536568"
---
# <a name="dv-splitter-filter"></a>Filtro de divisor DV

Este filtro divide una secuencia de vídeo digital (DV) intercalada en sus secuencias de audio y vídeo de componentes.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, format \_ DvInfo                                                                                         |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de anclaje de salida                   | **Vídeo**: \_ vídeo de MEDIATYPE, formato \_ DvInfo<br/> **Audio**: MEDIATYPE \_ audio, MEDIASUBTYPE \_ PCM, formato \_ WaveFormatEx<br/>             |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                  |
| Executable                               | qdv.dll                                                                                                                                            |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Los fotogramas DV contienen audio y vídeo en el mismo fotograma. El filtro de divisor DV extrae los datos de audio y los entrega como uno o dos flujos de audio de los pin de salida de audio. El fotograma DV original se entrega desde el PIN de salida de vídeo, como un fotograma de vídeo. El tipo de medio en el fotograma de vídeo se cambia de MEDIATYPE \_ intercalado a un vídeo de mediatype \_ , pero de lo contrario no se modifican los datos. El tipo de medio se cambia para indicar que los datos de audio del fotograma deben omitirse. El divisor DV no establece una hora de medio en sus ejemplos de salida; Si está escribiendo un filtro de nivel inferior que requiera las horas del medio, puede derivar las horas del recuento de fotogramas.

Solo un PIN de salida a la vez expone las interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .

El filtro de divisor DV puede aceptar cambios de formato dinámico en la secuencia de audio. Sin embargo, si el filtro de [AVI-MUX](avi-mux-filter.md) está en el nivel inferior, rechazará el cambio de formato. Si esto ocurre, el divisor DV deja de generar una secuencia de audio. Esta limitación solo afecta a la captura de archivos de tipo 2. En el caso de los archivos de tipo 1, la secuencia intercalada no se divide en primer lugar. En el caso de la versión preliminar, no hay ningún filtro de AVI en el nivel inferior.

Si el origen DV es una cámara activa, normalmente no hay ningún motivo por el que el formato de audio cambie. Sin embargo, el formato puede cambiar si se transmite desde una cinta VTR que contiene varios orígenes heterogéneos.

Cada fotograma DV contiene metadatos, además de los datos de audio y vídeo. Estos metadatos pueden cambiar de Frame a frame. Las aplicaciones pueden analizar los metadatos examinando los ejemplos de entrada o de salida de vídeo. Sin embargo, DirectShow no proporciona ninguna compatibilidad directa con el análisis de metadatos de DV. Consulte IEC 61834-4 para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




