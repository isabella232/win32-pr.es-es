---
description: Filtro descodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro descodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e72e575baf6761a34078ee4413b6dd095871a646d9539d08c9357ffd8af5efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051025"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtro descodificador de vídeo MPEG-1

Descodifica vídeo MPEG-1.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de entrada</td>
<td>MEDIATYPE_Video, FORMAT_MPEGVideo<br/> Los subtipos siguientes son válidos:<br/>
<ul>
<li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li>
<li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pin de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de salida</td>
<td>Tipo principal: <strong>MEDIATYPE_Video</strong>,<br/> Tipo de formato: <strong>FORMAT_VideoInfo</strong> o <strong>FORMAT_VideoInfo2</strong><br/> Subtipos:<br/>
<ul>
<li><strong>MEDIASUBTYPE_RGB24</strong></li>
<li><strong>MEDIASUBTYPE_RGB32</strong></li>
<li><strong>MEDIASUBTYPE_RGB8</strong></li>
<li><strong>MEDIASUBTYPE_RGB555</strong></li>
<li><strong>MEDIASUBTYPE_RGB565</strong></li>
<li><strong>MEDIASUBTYPE_UYVY</strong></li>
<li><strong>MEDIASUBTYPE_Y41P</strong></li>
<li><strong>MEDIASUBTYPE_YUY2</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pin de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td><strong>CLSID_CMpegVideoCodec</strong></td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td><strong>CLSID_MpegVideoDecodePropertyPage</strong></td>
</tr>
<tr class="even">
<td>Executable</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérito</a></td>
<td>0x40000001</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Este filtro se puede descodificar en una superficie directdraw. El filtro usa MMX si la máquina admite MMX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




