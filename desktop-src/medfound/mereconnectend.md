---
description: Indica que un origen multimedia ha completado un intento de volver a conectarse al servidor.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Evento MEReconnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544382"
---
# <a name="mereconnectend-event"></a>Evento MEReconnectEnd

Indica que un origen multimedia ha completado un intento de volver a conectarse al servidor.

Generado por un origen multimedia al final de un intento de reconexión. El origen de red genera este evento si se vuelve a conectar al servidor. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



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

 

 




