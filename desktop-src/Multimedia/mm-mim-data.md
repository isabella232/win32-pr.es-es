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
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265943"
---
# <a name="mm_mim_data-message"></a>MENSAJE \_ DE MIM \_ MM

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



| Requisito | Value | Descripción |
|-----------|-----------------|-----------------------------------------------------|
| Palabra alta | Byte de orden superior | No se utiliza.                                           |
|           | Byte de orden bajo  | Contiene un segundo byte de datos DE MIDI (cuando sea necesario).  |
| Palabra baja  | Byte de orden superior | Contiene el primer byte de datos DE MIDI (cuando sea necesario). |
|           | Byte de orden bajo  | Contiene el estado de MIDI.                           |



 

Los dos bytes de datos de MIDI son opcionales, dependiendo del byte de estado de MIDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los mensajes DE MIDI recibidos de un puerto de entrada de MIDI tienen el estado de ejecución deshabilitado; cada mensaje se expande para incluir el byte de estado DE MIDI.

Este mensaje no se envía cuando se recibe un mensaje exclusivo del sistema MIDI. No hay ninguna marca de tiempo disponible con este mensaje. Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

 





