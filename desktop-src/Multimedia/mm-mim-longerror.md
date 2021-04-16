---
title: Mensaje de MM_MIM_LONGERROR (mmsystem. h)
description: El \_ mensaje LONGERROR de MIM de mm \_ se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- Mensaje de MM_MIM_LONGERROR de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686146"
---
# <a name="mm_mim_longerror-message"></a>Mensaje de LONGERROR de \_ MIM mm \_

El **mensaje \_ \_ LONGERROR de MIM de mm** se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI no válido o incompleto.


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada MIDI que recibió el mensaje no válido.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer que contiene el mensaje no válido.

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

 

