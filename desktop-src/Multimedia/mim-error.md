---
title: MIM_ERROR mensaje (Mmsystem.h)
description: El MIM error se envía a una función de devolución de llamada de entrada DE MIDI cuando se recibe \_ un mensaje MIDI no válido.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370874"
---
# <a name="mim_error-message"></a>\_MIM MENSAJE DE ERROR

El **MIM \_ error se** envía a una función de devolución de llamada de entrada DE MIDI cuando se recibe un mensaje NO VÁLIDO DE MIDI.


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Mensaje DE MIDI no válido que se recibió. El mensaje se empaqueta en un valor doubleword con el primer byte del mensaje en el byte de orden bajo.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Hora a la que el controlador del dispositivo de entrada recibió el mensaje. La marca de tiempo se especifica en milisegundos, empezando en cero cuando se llamó [**a la función midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

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

 

