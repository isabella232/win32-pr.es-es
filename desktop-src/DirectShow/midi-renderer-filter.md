---
description: El filtro de representador MIDI representa datos MIDI del filtro de analizador MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de representador MIDI (Windows. Devices. MIDI. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690778"
---
# <a name="midi-renderer-filter"></a>Filtro de representador MIDI

El filtro de representador MIDI representa datos MIDI del filtro de [analizador MIDI](midi-parser-filter.md) .



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                                                                                                                  |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Tipos de medios de anclaje de salida                   | No aplicable                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de clavija de salida                    | No aplicable                                                                                                                                                                                                                                                                                                                                                                       |
| Identificador CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                                                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ preferido                                                                                                                                                                                                                                                                                                                                                                     |
| [Categoría de filtro](filter-categories.md) | CLSID \_ MidiRendererCategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Observaciones

El GUID para el tipo de formato es **null**, pero el bloque de formato contiene la siguiente estructura:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



El miembro **dwDivision** especifica la división de tiempo del archivo. La división de tiempo se proporciona en el encabezado de cualquier archivo MIDI estándar (SMF) del `MThd` fragmento. El representador MIDI establece esta propiedad en el flujo de datos MIDI mediante una llamada a la función **midiStreamProperty** .

Los ejemplos del filtro del analizador MIDI contienen un segundo de datos MIDI. El representador MIDI utiliza la función **midiStreamOut** para representar los datos MIDI. Cada ejemplo es un punto de sincronización: el inicio del búfer contiene todos los comandos necesarios para establecer el estado correcto para representar ese búfer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Windows. Devices. MIDI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




