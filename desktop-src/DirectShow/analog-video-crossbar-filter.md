---
description: Filtro de barras de vídeos analógicos
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro de barras de vídeos analógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997813"
---
# <a name="analog-video-crossbar-filter"></a>Filtro de barras de vídeos analógicos

El filtro de barras de vídeo analógicas representa una cruz de vídeo en un dispositivo de captura de vídeo que admite el Modelo de controlador de Windows (WDM).

Este filtro es un filtro de contenedor para las barras cruzadas en los dispositivos de streaming WDM. El nombre descriptivo del filtro se toma del dispositivo. Cada pin de salida representa una ruta de acceso de hardware para el vídeo analógico de banda. Uno de los pines de entrada procede de un sintonizador de TV (el [filtro de sintonizador de TV](tv-tuner-filter.md)). Otros PIN de entrada admiten secuencias de audio o vídeo. El filtro admite los subtipos de medios y los formatos que se admiten en las conexiones de nivel inferior.

No se puede crear directamente este filtro con CoCreateInstance. La interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) agrega automáticamente este filtro al gráfico según sea necesario.

Para obtener más información sobre los filtros de contenedor y los dispositivos de streaming WDM, consulte [Cómo participan los dispositivos de hardware en el gráfico de filtro](how-hardware-devices-participate-in-the-filter-graph.md).



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ AnalogAudio, mediatype \_ AnalogVideo                                                 |
| Interfaces de PIN de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ AnalogAudio, mediatype \_ AnalogVideo                                                 |
| Interfaces de clavija de salida                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Identificador CLSID                             | No aplicable                                                                                 |
| CLSID de la página de propiedades                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| Executable                               | ksxbar.ax                                                                                      |
| [Fundament](merit.md)                       | Dependiente del controlador.                                                                              |
| [Categoría de filtro](filter-categories.md) | KSCATEGORY de AM de la \_ \_ Cruz                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Trabajar con barras cruzadas](working-with-crossbars.md)
</dt> </dl>

 

 



