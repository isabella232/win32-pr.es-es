---
title: MM_MIM_MOREDATA mensaje (Mmsystem.h)
description: El mensaje MM MIM MOREDATA se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE MIM lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de \_ \_ \_ entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120030"
---
# <a name="mm_mim_moredata-message"></a>Mensaje \_ MM MIM \_ MOREDATA

El **mensaje MM \_ MIM \_ MOREDATA** se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no procesa los mensajes DE DATOS DE [**MIM \_**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador del dispositivo de entrada. La ventana recibe este mensaje solo cuando la aplicación especifica EL ESTADO DE E/S DE MIDI en \_ la llamada a la función \_ [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Controle el dispositivo de entrada de MIDI que recibió el mensaje DE MIDI.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Especifica el mensaje MIDI que se recibió. El mensaje se empaqueta en un valor doubleword como se indica a continuación:



| Requisito | Valor | Descripción |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se usa.                                           |
|           | Byte de orden bajo  | Contiene un segundo byte de datos MIDI (cuando sea necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos DE MIDI (cuando sea necesario). |
|           | Byte de orden bajo  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si la aplicación recibirá datos DE MIDI más rápido de lo que puede procesar, no debe usar un mecanismo de devolución de llamada de ventana. Para maximizar la velocidad, use una función de devolución de llamada y use el mensaje [**\_ MOREDATA de MIM**](mim-moredata.md) en lugar de MM \_ MIM \_ MOREDATA.

Una aplicación solo debe realizar una cantidad mínima de procesamiento de mensajes \_ \_ MOREDATA de MM MIM. (En concreto, las aplicaciones no deben llamar a la [función PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante el procesamiento de MM \_ MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos del evento en un búfer y, a continuación, devolver.

Cuando una aplicación recibe un mensaje [**MM \_ MIM \_ DATA**](mm-mim-data.md) después de una serie de mensajes \_ MM MIM MOREDATA, se ha puesto al día con los eventos ENTRANTES DE MIDI y puede llamar de forma segura a funciones que consumen mucho \_ tiempo.

Los mensajes DE MIDI recibidos desde un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.

Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI. No hay ninguna marca de tiempo disponible con este mensaje. Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluye Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

