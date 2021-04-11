---
description: Filtro de dibujo AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de dibujo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152056"
---
# <a name="avi-draw-filter"></a>Filtro de dibujo AVI

El filtro de extracción AVI se extrae automáticamente en un gráfico de reproducción en lugar del [descompresor AVI](avi-decompressor-filter.md) cuando el vídeo se envía a un monitor de televisión NTSC externo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_VideoSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_MJPG</li>
<li>MEDIASUBTYPE_TVMJ</li>
<li>MEDIASUBTYPE_WAKE</li>
<li>MEDIASUBTYPE_CFCC</li>
<li>MEDIASUBTYPE_IJPG</li>
<li>MEDIASUBTYPE_Plum</li>
<li>MEDIASUBTYPE_DVCS</li>
<li>MEDIASUBTYPE_DVSD</li>
<li>MEDIASUBTYPE_MDVF</li>
<li>Tipo de formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_NULL</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_AVIDraw</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Ninguna página de propiedades.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_NORMAL + 100</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Puesto que el filtro de dibujo AVI y el [filtro de captura VFW](vfw-capture-filter.md) se conectan al mismo hardware, no pueden estar en el mismo gráfico de filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




