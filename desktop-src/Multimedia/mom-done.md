---
title: Mensaje de MOM_DONE (Mciapi. h)
description: El \_ mensaje MOM done se envía a una función de devolución de llamada de salida MIDI cuando se ha reproducido el búfer de secuencia o exclusivo del sistema especificado y se va a devolver a la aplicación.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- Mensaje de MOM_DONE de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422181"
---
# <a name="mom_done-message"></a>Mensaje de MOM \_ Done

El mensaje **MOM \_ Done** se envía a una función de devolución de llamada de salida MIDI cuando se ha reproducido el búfer de secuencia o exclusivo del sistema especificado y se va a devolver a la aplicación.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Sector No use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes MIDI](midi-messages.md)
</dt> </dl>

 

