---
description: Indica que un origen multimedia está intentando volver a conectarse al servidor.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Evento MEReconnectStart (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc365acf5d91796b6d9c3fe371b9a0ec54435769381c41f0bf45cedb73003660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114015"
---
# <a name="mereconnectstart-event"></a>Evento MEReconnectStart

Indica que un origen multimedia está intentando volver a conectarse al servidor.

Lo genera un origen multimedia al principio de un intento de reconexión. El origen de red genera este evento si intenta volver a conectarse al servidor. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




