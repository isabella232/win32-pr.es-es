---
description: Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción. La aplicación debe llamar a IMFRateControl::SetRate con la velocidad solicitada. Un origen multimedia podría generar este evento si no puede continuar la reproducción a la velocidad actual.
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d8a88225fd3a0a95c56d549a712b295ba562cc684c08fe4b762c0169e3637c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974134"
---
# <a name="mesourceratechangerequested-event"></a>Evento MESourceRateChangeRequested

Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción. La aplicación debe llamar [**a IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la velocidad solicitada. Un origen multimedia podría generar este evento si no puede continuar la reproducción a la velocidad actual.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE           | Descripción                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Nueva velocidad de reproducción solicitada.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                    | Descripción                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ \_ DONNING**](mf-event-do-thinning-attribute.md)<br/> | Especifica si el origen de medios también solicita la simplificación.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




