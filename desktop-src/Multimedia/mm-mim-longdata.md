---
title: MM_MIM_LONGDATA mensaje (Mmsystem.h)
description: El mensaje MM MIM LONGDATA se envía a una ventana cuando se recibe un mensaje completo exclusivo del sistema DE MIDI o cuando se ha rellenado un búfer con datos exclusivos \_ \_ del sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265903"
---
# <a name="mm_mim_longdata-message"></a>Mensaje \_ \_ LONGDATA MIM MM

El **mensaje MM MIM \_ \_ LONGDATA** se envía a una ventana cuando se recibe un mensaje completo exclusivo del sistema DE LÍNEA o cuando se ha rellenado un búfer con datos exclusivos del sistema.


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Controle el dispositivo de entrada MIDI que recibió los datos.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Para determinar el número de bytes registrados en el búfer devuelto, use el **miembro dwBytesRecorded** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a la que apunta *lpMidiHdr*.

No hay ninguna marca de tiempo disponible con este mensaje. Para los datos de entrada con marca de tiempo, debe usar los mensajes que se envían a las funciones de devolución de llamada.

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

 

