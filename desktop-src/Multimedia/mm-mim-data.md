---
title: MM_MIM_DATA mensaje (Mmsystem.h)
description: El mensaje MM MIM DATA se envía a una ventana cuando un dispositivo de entrada MIDI recibe un \_ \_ mensaje MIDI completo.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA mensaje Windows Multimedia
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
ms.openlocfilehash: 4309149c8b69fd4396de3a4e67ab18c49008dd7051ed52d4fe992867d1262fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807385"
---
# <a name="mm_mim_data-message"></a>Mensaje \_ MM MIM \_ DATA

El **mensaje MM MIM \_ \_ DATA** se envía a una ventana cuando un dispositivo de entrada MIDI recibe un mensaje MIDI completo.


```C++
MM_MIM_DATA 
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

Mensaje DE MIDI que se recibió. El mensaje se empaqueta en un valor doubleword como se indica a continuación:



| Requisito | Valor | Descripción |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se usa.                                           |
|           | Byte de orden bajo  | Contiene un segundo byte de datos DE MIDI (cuando sea necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos DE MIDI (cuando sea necesario). |
|           | Byte de orden bajo  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Los mensajes DE MIDI recibidos de un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.

Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI. No hay ninguna marca de tiempo disponible con este mensaje. Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 





