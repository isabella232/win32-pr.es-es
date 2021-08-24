---
description: Filtro de representador de DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de representador de DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e754c81ba9ac6d22141735ac1488218461d9ea63ef81f7bb947cb3e72fd81d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966325"
---
# <a name="directsound-renderer-filter"></a>Filtro de representador de DirectSound

Este filtro representa el audio mediante DirectSound. Este filtro es actualmente el representador de audio predeterminado para el sonido de forma de onda.

Además de sus funcionalidades básicas de representación de sonido, este filtro puede procesar llamadas a DirectSound API. Use los [**métodos IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para establecer y recuperar la ventana que controlará la reproducción de sonido. DirectSound Audio Renderer es el filtro de representación de audio predeterminado para DirectShow.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockBasice,</strong></a> <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer,</strong> <strong>IDirectSound3dListener,</strong> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de entrada</td>
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
<td>Interfaces de pin de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de pin de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="odd">
<td>Interfaces de pin de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
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
<td><a href="merit.md">Mérito</a></td>
<td>MERIT_PREFERRED</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_AudioRendererCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Este filtro actúa como un contenedor para un dispositivo de audio. Para enumerar los dispositivos de audio disponibles en el sistema del usuario, use la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoría de representador de audio (CLSID \_ AudioRendererCategory). Para cada dispositivo de audio, la categoría representador de audio contiene dos instancias de filtro. Una de ellas corresponde al representador de DirectSound y la otra corresponde al [filtro Representador de audio (WaveOut).](audio-renderer--waveout--filter.md) La instancia de DirectSound tiene el nombre descriptivo "DirectSound: *DeviceName",* donde *DeviceName* es el nombre del dispositivo. La instancia de WaveOut tiene el nombre descriptivo *DeviceName.*

La categoría de representador de audio contiene dos instancias de filtro adicionales, denominadas "Default Direct Sound Device" y "Default WaveOut Device". Se corresponden con el dispositivo de sonido predeterminado, según lo elegido por el usuario a través del Panel de control. En realidad, son asignaciones a uno de los pares descritos en el párrafo anterior. Por ejemplo, si el sistema tiene dos dispositivos de audio, Dispositivo A y Dispositivo B, la categoría representador de audio contendrá lo siguiente:

-   Dispositivo A
-   DirectSound: Dispositivo A
-   Dispositivo B
-   DirectSound: Dispositivo B
-   Dispositivo Direct Sound predeterminado
-   Dispositivo waveout predeterminado

Si el usuario seleccionó Dispositivo A como dispositivo predeterminado, "Dispositivo Direct Sound predeterminado" equivale a "DirectSound: Dispositivo A" y "Dispositivo WaveOut predeterminado" equivale a "Dispositivo A". Si el usuario selecciona Dispositivo B como dispositivo predeterminado, estas asignaciones cambiarán.

A "Dispositivo DirectSound predeterminado" se le asigna un abate de PREFERRED \_ PREFERRED. Los demás tienen el favor DE NO \_ \_ \_ USAR. Por lo tanto, Intelligent Conectar elegirá siempre el dispositivo DirectSound predeterminado.

El filtro Representador de DirectSound admite sonido 3D a través de las interfaces **IDirectSound3DBuffer** e **IDirectSound3dListener** de Direct Sound. También puede consultar el filtro para las versiones actuales de estas interfaces, **IDirectSound3DBuffer8** e **IDirectSound3dListener8**. Ejecute el gráfico antes de llamar a métodos en estas interfaces.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




