---
description: Filtro de tuner de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de tuner de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909033"
---
# <a name="tv-tuner-filter"></a>Filtro de tuner de TV

El filtro de tv tuner selecciona un canal de difusión o cable análogo que se va a ver. El flujo de salida único es una ruta de acceso de hardware para vídeo de banda base análoga. Esta salida debe conectarse al filtro de barra cruzada de vídeo análogo. Las clavijas de entrada incluyen una entrada para el cable y una entrada de la antena.



| Etiqueta | Value |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md) |
| Tipos de medios de pin de entrada                    | No es aplicable.                                                                                                                                                                   |
| Interfaces de pin de entrada                     | No es aplicable.                                                                                                                                                                   |
| Tipos de medios de pin de salida                   | Vídeo: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                      |
| Interfaces de pin de salida                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| Filtrar CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID de la página de propiedades                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| Executable                               | KSTVTune.ax                                                                                                                                                                       |
| [Mérito](merit.md)                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                                                                                               |
| [Categoría de filtro](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



