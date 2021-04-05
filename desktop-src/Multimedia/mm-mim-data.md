---
title: Mensaje de MM_MIM_DATA (mmsystem. h)
description: El \_ mensaje de datos de MIM mm \_ se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje MIDI completo.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- Mensaje de MM_MIM_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078977"
---
# <a name="mm_mim_data-message"></a>Mensaje de datos de MM \_ MIM \_

El mensaje de **\_ \_ datos de MIM mm** se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje MIDI completo.


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada MIDI que recibió el mensaje MIDI.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Mensaje MIDI recibido. El mensaje se empaqueta en un valor de palabra como se indica a continuación:



| Requisito | Value |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se utiliza.                                           |
|           | Byte de orden inferior  | Contiene un segundo byte de datos MIDI (si es necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos MIDI (si es necesario). |
|           | Byte de orden inferior  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los mensajes MIDI recibidos de un puerto de entrada MIDI tienen el estado de en ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado de MIDI.

No se envía este mensaje cuando se recibe un mensaje de sistema exclusivo de MIDI. No hay ninguna marca de tiempo disponible con este mensaje. En el caso de los datos de entrada con marca de tiempo, debe utilizar los mensajes que se envían a las funciones de devolución de llamada.

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

 

 





