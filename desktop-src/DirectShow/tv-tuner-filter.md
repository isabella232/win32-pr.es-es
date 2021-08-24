---
description: Filtro de tuner de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de tuner de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101dfcce4877570a2072d9e4c116466223e56889fb5e66de3e6ef0ec24afad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015523"
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

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



