---
description: El filtro Representador de MIDI representa los datos DE MIDI del filtro analizador de MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de representador de MIDI (Windows.devices.midi.h)
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
ms.openlocfilehash: 3727fb322e03338723eb3c9da1ac86d4e6a7145424cb04b0c050b67f83aa141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791455"
---
# <a name="midi-renderer-filter"></a>Filtro del representador de MIDI

El filtro Representador de MIDI representa los datos DE MIDI del [filtro analizador de MIDI.](midi-parser-filter.md)



| Etiqueta | Valor |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMClockControle,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirect Sound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




