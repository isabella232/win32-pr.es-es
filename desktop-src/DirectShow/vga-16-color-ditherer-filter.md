---
description: Filtro de disexistente de color VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de disexistente de color VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082945"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtro de disexistente de color VGA 16

El filtro de separador de color VGA 16 convierte un tipo de color RGB en una pantalla de color de 4 bits para que las secuencias de vídeo AVI y MPEG se puedan mostrar en monitores de 16 colores más antiguos. Este filtro se inserta en el gráfico entre un filtro de descompresor y un filtro de representador de vídeo.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de anclaje de salida                   | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | \_Interpolación de CLSID                                                                                                                                      |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                  |
| Executable                               | quartz.dll                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                                                                    |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



