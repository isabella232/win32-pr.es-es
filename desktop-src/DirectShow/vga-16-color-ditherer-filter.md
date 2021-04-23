---
description: Filtro de ditherer de color VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de ditherer de color VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908683"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtro de ditherer de color VGA 16

El filtro Vga 16 Color Ditherer convierte un tipo de color RGB en una pantalla de color de 4 bits para que se puedan mostrar secuencias de vídeo AVI y MPEG en monitores de 16 colores anteriores. Este filtro se inserta en el gráfico entre un filtro de descompresión y un filtro de representador de vídeo.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de pin de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de pin de salida                   | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ Dither                                                                                                                                      |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                  |
| Executable                               | quartz.dll                                                                                                                                         |
| [Mérito](merit.md)                       | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                                                                    |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



