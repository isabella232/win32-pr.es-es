---
title: MM_MOM_POSITIONCB mensaje (Mmsystem.h)
description: El mensaje MM MOM POSITIONCB se envía a una ventana cuando se alcanza un evento \_ \_ MEVT \_ F \_ CALLBACK en el flujo de salida de MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB mensaje Windows Multimedia
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
ms.openlocfilehash: 4f68afecddd9b6ca8a0e5f6305b430b059b93db5a2abb966c0a7aed9ab350f7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807165"
---
# <a name="mm_mom_positioncb-message"></a>Mensaje \_ DE MM MOM \_ POSITIONCB

El **mensaje MM MOM \_ \_ POSITIONCB** se envía a una ventana cuando se alcanza un evento MEVT \_ F \_ CALLBACK en el flujo de salida DE MIDI.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el evento que produjo la devolución de llamada. El **miembro dwOffset** proporciona el desplazamiento del evento.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reservado; no se usan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

La reproducción del búfer de flujo continúa incluso mientras se ejecuta la función de devolución de llamada. Los eventos después del evento MEVT F CALLBACK en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedó a la función \_ \_ de devolución de llamada.

Si las devoluciones de llamada de posición se generan más rápidamente de lo que la aplicación puede procesarlas, el **miembro dwOffset** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) podría hacer referencia a un evento que la aplicación aún no ha procesado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

