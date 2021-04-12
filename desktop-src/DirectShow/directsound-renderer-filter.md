---
description: Filtro de representador de DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de representador de DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151997"
---
# <a name="directsound-renderer-filter"></a>Filtro de representador de DirectSound

Este filtro representa el audio mediante DirectSound. Este filtro es actualmente el representador de audio predeterminado para el sonido de la forma de onda.

Además de sus capacidades básicas de representación de sonido, este filtro puede procesar llamadas API de DirectSound. Use los métodos [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para establecer y recuperar la ventana que controlará la reproducción del sonido. DirectSound audio renderer es el filtro de representación de audio predeterminado para DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_AudioSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_PCM</li>
<li>MEDIASUBTYPE_IEEE_FLOAT</li>
<li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li>
<li>MEDIASUBTYPE_RAW_SPORT</li>
<li>MEDIASUBTYPE_SPDIF_TAG_241h</li>
<li>MEDIASUBTYPE_DRM_Audio</li>
</ul>
Tipo de formato: FORMAT_WaveFormatEx<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
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
<td>CLSID_DSoundRender</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Este filtro actúa como un contenedor para un dispositivo de audio. Para enumerar los dispositivos de audio disponibles en el sistema del usuario, use la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoría de representador de audio (CLSID \_ AudioRendererCategory). Para cada dispositivo de audio, la categoría representador de audio contiene dos instancias de filtro. Uno de ellos corresponde al representador de DirectSound y el otro corresponde al filtro de [representador de audio (WaveOut)](audio-renderer--waveout--filter.md) . La instancia de DirectSound tiene el nombre descriptivo "DirectSound: *DeviceName*", donde *DeviceName* es el nombre del dispositivo. La instancia de WaveOut tiene el nombre descriptivo *DeviceName*.

La categoría representador de audio contiene dos instancias de filtro adicionales, denominadas "dispositivo DirectSound predeterminado" y "dispositivo WaveOut predeterminado". Estos se corresponden con el dispositivo de sonido predeterminado, elegido por el usuario a través del panel de control. En realidad, se asignan a uno de los pares descritos en el párrafo anterior. Por ejemplo, si el sistema tiene dos dispositivos de audio, el dispositivo A y el dispositivo B, la categoría de representador de audio contendrá lo siguiente:

-   Dispositivo A
-   DirectSound: dispositivo A
-   Dispositivo B
-   DirectSound: dispositivo B
-   Dispositivo DirectSound predeterminado
-   Dispositivo WaveOut predeterminado

Si el usuario seleccionó el dispositivo A como el dispositivo predeterminado, el "dispositivo de DirectSound predeterminado" es equivalente a "DirectSound: dispositivo A" y "dispositivo WaveOut predeterminado" es equivalente a "dispositivo A". Si el usuario selecciona el dispositivo B como dispositivo predeterminado, se cambiarán estas asignaciones.

El "dispositivo DirectSound predeterminado" tiene asignado el mérito de los MÉRITOs \_ preferidos. Los demás tienen MÉRITOs \_ que \_ no \_ usan. Por lo tanto, Intelligent Connect siempre elegirá el dispositivo DirectSound predeterminado.

El filtro de representador de DirectSound admite el sonido 3D a través de las interfaces **IDirectSound3DBuffer** y **IDirectSound3dListener** de DirectSound. También puede consultar el filtro para las versiones actuales de estas interfaces, **IDirectSound3DBuffer8** y **IDirectSound3dListener8**. Ejecute el gráfico antes de llamar a métodos en estas interfaces.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




