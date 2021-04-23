---
description: Filtro de barra cruzada de vídeo análogo
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro de barra cruzada de vídeo análogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909603"
---
# <a name="analog-video-crossbar-filter"></a>Filtro de barra cruzada de vídeo análogo

El filtro Analog Video Crossbar representa una barra cruzada de vídeo en un dispositivo de captura de vídeo que admite Modelo de controlador de Windows (WDM).

Este filtro es un filtro contenedor para barras cruzadas en dispositivos de streaming WDM. El nombre descriptivo del filtro se toma del dispositivo. Cada pin de salida representa una ruta de acceso de hardware para vídeo de banda base análoga. Una de las clavijas de entrada procede de un afinador de TV (el [filtro de tuner de TV).](tv-tuner-filter.md) Otras patillas de entrada admiten secuencias de audio o vídeo. El filtro admite los subtipos de medios y los formatos que se admiten en las conexiones de nivel inferior.

No se puede crear directamente este filtro con CoCreateInstance. La [**interfaz ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) agrega automáticamente este filtro al gráfico según sea necesario.

Para obtener más información sobre los filtros de contenedor y los dispositivos de streaming de WDM, vea [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).



| Etiqueta | Value |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMCrossbar,**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfaces de pin de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfaces de pin de salida                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Filtrar CLSID                             | No aplicable                                                                                 |
| CLSID de la página de propiedades                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| Executable                               | ksxbar.ax                                                                                      |
| [Mérito](merit.md)                       | Dependiente del controlador.                                                                              |
| [Categoría de filtro](filter-categories.md) | BARRA \_ CRUZADA DE AM KSCATEGORY \_                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Trabajar con barras cruzadas](working-with-crossbars.md)
</dt> </dl>

 

 



