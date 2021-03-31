---
title: Mensaje de MM_MOM_POSITIONCB (mmsystem. h)
description: El \_ mensaje POSITIONCB de MOM de mm \_ se envía a una ventana cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- Mensaje de MM_MOM_POSITIONCB de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995995"
---
# <a name="mm_mom_positioncb-message"></a>Mensaje de POSITIONCB de \_ MOM de mm \_

El **mensaje \_ \_ POSITIONCB de MOM de mm** se envía a una ventana cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el evento que provocó la devolución de llamada. El miembro **dwOffset** proporciona el desplazamiento del evento.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Sector No use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La reproducción del búfer de secuencia continúa incluso mientras se ejecuta la función de devolución de llamada. Todos los eventos después del \_ \_ evento de devolución de llamada de MEVT F en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedique a la función de devolución de llamada.

Si se generan devoluciones de llamada de posición más rápidamente de lo que la aplicación puede procesar, el miembro **dwOffset** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) podría hacer referencia a un evento que la aplicación aún no ha procesado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes MIDI](midi-messages.md)
</dt> </dl>

 

