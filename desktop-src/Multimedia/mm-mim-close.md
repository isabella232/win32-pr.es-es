---
title: Mensaje de MM_MIM_CLOSE (mmsystem. h)
description: El mensaje de cierre de MIM de MM \_ \_ se envía a una ventana cuando se cierra un dispositivo de entrada MIDI.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- Mensaje de MM_MIM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996696"
---
# <a name="mm_mim_close-message"></a>Mensaje de cierre de MM \_ MIM \_

El mensaje de **\_ \_ cierre de MIM de mm** se envía a una ventana cuando se cierra un dispositivo de entrada MIDI.


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada MIDI que se cerró.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Sector No use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El identificador de dispositivo ya no es válido después de enviar este mensaje.

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

 

 





