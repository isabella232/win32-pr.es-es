---
description: Asignador de superficie de VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Asignador de superficie de VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909013"
---
# <a name="vbi-surface-allocator"></a>Asignador de superficie de VBI

El asignador de superficie de VBI controla la asignación de búferes de VBI en gráficos de televisión análogos con escenarios de captura de puertos de vídeo de hardware. Con dispositivos como el descodificador Bt829, el búfer de fotogramas puede contener varios búferes de captura de VBI a los que se accede a través de un mecanismo propietario basado en hardware conocido genéricamente como puerto de vídeo. El filtro Asignador de superficie de VBI se conecta de bajada desde el filtro de captura y no tiene ningún pin de salida. El filtro funciona estrechamente con el mezclador de superposición [(a](overlay-mixer-filter.md) través de DirectDraw) para realizar operaciones coordinadas en el puerto de vídeo de hardware, utilizando la misma memoria de búfer de fotograma SVGA limitada.



| Etiqueta | Value |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipos de medios de pin de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfaces de pin de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL. (Nunca se ha conectado nada al pin de salida). |
| Interfaces de pin de salida                    | No es aplicable.                                                                     |
| Filtrar CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                   |
| Executable                               | vbisurf.ax                                                                          |
| [Mérito](merit.md)                       | PROCEDIMIENTO \_ NORMAL                                                                       |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



