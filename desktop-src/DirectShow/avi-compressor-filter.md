---
description: Filtro de compresor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compresor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906317"
---
# <a name="avi-compressor-filter"></a>Filtro de compresor AVI

El filtro del compresor AVI permite que los códecs del administrador de compresión de vídeo (VCM) se unan a un gráfico de filtro. Cada códec aparece como una instancia independiente del filtro. No se puede crear directamente este filtro con CoCreateInstance. En su lugar, debe usar el enumerador de dispositivos del sistema. Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

El PIN de entrada del filtro se conecta a los filtros que generan datos de vídeo sin comprimir, como filtros de captura de vídeo o el [filtro de divisor de AVI](avi-splitter-filter.md). El PIN de salida del filtro se conecta normalmente a un filtro MUX, como el [filtro de AVI](avi-mux-filter.md).

Si el códec es compatible con un cuadro de diálogo de configuración de VFW de estilo antiguo o con el cuadro de diálogo acerca de, una aplicación puede mostrarlo mediante la interfaz [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> Los compresores MPEG nunca se implementan como códecs VCM, sino únicamente como filtros de DirectShow nativos.

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de anclaje de salida                   | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces de clavija de salida                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | No aplicable                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                                                                                                                  |
| Executable                               | qcap.dll                                                                                                                                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



