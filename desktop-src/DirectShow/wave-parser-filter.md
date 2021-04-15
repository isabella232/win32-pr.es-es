---
description: Filtro de WAVE parser
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro de WAVE parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669955"
---
# <a name="wave-parser-filter"></a>Filtro de WAVE parser

El filtro del analizador de onda analiza los datos de audio con formato WAV de los archivos. wav,. au o. AIF. El filtro de nivel superior debe ser el filtro de [origen de archivo asincrónico](file-source--async--filter.md) , el filtro de [origen de archivo URL](file-source--url--filter.md) o un filtro de origen asincrónico de terceros compatible que contenga datos de audio WAV. El flujo de salida es datos de audio, que puede conectarse directamente a un filtro de representación de audio o a un filtro de transformación de audio que intervenga.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_StreamThe siguientes subtipos son válidos:<br/>
<ul>
<li>MEDIASUBTYPE_AIFF</li>
<li>MEDIASUBTYPE_AU</li>
<li>MEDIASUBTYPE_WAVE</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>Tipo principal: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM u otro tipo de compresión. (Consulte <a href="audio-subtypes.md"><strong>subtipos de audio</strong></a>).<br/> Tipo de formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>{D51BD5A1-7548-11cf-A520-0080C77EF58A}</td>
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
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Este filtro admite los siguientes tipos de archivo:

-   ONDA (. wav)
-   AIFF y AIFF-C (. AIF)
-   AU (. au)

Sin embargo, tiene las siguientes limitaciones en el formato de audio:

-   El audio debe ser PCM lineal de 8 o 16 bits.
-   En el caso de los archivos AIFF-C, el audio se debe descomprimir, en el orden de bytes big-endian (tipo de compresión ' NONE ').

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




