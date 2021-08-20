---
title: MIM_LONGDATA mensaje (Mmsystem.h)
description: El MIM longdata se envía a una función de devolución de llamada de entrada DE MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve \_ a la aplicación.
ms.assetid: 3a11ed21-e7c5-4b78-9536-f0d862e26a02
keywords:
- MIM_LONGDATA mensaje Windows Multimedia
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
ms.openlocfilehash: 82605835ce8ac231346014215c854abfe9ae7a55fd81e81b8d6214fb8a230327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137216"
---
# <a name="mim_longdata-message"></a>\_MIM Mensaje LONGDATA

El **MIM \_ longdata** se envía a una función de devolución de llamada de entrada DE MIDI cuando un búfer exclusivo del sistema se ha rellenado con datos y se devuelve a la aplicación.


```C++
MIM_LONGDATA 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer de entrada.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Hora a la que el controlador del dispositivo de entrada recibió los datos. La marca de tiempo se especifica en milisegundos, empezando por cero cuando se llamó [**a la función midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Es posible que el búfer devuelto no esté lleno. Para determinar el número de bytes registrados en el búfer devuelto, use el **miembro dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) especificada por *lpMidiHdr*.

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

 

