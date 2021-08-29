---
description: Filtro de descompresión AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompresión AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e7511c4243d2e36ff6270826201b4b6dc58246ed2a1d815f34ee14f9aff7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689485"
---
# <a name="avi-decompressor-filter"></a>Filtro de descompresión AVI

El filtro de descompresión AVI permite que los códecs del Administrador de compresión de vídeo (VCM) se unan a un gráfico de filtros. La aplicación no necesita agregar el filtro al gráfico de filtros; El Administrador de filtros Graph lo extrae automáticamente cuando sea necesario.

Cuando filter Graph Manager está creando un gráfico para representar un archivo AVI, comprueba fourcc en el encabezado AVI del archivo para determinar si la secuencia de vídeo está comprimida. Si es así, filter Graph Manager agrega el descompresión AVI, que busca en el Registro un descomprimidor instalado que pueda controlar el archivo.

> [!Note]  
> Los descomprimores MPEG nunca se implementan como códecs de VCM, sino solo como filtros DirectShow nativos.

 

En su ancla ascendente, el descomprimidor AVI normalmente se conecta al [divisor AVI.](avi-splitter-filter.md) En su ancla de salida, normalmente se conecta al representador [de](video-renderer-filter.md) vídeo o [al filtro Mux de AVI.](avi-mux-filter.md)



| Etiqueta | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Tipos de medios de pin de entrada                    | Tipo principal: MEDIATYPE \_ VideoSubtype: debe corresponder al código FOURCC para el tipo de compresión. Para obtener más información, vea [FOURCC Codes](fourcc-codes.md).<br/> Tipo de formato: FORMAT \_ VideoInfo<br/> |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo                                                                                                                                                            |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| Filtrar CLSID                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                                                                                  |
| Executable                               | quartz.dll                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                                                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




