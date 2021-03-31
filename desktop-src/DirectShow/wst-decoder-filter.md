---
description: Filtro de descodificador de elemento WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de descodificador de elemento WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908357"
---
# <a name="wst-decoder-filter"></a>Filtro de descodificador de elemento WST

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Windows XP y Windows Server 2003.

> [!Note]  
> A partir de Windows Vista, DirectShow no proporciona un filtro para descodificar el teletexto del estándar mundial (elemento WST).

 

El descodificador de elemento WST es un filtro de modo kernel que acepta datos de teletexto del mundo descodificados del [códec elemento WST](wst-codec-filter.md) y entrega los mapas de bits al pin 2 del [mezclador de superposición](overlay-mixer-filter.md) con las fuentes proporcionadas por Microsoft. En este momento solo se admiten idiomas de Europa occidental; no se proporcionan fuentes Unicode actualmente.

Este filtro se puede Agregar al gráfico automáticamente mediante una llamada a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), mediante el PIN de salida del códec elemento WST.



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| Interfaces de filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ teletexto                        |
| Interfaces de PIN de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipos de medios de anclaje de salida                   | Vídeo de MEDIATYPE \_                                              |
| Interfaces de clavija de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Identificador CLSID                             | CLSID \_ WSTDecoder                                             |
| CLSID de la página de propiedades                      | CLSID \_ WstDecoderPropertyPage                                 |
| Executable                               | Wstdecod.DLL                                                  |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                 |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Ver teletexto estándar del mundo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



