---
description: Filtro de teo inteligente
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro de teo inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063171"
---
# <a name="smart-tee-filter"></a>Filtro de teo inteligente

El filtro Smart Tee se usa en gráficos de captura de vídeo para dividir la secuencia de vídeo en una secuencia de vista previa y una secuencia de captura. Esto se hace sin copiar datos adicionales. Las clavijas de salida admiten cualquier tipo de medio que se admita en la conexión de bajada.

El filtro Smart Tee es útil cuando un filtro de captura de vídeo no proporciona pasadores independientes para la captura y vista previa. El filtro Smart Tee ofrece datos de vista previa solo si esto no afecta al rendimiento de la captura. También quita las marcas de tiempo de la secuencia de vista previa. El generador de gráficos de captura inserta automáticamente el filtro Smart Tee cuando es necesario. Para obtener más información, vea [Combinar captura de vídeo y versión preliminar.](combining-video-capture-and-preview.md)

En la ilustración siguiente se muestra un gráfico de captura típico que usa el filtro Smart Tee.

![usar el filtro de tee inteligente](images/smarttee.png)



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Tipos de medios de pin de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                           |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Tipos de medios de pin de salida                   | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                           |
| Interfaces de pin de salida                    | [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ SmartTee                                                                                                |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                              |
| Executable                               | qcap.dll                                                                                                       |
| [Mérito](merit.md)                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                            |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Observaciones

El pin de captura es el pin de salida 0 y el pin de vista previa es el pin de salida 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



