---
description: Filtro de representador de audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de representador de audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66d92357b41b6fa23018acf6d44b966eb77fab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162213"
---
# <a name="audio-renderer-waveout-filter"></a>Filtro de representador de audio (WaveOut)

Este filtro usa waveOut \* API para representar el audio de forma de onda. Sin embargo, [el filtro de representador de Direct Sound](directsound-renderer-filter.md) proporciona la misma funcionalidad mediante Direct Sound. De forma predeterminada, el Administrador de Graph usa el representador de Direct Sound en lugar de este filtro. La mezcla de audio está deshabilitada en el representador de audio waveOut, por lo que si necesita mezclar varias secuencias de audio durante la reproducción, use el representador de Direct Sound.

Este filtro no comprueba el subtipo de la secuencia de audio. La [**estructura WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEATEX**](/previous-versions/dd757713(v=vs.85)) pasada en el formato contiene la información necesaria para la conexión.

Este filtro admite una variedad de frecuencias de muestreo que dependen del controlador de audio.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockLockLock</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirect Sound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>Ipersiststream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Tipos de medios de pin de entrada | <strong>MEDIATYPE_Audio</strong> | 
| Interfaces de pin de entrada | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | 
| Tipos de medios de pin de salida | No aplicable. | 
| Interfaces de pin de salida | No aplicable. | 
| Filtrar CLSID | <strong>CLSID_AudioRender</strong> | 
| CLSID de la página de propiedades | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | 
| Executable | quartz.dll | 
| <a href="merit.md">Mérito</a> | <strong>MERIT_DO_NOT_USE</strong> | 
| <a href="filter-categories.md">Categoría de filtro</a> | <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 
