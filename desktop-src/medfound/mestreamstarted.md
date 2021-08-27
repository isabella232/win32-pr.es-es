---
description: Lo genera una secuencia multimedia cuando el origen comienza sin buscar. Una secuencia multimedia genera este evento cuando el origen multimedia genera el evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113945"
---
# <a name="mestreamstarted-event"></a>Evento MEStreamStarted

Lo genera una secuencia multimedia cuando el origen comienza sin buscar. Una secuencia multimedia genera este evento cuando el origen multimedia genera el [evento MESourceStarted.](mesourcestarted.md)

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/>                                                                          |
| VT \_ I8<br/>    | Hora de inicio, en unidades de 100 nanosegundos, con respecto a las marcas de tiempo de los ejemplos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




