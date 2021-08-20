---
description: Enviado por el método IMFMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78246d6560344735167fc6efd45ba0481095534977c67dac11a76ffae0947d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061168"
---
# <a name="mevideocapturedevicepreempted-event"></a>Evento MEVideoCaptureDevicePreempted

Enviado por [**ELSOURCEMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este evento se envía mediante [**el método IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




