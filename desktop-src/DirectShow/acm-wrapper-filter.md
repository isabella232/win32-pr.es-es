---
description: Filtro de contenedor de ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro de contenedor de ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162413"
---
# <a name="acm-wrapper-filter"></a>Filtro de contenedor de ACM

El filtro contenedor de ACM permite que los códecs del Administrador de compresión de audio (ACM) se unan a un gráfico de filtros. Puede actuar como filtro de descompresión o como filtro de compresión.

Como filtro de descompresión, el contenedor de ACM aparece en la categoría "filtros de DirectShow" (CLSID LegacyAmFilterCategory) y tiene un nivel \_ de VALOR NORMAL DE \_ MES. El tipo de medio de conexión en el pin de entrada determina qué códec usa el filtro. Normalmente, la aplicación no necesita agregar el filtro al gráfico de filtros; El Administrador de filtros lo extrae automáticamente cuando Graph necesario. La descompresión es solo para el audio PCM.

Como filtro de compresión, el contenedor de ACM aparece en la categoría "Audio Deserciones" (CLSID AudioCompressorCategory) y tiene una virtud \_ de NO USAR NO \_ \_ \_ USAR. Cada códec aparece como una instancia independiente. Para la compresión, no puede crear directamente el filtro con CoCreateInstance. En su lugar, debe usar el enumerador de dispositivos del sistema. Para obtener más información, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag | 
| Tipos de medios de pin de entrada | MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Cualquier combinación de lo siguiente es posible:<br /><ul><li>Muestras por segundo (kHz): 44.1, 22.05, 11.025 o 8.0.</li><li>Canales: estéreo o mono.</li><li>Bits por muestra: 8 o 16.</li></ul> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_ACMWrapper | 
| CLSID de la página de propiedades | No hay ninguna página de propiedades. | 
| Executable | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL o MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




