---
title: Mensaje de MIM_LONGDATA (mmsystem. h)
description: El mensaje de LONGDATA de MIM \_ se envía a una función de devolución de llamada de entrada MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve a la aplicación.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- Mensaje de MIM_LONGDATA de Windows multimedia
topic_type:
- apiref
api_name:
- MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc5f83b1f0468540da18d0d8317dae42cbf33bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151235"
---
# <a name="mim_longdata-message"></a>Mensaje de LONGDATA de MIM \_

El mensaje de **\_ LONGDATA de MIM** se envía a una función de devolución de llamada de entrada MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve a la aplicación.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer de entrada.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Hora a la que el controlador del dispositivo de entrada recibió los datos. La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó a la función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.

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

 

