---
title: Mensaje de MIM_MOREDATA (mmsystem. h)
description: El mensaje de MOREDATA de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando \_ los mensajes de datos de MIM lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Mensaje de MIM_MOREDATA de Windows multimedia
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
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804099"
---
# <a name="mim_moredata-message"></a>Mensaje de MOREDATA de MIM \_

El mensaje de **\_ MOREDATA de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada. La función de devolución de llamada recibe este mensaje solo cuando la aplicación especifica el \_ Estado de e/s \_ de MIDI en la llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Especifica el mensaje MIDI recibido. El mensaje se empaqueta en un valor **DWORD** como se indica a continuación:



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

Especifica la hora a la que el controlador de dispositivo de entrada recibió el mensaje. La marca de tiempo se especifica en milisegundos, empezando en 0 cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una aplicación solo debe realizar una cantidad mínima de procesamiento de \_ mensajes MOREDATA de MIM. (En concreto, las aplicaciones no deben llamar a la función [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) mientras PROCESAn MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos de evento en un búfer y, a continuación, devolver.

Cuando una aplicación recibe un mensaje de [**\_ datos de MIM**](mim-data.md) después de una serie de mensajes de MOREDATA de MIM, se ha puesto al \_ día con los eventos MIDI entrantes y puede llamar a funciones con un uso intensivo de tiempo.

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

 

