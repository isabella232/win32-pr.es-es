---
description: Lo genera una secuencia multimedia cuando inicia o detiene la simplificación de la secuencia. Para obtener información sobre la simplificación, vea Acerca del control de velocidad.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13a9cc5b625a8b366bece1debc2017fce51e35d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479521"
---
# <a name="mestreamthinmode-event"></a>Evento MEStreamThinMode

Lo genera una secuencia multimedia cuando inicia o detiene la simplificación de la secuencia. Para obtener información sobre *la simplificación,* vea [About Rate Control](about-rate-control.md).

Este evento se puede enviar en respuesta al método [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) o al método [**IMFQualityAdvise::SetDropMode.**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode)

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.




| VARTYPE | Descripción | 
|---------|-------------|
| VT_BOOL<br /> | Indica si la simplificación se ha iniciado o detenido.<br /><ul><li>VARIANT_TRUE: los ejemplos entregados después de este evento se afilan.</li><li>VARIANT_FALSE: los ejemplos entregados después de este evento no se thinned.</li></ul><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




