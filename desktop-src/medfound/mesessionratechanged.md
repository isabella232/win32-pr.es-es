---
description: Lo genera la sesión multimedia cuando cambia la velocidad de reproducción. Este evento se envía después de que el método IMFRateControl::SetRate se complete de forma asincrónica.
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Evento MESessionRateChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257884"
---
# <a name="mesessionratechanged-event"></a>Evento MESessionRateChanged

Lo genera la sesión multimedia cuando cambia la velocidad de reproducción. Este evento se envía después de que [**el método IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se complete de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE           | Descripción                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| VT \_ R4<br/> | La nueva velocidad de reproducción, expresada como una proporción de la velocidad de reproducción normal.<br/> <br/> |



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

 

 




