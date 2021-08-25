---
description: Filtro de representador de Direct Sound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de representador de Direct Sound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b601c0e85169857cd628b3b3e55b5c00af8ea11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481581"
---
# <a name="directsound-renderer-filter"></a>Filtro de representador de Direct Sound

Este filtro representa el audio mediante Direct Sound. Este filtro es actualmente el representador de audio predeterminado para el sonido de forma de onda.

Además de sus funcionalidades básicas de representación de sonido, este filtro puede procesar llamadas a Direct Sound API. Use los [**métodos IAMDirect Sound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para establecer y recuperar la ventana que controlará la reproducción de sonido. El representador de audio Direct Sound es el filtro de representación de audio predeterminado para DirectShow.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirect Sound,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio,</strong></a> <strong>IDirect Sound3DBuffer,</strong> <strong>IDirect Sound3dListener,</strong> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_AudioSubtypes:<br /><ul><li>MEDIASUBTYPE_PCM</li><li>MEDIASUBTYPE_IEEE_FLOAT</li><li>MEDIASUBTYPE_DOLBY_AC3_SPDIF</li><li>MEDIASUBTYPE_RAW_SPORT</li><li>MEDIASUBTYPE_SPDIF_TAG_241h</li><li>MEDIASUBTYPE_DRM_Audio</li></ul>Tipo de formato: FORMAT_WaveFormatEx<br /> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | No aplicable. | | Interfaces de pin de salida | No aplicable. | | Filtrar clsid | CLSID_DSoundRender | | ClSID de página de propiedades | CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties | | Archivos ejecutables | quartz.dll | | <a href="merit.md">Ventajas |</a> MERIT_PREFERRED | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_AudioRendererCategory | 




 

## <a name="remarks"></a>Comentarios

Este filtro actúa como contenedor para un dispositivo de audio. Para enumerar los dispositivos de audio disponibles en el sistema del usuario, use la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoría de representador de audio (CLSID \_ AudioRendererCategory). Para cada dispositivo de audio, la categoría representador de audio contiene dos instancias de filtro. Una de ellas corresponde al representador de Direct Sound y la otra corresponde al filtro Representador de [audio (WaveOut).](audio-renderer--waveout--filter.md) La instancia de Direct Sound tiene el nombre descriptivo "Direct Sound: *DeviceName*," donde *DeviceName* es el nombre del dispositivo. La instancia de WaveOut tiene el nombre descriptivo *DeviceName*.

La categoría representador de audio contiene dos instancias de filtro adicionales, denominadas "Default Direct Sound Device" y "Default WaveOut Device". Se corresponden con el dispositivo de sonido predeterminado, según lo elegido por el usuario a través del Panel de control. En realidad, son asignaciones a uno de los pares descritos en el párrafo anterior. Por ejemplo, si el sistema tiene dos dispositivos de audio, Dispositivo A y Dispositivo B, la categoría representador de audio contendrá lo siguiente:

-   Dispositivo A
-   Direct Sound: Dispositivo A
-   Dispositivo B
-   Direct Sound: Dispositivo B
-   Dispositivo Direct Sound predeterminado
-   Dispositivo WaveOut predeterminado

Si el usuario seleccionó Dispositivo A como dispositivo predeterminado, "Dispositivo Direct Sound predeterminado" equivale a "Direct Sound: Device A" y "Default WaveOut Device" es equivalente a "Device A". Si el usuario selecciona Dispositivo B como dispositivo predeterminado, estas asignaciones cambiarán.

A "Dispositivo Direct Sound predeterminado" se le asigna un valor de PREFERRED \_ PREFERRED. Los demás tienen la virtud DE NO \_ \_ \_ USAR. Por lo tanto, intelligent Conectar elegirá siempre el dispositivo Direct Sound predeterminado.

El filtro Representador de Direct Sound admite el sonido 3D a través de las interfaces **IDirectSound3DBuffer** e **IDirect Sound3dListener** de Direct Sound. También puede consultar el filtro de las versiones actuales de estas interfaces, **IDirect Sound3DBuffer8** **e IDirect Sound3dListener8**. Ejecute el gráfico antes de llamar a métodos en estas interfaces.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




