---
title: Mensaje de MOM_POSITIONCB (mmsystem. h)
description: El mensaje de posición de MOM \_ se envía cuando \_ \_ se alcanza un evento de devolución de llamada de MEVT F en el flujo de salida de MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- Mensaje de MOM_POSITIONCB de Windows multimedia
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803667"
---
# <a name="mom_positioncb-message"></a>Mensaje de POSITIONCB de MOM \_

El mensaje de **\_ posición de MOM** se envía cuando se alcanza un evento de **devolución de \_ \_ llamada de MEVT F** en el flujo de salida de MIDI.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntero a una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer de entrada.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La reproducción del búfer de secuencia continúa incluso mientras se ejecuta la función de devolución de llamada. Todos los eventos después del evento de **\_ devolución de \_ llamada de MEVT F** en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedique a la función de devolución de llamada.

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

 

