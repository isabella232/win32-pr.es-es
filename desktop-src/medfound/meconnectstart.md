---
description: Lo genera el origen de red cuando comienza a abrir una dirección URL.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Evento MEConnectStart (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01360d452e6b20bde9e7aaaaf9e678cab1b3c6fe912e9682949dfc24e1e7d5cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013855"
---
# <a name="meconnectstart-event"></a>Evento MEConnectStart

Lo genera el origen de red cuando comienza a abrir una dirección URL.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

El origen de red envía este evento directamente a la aplicación a través del método [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) de la aplicación, no a través de la interfaz [**USUAL DEMEMEDIAEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




