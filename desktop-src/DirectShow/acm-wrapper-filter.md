---
description: Filtro de contenedor de ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro de contenedor de ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aaa56d955fe9cf1966e17c657fbf741b4bb8694a7f18b501b148b0383ea19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664084"
---
# <a name="acm-wrapper-filter"></a>Filtro de contenedor de ACM

El filtro contenedor de ACM permite que los códecs del Administrador de compresión de audio (ACM) se unan a un gráfico de filtros. Puede actuar como filtro de descompresión o como filtro de compresión.

Como filtro de descompresión, el contenedor de ACM aparece en la categoría "filtros de DirectShow" (CLSID LegacyAmFilterCategory) y tiene el nivel \_ DE NORMAL DE \_ ACM. El tipo de medio de conexión en el pin de entrada determina qué códec usa el filtro. Normalmente, la aplicación no necesita agregar el filtro al gráfico de filtros; El Administrador de filtros Graph lo extrae automáticamente cuando sea necesario. La descompresión es solo para el audio PCM.

Como filtro de compresión, el contenedor de ACM aparece en la categoría "Audio Deserciones" (CLSID \_ AudioCompressorCategory) y tiene el honor DE NO USAR. \_ \_ \_ Cada códec aparece como una instancia independiente. Para la compresión, no puede crear directamente el filtro con CoCreateInstance. En su lugar, debe usar el enumerador de dispositivos del sistema. Para obtener más información, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de entrada</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfaces de pin de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de salida</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Cualquier combinación de lo siguiente es posible:<br/>
<ul>
<li>Muestras por segundo (kHz): 44,1, 22,05, 11,025 o 8,0.</li>
<li>Canales: estéreo o mono.</li>
<li>Bits por ejemplo: 8 o 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pin de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>No hay ninguna página de propiedades.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérito</a></td>
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

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




