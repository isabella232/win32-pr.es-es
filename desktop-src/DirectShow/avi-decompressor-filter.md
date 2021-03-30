---
description: Filtro de descompresor de AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompresor de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806343"
---
# <a name="avi-decompressor-filter"></a>Filtro de descompresor de AVI

El filtro de descompresor de AVI permite que los códecs del administrador de compresión de vídeo (VCM) se unan a un gráfico de filtro. No es necesario que la aplicación agregue el filtro al gráfico de filtros. lo extrae automáticamente el administrador de gráficos de filtro cuando sea necesario.

Cuando el administrador de gráficos de filtro está compilando un gráfico para representar un archivo AVI, comprueba el FOURCC en el encabezado AVI del archivo para determinar si la secuencia de vídeo está comprimida. Si es así, el administrador de gráficos de filtros agrega el descompresor de AVI, que, a continuación, busca en el registro un descompresor instalado que pueda controlar el archivo.

> [!Note]  
> Los descompresores MPEG nunca se implementan como códecs VCM, sino únicamente como filtros de DirectShow nativos.

 

En su PIN ascendente, el descompresor AVI normalmente se conecta al [divisor de AVI](avi-splitter-filter.md). En el PIN de salida, normalmente se conecta al [representador de vídeo](video-renderer-filter.md) o al [filtro de AVI](avi-mux-filter.md).



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Tipos de medios de anclaje de entrada                    | Tipo principal: MEDIATYPE \_ VideoSubtype: debe corresponderse con el código FourCC para el tipo de compresión. Para obtener más información, consulte [códigos FourCC](fourcc-codes.md).<br/> Tipo de formato: formato de \_ Videoinfo<br/> |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ vídeo, MEDIASUBTYPE \_ null, formato de \_ videoinfo                                                                                                                                                            |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| Identificador CLSID                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                                                                                  |
| Executable                               | quartz.dll                                                                                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




