---
description: Generado por un flujo multimedia cuando el origen comienza sin búsquedas. Un flujo multimedia genera este evento cuando el origen del medio genera el evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705990"
---
# <a name="mestreamstarted-event"></a>Evento MEStreamStarted

Generado por un flujo multimedia cuando el origen comienza sin búsquedas. Un flujo multimedia genera este evento cuando el origen del medio genera el evento [MESourceStarted](mesourcestarted.md) .

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/>                                                                          |
| VT \_ i8<br/>    | La hora de inicio, en unidades de 100-nanosegundos, con respecto a las marcas de tiempo de los ejemplos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




