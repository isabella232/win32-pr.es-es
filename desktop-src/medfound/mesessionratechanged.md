---
description: Lo genera la sesión multimedia cuando cambia la velocidad de reproducción. Este evento se envía después de que el método IMFRateControl::SetRate se complete de forma asincrónica.
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Evento MESessionRateChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682af0dbfde598e09ad3e80fd2e5594735e73758b9389faf2bd48540195a2773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941460"
---
# <a name="mesessionratechanged-event"></a>Evento MESessionRateChanged

Lo genera la sesión multimedia cuando cambia la velocidad de reproducción. Este evento se envía después de que el [**método IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se complete de forma asincrónica.

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
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




