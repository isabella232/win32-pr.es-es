---
title: MOM_POSITIONCB mensaje (Mmsystem.h)
description: El mensaje MOM POSITION se envía cuando se alcanza un \_ evento MEVT \_ F \_ CALLBACK en el flujo de salida de MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB mensaje Windows Multimedia
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265791"
---
# <a name="mom_positioncb-message"></a>Mensaje \_ MOM POSITIONCB

El **mensaje \_ MOM POSITION** se envía cuando se alcanza un evento **MEVT F \_ \_ CALLBACK** en el flujo de salida de MIDI.

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

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

La reproducción del búfer de flujo continúa incluso mientras se ejecuta la función de devolución de llamada. Los eventos después del evento **MEVT \_ F \_ CALLBACK** en el búfer se programarán y enviarán a tiempo, independientemente de cuánto tiempo se dedó en la función de devolución de llamada.

Si las devoluciones de llamada de posición se generan más rápidamente de lo que la aplicación puede procesarlas, el **miembro dwOffset** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) podría hacer referencia a un evento que la aplicación aún no ha procesado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

