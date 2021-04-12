---
description: Filtro de divisor de secuencia MPEG-1
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: Filtro de divisor de secuencia MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152569"
---
# <a name="mpeg-1-stream-splitter-filter"></a>Filtro de divisor de secuencia MPEG-1

Este filtro divide un flujo del sistema MPEG-1 en sus secuencias de audio y vídeo de componentes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_Stream<br/> Subtipos<br/>
<ul>
<li>MEDIASUBTYPE_MPEG1System</li>
<li>MEDIASUBTYPE_MPEG1VideoCD</li>
<li>MEDIASUBTYPE_Audio</li>
<li>MEDIASUBTYPE_Video</li>
</ul>
Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de medios MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>Tipo principal: MEDIATYPE_Audio o MEDIATYPE_Video<br/> Subtipo: MEDIASUBTYPE_MPEG1Payload o MEDIASUBTYPE_MPEG1Packet<br/> Consulte <a href="mpeg-1-media-types.md"> <strong>tipos de medios MPEG-1</strong></a><br/></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_MPEG1Splitter</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Ninguna página de propiedades</td>
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



 

## <a name="remarks"></a>Observaciones

Este archivo admite el modo de extracción solo a través de [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ; no admite el modo de extracción.

Dado que el contenido de MPEG-1 no está indexado, la búsqueda puede ser muy aproximada. Normalmente, es conveniente para una secuencia de sistema MPEG-1 de velocidad de bits fija (que normalmente se genera por el hardware del CD de vídeo).

El filtro admite la interfaz [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) para recuperar los metadatos ID3.

No todos los ejemplos de MPEG tienen marcas de tiempo. La falta de una marca de tiempo en una muestra de MPEG no es un error. En el caso de los desarrolladores de filtros, esto significa que no debe devolver un código de error del método **Receive** del PIN de entrada si se produce un error en [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) . Si **Receive** devuelve cualquier valor distinto de S \_ OK, hará que el divisor deje de enviar ejemplos.

Si el archivo contiene una secuencia de vídeo, el divisor de secuencias MPEG-1 admite búsquedas por número de fotogramas. Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el [Administrador de gráficos de filtro](filter-graph-manager.md) con el **\_ \_ marco de formato de hora** de valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




