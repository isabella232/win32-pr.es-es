---
description: Lo genera un receptor de flujo cuando la velocidad ha cambiado.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Evento MEStreamSinkRateChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43a3a4cbff4464f78e71d3047e2b9ccaddfcbf38adcb5e84bab8f5ae49c5d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827145"
---
# <a name="mestreamsinkratechanged-event"></a>Evento MEStreamSinkRateChanged

Lo genera un receptor de flujo cuando la velocidad ha cambiado.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Si un receptor de flujo admite cambios de velocidad, envía este evento una vez completado el cambio de velocidad. El evento se envía una vez por cada llamada al método [**IMFClockStateSink::OnClockSetRate del**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) receptor. Si el cambio de velocidad no se realiza correctamente, el valor de estado del evento es un código de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Receptores multimedia](media-sinks.md)
</dt> </dl>

 

 




