---
title: Mensaje de MM_MIM_MOREDATA (mmsystem. h)
description: El mensaje de MOREDATA de MIM de MM \_ \_ se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando \_ los mensajes de datos de MIM lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- Mensaje de MM_MIM_MOREDATA de Windows multimedia
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
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079345"
---
# <a name="mm_mim_moredata-message"></a>Mensaje de MOREDATA de \_ MIM mm \_

El mensaje de **\_ \_ MOREDATA de MIM de mm** se envía a una ventana de devolución de llamada cuando un dispositivo de entrada MIDI recibe un mensaje MIDI, pero la aplicación no está procesando los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada. La ventana recibe este mensaje solo cuando la aplicación especifica el \_ Estado de e/s \_ de MIDI en la llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MM_MIM_MOREDATA 
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

Especifica el mensaje MIDI recibido. El mensaje se empaqueta en un valor de palabra como se indica a continuación:



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

Si la aplicación va a recibir datos MIDI más rápido de lo que puede procesarlos, no debe utilizar un mecanismo de devolución de llamada de ventana. Para maximizar la velocidad, use una función de devolución de llamada y use el mensaje de [**\_ MOREDATA de MIM**](mim-moredata.md) en lugar de mm \_ MIM \_ MOREDATA.

Una aplicación solo debe realizar una cantidad mínima de procesamiento de mensajes de MOREDATA de MIM de MM \_ \_ . (En particular, las aplicaciones no deben llamar a la función [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) mientras PROCESAn mm \_ MIM \_ MOREDATA). En su lugar, la aplicación debe colocar los datos de evento en un búfer y, a continuación, devolver.

Cuando una aplicación recibe un mensaje de [**\_ \_ datos de mm MIM**](mm-mim-data.md) después de una serie de mensajes de MOREDATA de MIM de mm, se ha puesto al \_ \_ día con los eventos MIDI entrantes y puede llamar a funciones que consumen mucho tiempo.

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

 

