---
description: Lo genera una autoridad de confianza de salida (OTA) cuando el método IMFOutputTrustAuthority::SetPolicy se completa de forma asincrónica.
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064cbb92e85e300aa2c2b7db28d08b01296834413ed92e36eb5b7ce88e5486c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877562"
---
# <a name="mepolicyset-event"></a>Evento MEPolicySet

Lo genera una autoridad de confianza de salida (OTA) cuando el método [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) se completa de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |
| VT \_ UI4<br/> | Identificador que se puede establecer en [UN ELEMENTO IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) a través [del MF_POLICY_ID](mf-policy-id.md) atributo .<br/> <br/> |



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

 

 




