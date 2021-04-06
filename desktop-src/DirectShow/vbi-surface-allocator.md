---
description: Asignador de superficie de VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Asignador de superficie de VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815259"
---
# <a name="vbi-surface-allocator"></a>Asignador de superficie de VBI

El asignador de superficie de VBI controla la asignación de búferes VBI en gráficos de televisión analógica con escenarios de captura de puerto de vídeo de hardware. Con dispositivos como el descodificador de Bt829, el búfer de fotogramas puede contener varios búferes de captura de VBI a los que se tiene acceso a través de un mecanismo propio basado en hardware conocido como un puerto de vídeo. El filtro de asignador de superficie de VBI conecta el nivel inferior del filtro de captura y no tiene ningún PIN de salida. El filtro funciona en estrecha colaboración con el [mezclador de superposición](overlay-mixer-filter.md) (a través de DirectDraw) para realizar operaciones coordinadas en el puerto de vídeo de hardware, usando la misma memoria de búfer de fotogramas SVGA limitada.



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ VPVBI                                               |
| Interfaces de PIN de entrada                     | [**IKsPropertySet**](ikspropertyset.md)                                            |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ null, MEDIASUBTYPE \_ null. (Nunca se conecta a la clavija de salida). |
| Interfaces de clavija de salida                    | No es aplicable.                                                                     |
| Identificador CLSID                             | CLSID \_ VBISurfaces                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                   |
| Executable                               | vbisurf.ax                                                                          |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                       |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



