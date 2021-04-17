---
description: Filtro contenedor ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro contenedor ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686413"
---
# <a name="acm-wrapper-filter"></a>Filtro contenedor ACM

El filtro contenedor ACM permite a los códecs del administrador de compresión de audio (ACM) unirse a un gráfico de filtros. Puede actuar como un filtro de descompresión o como un filtro de compresión.

Como filtro de descompresión, el contenedor ACM aparece en la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory) y tiene un mérito de mérito \_ normal. El tipo de medio de conexión en el PIN de entrada determina qué códec usa el filtro. Normalmente, la aplicación no necesita agregar el filtro al gráfico de filtro; lo extrae automáticamente el administrador de gráficos de filtro cuando sea necesario. La descompresión solo es para audio PCM.

Como filtro de compresión, el contenedor ACM aparece en la categoría "compresores de audio" (CLSID \_ AudioCompressorCategory) y tiene un mérito de mérito \_ \_ no \_ utilizado. Cada códec aparece como una instancia independiente. Para la compresión, no se puede crear directamente el filtro con CoCreateInstance. En su lugar, debe usar el enumerador de dispositivos del sistema. Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. es posible cualquier combinación de lo siguiente:<br/>
<ul>
<li>Muestras por segundo (kHz): 44,1, 22,05, 11,025 o 8,0.</li>
<li>Canales: estéreo o mono.</li>
<li>Bits por muestra: 8 o 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Ninguna página de propiedades.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_NORMAL o MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




