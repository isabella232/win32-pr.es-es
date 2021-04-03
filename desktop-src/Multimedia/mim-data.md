---
title: Mensaje de MIM_DATA (mmsystem. h)
description: El mensaje de datos de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- Mensaje de MIM_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905659"
---
# <a name="mim_data-message"></a>Mensaje de datos de MIM \_

El mensaje de **\_ datos de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Mensaje MIDI recibido. El mensaje se empaqueta en un valor de palabra como se indica a continuación:



| Requisito | Value |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se utiliza.                                           |
|           | Byte de orden inferior  | Contiene un segundo byte de datos MIDI (si es necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos MIDI (si es necesario). |
|           | Byte de orden inferior  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Hora en que el controlador del dispositivo de entrada recibió el mensaje. La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.

No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensajes MIDI](midi-messages.md)
</dt> </dl>

 

