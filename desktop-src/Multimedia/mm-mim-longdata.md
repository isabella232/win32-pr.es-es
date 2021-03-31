---
title: Mensaje de MM_MIM_LONGDATA (mmsystem. h)
description: El mensaje de LONGDATA de MIM de MM \_ \_ se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- Mensaje de MM_MIM_LONGDATA de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151027"
---
# <a name="mm_mim_longdata-message"></a>Mensaje de LONGDATA de \_ MIM mm \_

El mensaje de **\_ \_ LONGDATA de MIM de mm** se envía a una ventana cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada MIDI que recibió los datos.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Para determinar el número de bytes grabados en el búfer devuelto, use el miembro **dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a la que apunta *lpMidiHdr*.

No hay ninguna marca de tiempo disponible con este mensaje. En el caso de los datos de entrada con marca de tiempo, debe utilizar los mensajes que se envían a las funciones de devolución de llamada.

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

 

