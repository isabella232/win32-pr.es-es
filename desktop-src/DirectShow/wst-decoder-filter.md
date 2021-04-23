---
description: Filtro de descodificador de WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de descodificador de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908483"
---
# <a name="wst-decoder-filter"></a>Filtro de descodificador de WST

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Windows XP y Windows Server 2003.

> [!Note]  
> A partir de Windows Vista, DirectShow no proporciona un filtro para descodificar El teletexto estándar mundial (WST).

 

El descodificador de WST es un filtro en modo kernel que acepta datos descodificados de Teletext world [](overlay-mixer-filter.md) standard del códec [WST](wst-codec-filter.md) y entrega los mapas de bits al pin 2 en el mezclador de superposición mediante fuentes proporcionadas por Microsoft. En este momento solo se admiten los idiomas europeos occidental; actualmente no se proporcionan fuentes Unicode.

Este filtro se puede agregar automáticamente al gráfico llamando a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mediante el pin de salida del códec WST.



| Etiqueta | Value |
|------------------------------------------|---------------------------------------------------------------|
| Interfaces de filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Interfaces de pin de entrada                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipos de medios de pin de salida                   | VÍDEO \_ MEDIATYPE                                              |
| Interfaces de pin de salida                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Filtrar CLSID                             | CLSID \_ WSTDecoder                                             |
| CLSID de la página de propiedades                      | CLSID \_ WstDecoderPropertyPage                                 |
| Executable                               | Wstdecod.DLL                                                  |
| [Mérito](merit.md)                       | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                 |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Visualización del texto teletexto estándar del mundo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



