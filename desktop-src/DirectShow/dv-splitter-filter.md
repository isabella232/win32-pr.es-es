---
description: Filtro de divisor DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro de divisor DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ca8e856f1a49ff22ee05f7dc0ae341fad6aa91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246614"
---
# <a name="dv-splitter-filter"></a>Filtro de divisor DV

Este filtro divide una secuencia de vídeo digital intercalado (DV) en sus secuencias de audio y vídeo componentes.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                                         |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de pin de salida                   | **Vídeo:** VÍDEO \_ MEDIATYPE, FORMAT \_ DvInfo<br/> **Audio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx<br/>             |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                  |
| Executable                               | qdv.dll                                                                                                                                            |
| [Mérito](merit.md)                       | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Los marcos DV contienen audio y vídeo en el mismo fotograma. El filtro divisor DV extrae los datos de audio y los entrega como una o dos secuencias de audio, de las patillas de salida de audio. El fotograma DV original se entrega desde el pin de salida del vídeo, como un fotograma de vídeo. El tipo de medio en el fotograma de vídeo se cambia de MEDIATYPE intercalado a MEDIATYPE Video, pero de lo contrario los datos \_ \_ no se modifican. El tipo de medio se cambia para indicar que se deben omitir los datos de audio en el marco. El divisor DV no establece un tiempo de medios en sus ejemplos de salida; Si va a escribir un filtro de nivel inferior que requiere las horas de medios, puede derivar las horas del recuento de fotogramas.

Solo un pin de salida a la vez expone las interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) [**e IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)

El filtro divisor DV puede aceptar cambios de formato dinámico en la secuencia de audio. Sin embargo, si el [filtro Mux avi](avi-mux-filter.md) es descendente, rechazará el cambio de formato. Si esto sucede, el divisor DV deja de generar una secuencia de audio. Esta limitación solo afecta a la captura de archivos de tipo 2. En el caso de los archivos de tipo 1, la secuencia intercalada no se divide en primer lugar. Para la versión preliminar, no hay ningún filtro Mux AVI de bajada.

Si el origen dv es una cámara en directo, normalmente no hay ninguna razón para que cambie el formato de audio. Sin embargo, el formato puede cambiar si transmite desde una cinta VTR que contiene varios orígenes heterogéneos.

Cada fotograma DV contiene metadatos, además de los datos de audio y vídeo. Estos metadatos pueden cambiar de marco a marco. Las aplicaciones pueden analizar los metadatos examinando los ejemplos de entrada o los ejemplos de salida de vídeo. Sin embargo, DirectShow no proporciona compatibilidad directa para analizar metadatos DV. Consulte IEC 61834-4 para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




