---
description: Se genera cuando un origen multimedia busca una nueva posición. Un origen multimedia genera este evento si el origen está en ejecución o en pausa y la aplicación llama a IMFMediaSource::Start con una hora de inicio que no es igual a la posición actual.
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b913089ca40895a782f3c013b752db25fe754443ae6d79b410da98e759b4b8ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941415"
---
# <a name="mesourceseeked-event"></a>Evento MESourceSeeked

Se genera cuando un origen multimedia busca una nueva posición. Un origen multimedia genera este evento si el origen está en ejecución o en pausa y la aplicación llama a [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con una hora de inicio que no es igual a la posición actual.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE           | Descripción                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | Nueva posición inicial, en unidades de 100 nanosegundos.<br/> <br/> |



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

 

 




