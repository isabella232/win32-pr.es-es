---
description: Filtro de filtro de filtro de AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de filtro de filtro de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159277"
---
# <a name="avi-compressor-filter"></a>Filtro de filtro de filtro de AVI

El filtro Desenlazador AVI permite que los códecs del Administrador de compresión de vídeo (VCM) se unan a un gráfico de filtros. Cada códec aparece como una instancia independiente del filtro. No se puede crear directamente este filtro con CoCreateInstance. En su lugar, debe usar el enumerador de dispositivos del sistema. Para obtener más información, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

El pin de entrada del filtro se conecta a los filtros que emiten datos de vídeo sin comprimir, como los filtros de captura de vídeo o el filtro [divisor AVI](avi-splitter-filter.md). El pin de salida del filtro normalmente se conecta a un filtro de MUX, como el filtro [Mux de AVI.](avi-mux-filter.md)

Si el códec admite un cuadro de diálogo de configuración de VFW de estilo antiguo o un cuadro de diálogo Acerca de, una aplicación puede mostrarlo mediante la [**interfaz IAMVfwCompressDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)

> [!Note]  
> Los mpeg mpeg nunca se implementan como códecs VCM, sino solo como filtros DirectShow nativos.

 



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMVfwCompressDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipos de medios de pin de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de pin de salida                   | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | No aplicable                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                                                                                                                  |
| Executable                               | qcap.dll                                                                                                                                                                                                                                           |
| [Mérito](merit.md)                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



