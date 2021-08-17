---
description: Filtro del navegador de DVD
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro del navegador de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a395001daeac5f90be85bea972d1d4f118198ee4343960cb4eed0d958e1677aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016013"
---
# <a name="dvd-navigator-filter"></a>Filtro del navegador de DVD

El filtro DVD Navigator es el filtro de origen de un DVD-Video de filtro de reproducción. Abre todos los archivos necesarios en un volumen DVD-Video, navega por los archivos .vob de DVD-Video lineales y analiza la secuencia de programa MPEG-2 resultante, dividiendo la secuencia en tres pines de salida (vídeo, audio, subpicture).

El filtro DVD Navigator también implementa las interfaces [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) que permiten que una aplicación de reproducción de DVD controle DVD-Video reproducción.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter,</strong></a> <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de entrada</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</td>
</tr>
<tr class="odd">
<td>Interfaces de pin de entrada</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de salida</td>
<td>Tipos base:<br/>
<ul>
<li>Vídeo: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li>Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li>Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Tipos extendidos:<br/> Vídeo:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li>
</ul>
Audio:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li>
</ul>
Subimagen:<br/>
<ul>
<li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
<li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li>
</ul>
Para habilitar los tipos extendidos, llame <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>a IDvdControl2::SetOption</strong></a> y establezca <br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pin de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td>CLSID_DVDNavigator</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>No hay ninguna página de propiedades.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 




