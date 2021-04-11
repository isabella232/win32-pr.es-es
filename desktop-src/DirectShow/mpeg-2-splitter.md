---
description: Separador MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Separador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274765"
---
# <a name="mpeg-2-splitter"></a>Separador MPEG-2

A partir de Microsoft® Windows® XP, el filtro de divisores MPEG-2 está en desuso. En su lugar, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .

En plataformas anteriores, use el divisor MPEG-2 para secuencias de programas MPEG-2 entregadas en modo de extracción que contienen al menos uno de los siguientes tipos de secuencias: vídeo MPEG-2; Audio MPEG-2; La codificación de audio AC3 tal y como se define para el vídeo de DVD; o PCM audio codificado tal y como se define para el vídeo en DVD. Este filtro analiza los flujos, crea un PIN de salida para cada flujo y envía los paquetes de audio o vídeo comprimidos MPEG a un filtro de descodificador MPEG-2.

En el caso de los flujos de programa y transporte entregados en modo de inserciones, use el [demultiplexador MPEG-2](mpeg-2-demultiplexer.md)en todas las plataformas.

> [!Note]  
> El separador MPEG-2 no admite búsquedas con precisión de fotogramas.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td><ul>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li>
<li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>Depende del tipo de flujo. Consulte <a href="mpeg-2-splitter-media-types.md">tipos de medios de divisor MPEG-2</a></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_MMSPLITTER</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>mpg2splt.ax</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_NORMAL + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_AudioInputDeviceCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Usar el divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



