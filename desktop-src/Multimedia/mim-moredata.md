---
title: MIM_MOREDATA mensaje (Mmsystem.h)
description: El mensaje MIM MOREDATA se envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada DE LÍNEA recibe un mensaje MIDI, pero la aplicación no procesa los mensajes data de MIM lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de \_ \_ entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 130a07d1d205e9944c7be6ab9ad1294e09d0ebdcdb81d5befc5468ff5a65218f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782975"
---
# <a name="mim_moredata-message"></a>\_MIM Mensaje MOREDATA

El **MIM \_ mensaje MOREDATA** se envía a una función de devolución de llamada de entrada DE MIDI cuando un dispositivo de entrada DE LÍNEA recibe un mensaje MIDI, pero la aplicación no procesa los mensajes data de [**MIM \_**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de entrada. La función de devolución de llamada recibe este mensaje solo cuando la aplicación especifica EL ESTADO DE E/S de MIDI en la llamada \_ \_ a la función [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Especifica el mensaje MIDI que se recibió. El mensaje se empaqueta en un **valor DWORD** como se indica a continuación:



| Requisito | Value | Descripción |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se usa.                                           |
|           | Byte de orden bajo  | Contiene un segundo byte de datos DE MIDI (cuando sea necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos DE MIDI (cuando sea necesario). |
|           | Byte de orden bajo  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Especifica la hora a la que el controlador de dispositivo de entrada recibió el mensaje. La marca de tiempo se especifica en milisegundos, empezando en 0 cuando se llamó [**a la función midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Una aplicación solo debe realizar una cantidad mínima de procesamiento de MIM \_ mensajes MOREDATA. (En concreto, las aplicaciones no deben llamar a la [función PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) mientras se procesa MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos del evento en un búfer y, a continuación, devolver.

Cuando una aplicación recibe un mensaje [**MIM \_ DATA**](mim-data.md) después de una serie de mensajes MOREDATA de MIM, se ha puesto al día con los eventos ENTRANTEs de MIDI y puede llamar de forma segura a funciones que requieren mucho \_ tiempo.

Los mensajes DE MIDI recibidos de un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.

Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

