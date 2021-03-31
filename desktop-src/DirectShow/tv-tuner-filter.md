---
description: Filtro de sintonizador de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de sintonizador de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361310"
---
# <a name="tv-tuner-filter"></a>Filtro de sintonizador de TV

El filtro sintonizador de TV selecciona un canal de difusión o cable analógico que se va a ver. El flujo de salida único es una ruta de acceso de hardware para el vídeo analógico de banda. Esta salida debe conectarse al filtro de barras de vídeo analógicas. Los pines de entrada incluyen una entrada de cable y una entrada de antena.



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Tipos de medios de anclaje de entrada                    | No es aplicable.                                                                                                                                                                   |
| Interfaces de PIN de entrada                     | No es aplicable.                                                                                                                                                                   |
| Tipos de medios de anclaje de salida                   | Vídeo: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SubType \_ None audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de clavija de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| Identificador CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID de la página de propiedades                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| Executable                               | KSTVTune.ax                                                                                                                                                                       |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                               |
| [Categoría de filtro](filter-categories.md) | \_TVTUNER KSCATEGORY \_ AM                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



