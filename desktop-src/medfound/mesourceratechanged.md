---
description: 'Generado por un origen de medios cuando cambia la velocidad de reproducción. Este evento se envía después de que el método IMFRateControl:: SetRate se complete de forma asincrónica.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Evento MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154656"
---
# <a name="mesourceratechanged-event"></a>Evento MESourceRateChanged

Generado por un origen de medios cuando cambia la velocidad de reproducción. Este evento se envía después de que el método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se complete de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | La nueva velocidad de reproducción.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de tasa de implementación](implementing-rate-control.md)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Control de tasa](rate-control.md)
</dt> <dt>

[**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




