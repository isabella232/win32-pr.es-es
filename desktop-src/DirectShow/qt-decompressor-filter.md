---
description: Filtro de descompresor de QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro de descompresor de QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494860"
---
# <a name="qt-decompressor-filter"></a>Filtro de descompresor de QT

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

El filtro de descompresor de QT descomprime el vídeo de Apple® QuickTime® 2,0. Este formato se usa normalmente en archivos QuickTime más antiguos.



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
<td>MEDIATYPE_Video, FORMAT_VideoInfo<br/> Los siguientes subtipos son válidos:<br/>
<ul>
<li>MEDIASUBTYPE_QTRpza</li>
<li>MEDIASUBTYPE_QTSmc</li>
<li>MEDIASUBTYPE_QTRle</li>
<li>MEDIASUBTYPE_QTJpeg</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_QTDec</td>
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
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




