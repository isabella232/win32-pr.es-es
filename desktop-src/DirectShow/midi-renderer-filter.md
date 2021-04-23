---
description: El filtro representador de MIDI representa los datos DE MIDI del filtro del analizador de MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de representador DE MIDI (Windows.devices.midi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909413"
---
# <a name="midi-renderer-filter"></a>Filtro de representador de MIDI

El filtro representador de MIDI representa los datos DE MIDI del filtro [del analizador de MIDI.](midi-parser-filter.md)



| Etiqueta | Value |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMClockVicee,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                                                                                                                  |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Tipos de medios de pin de salida                   | No aplicable                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pin de salida                    | No aplicable                                                                                                                                                                                                                                                                                                                                                                       |
| Filtrar CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                                                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Mérito](merit.md)                       | MERIT \_ PREFERRED                                                                                                                                                                                                                                                                                                                                                                     |
| [Categoría de filtro](filter-categories.md) | CLSID \_ MidiRendererCategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

El GUID del tipo de formato **es NULL,** pero el bloque de formato contiene la siguiente estructura:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



El **miembro dwDivision** especifica la división de tiempo del archivo. La división de tiempo se da en el encabezado de cualquier archivo MIDI estándar (SMF), en el `MThd` fragmento. El representador de MIDI establece esta propiedad en el flujo de datos de MIDI mediante una llamada a **la función midiStreamProperty.**

Los ejemplos del filtro analizador DE MIDI contienen un segundo de datos DE MIDI. El representador de MIDI usa **la función midiStreamOut** para representar los datos de MIDI. Cada ejemplo es un punto de sincronización: el inicio del búfer contiene todos los comandos necesarios para establecer el estado correcto para representar ese búfer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows.devices.midi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




