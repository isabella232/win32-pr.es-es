---
title: Mensaje de MM_MIM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MIM de mm \_ se envía a una ventana cuando se abre un dispositivo de entrada MIDI.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- Mensaje de MM_MIM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904978"
---
# <a name="mm_mim_open-message"></a>\_Mensaje abierto de MIM de mm \_

El **mensaje \_ \_ abierto de MIM de mm** se envía a una ventana cuando se abre un dispositivo de entrada MIDI.


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador del dispositivo de entrada MIDI que se abrió.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Sector No use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

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

 

 





