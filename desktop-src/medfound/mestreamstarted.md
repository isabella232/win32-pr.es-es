---
description: Lo genera una secuencia de medios cuando el origen comienza sin buscar. Una secuencia multimedia genera este evento cuando el origen multimedia genera el evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466805"
---
# <a name="mestreamstarted-event"></a>Evento MEStreamStarted

Lo genera una secuencia de medios cuando el origen comienza sin buscar. Una secuencia multimedia genera este evento cuando el origen multimedia genera el [evento MESourceStarted.](mesourcestarted.md)

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/>                                                                          |
| VT \_ I8<br/>    | Hora de inicio, en unidades de 100 nanosegundos, con respecto a las marcas de tiempo de los ejemplos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




