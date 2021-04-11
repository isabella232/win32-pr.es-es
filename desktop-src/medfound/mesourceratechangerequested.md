---
description: 'Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción. La aplicación debe llamar a IMFRateControl:: SetRate con la tasa solicitada. Un origen multimedia podría producir este evento si no puede continuar la reproducción a la velocidad actual.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275967"
---
# <a name="mesourceratechangerequested-event"></a>Evento MESourceRateChangeRequested

Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción. La aplicación debe llamar a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la tasa solicitada. Un origen multimedia podría producir este evento si no puede continuar la reproducción a la velocidad actual.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | La nueva velocidad de reproducción solicitada.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                    | Descripción                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**el \_ evento \_ MF \_ simplifica**](mf-event-do-thinning-attribute.md)<br/> | Especifica si el origen multimedia también solicita el ligero.<br/> <br/> |



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

 

 




