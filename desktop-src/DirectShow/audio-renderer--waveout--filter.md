---
description: Filtro de representador de audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de representador de audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686406"
---
# <a name="audio-renderer-waveout-filter"></a>Filtro de representador de audio (WaveOut)

Este filtro usa la API de waveOut \* para representar el audio de una onda. Sin embargo, el [filtro de representador de DirectSound](directsound-renderer-filter.md) proporciona la misma funcionalidad mediante DirectSound. De forma predeterminada, Filter Graph Manager usa el representador de DirectSound en lugar de este filtro. La mezcla de audio está deshabilitada en el representador de audio waveOut, por lo que si necesita mezclar varias transmisiones de audio durante la reproducción, use el representador de DirectSound.

Este filtro no comprueba el subtipo de la secuencia de audio. La estructura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) pasada en el formato contiene la información necesaria para la conexión.

Este filtro admite un intervalo de frecuencias de muestreo que depende del controlador de audio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li>IPersistPropertyBag</li>
<li>IPersistStream</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td><strong>MEDIATYPE_Audio</strong></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td><strong>CLSID_AudioRender</strong></td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></td>
</tr>
<tr class="even">
<td>Executable</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 
