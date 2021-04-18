---
description: Enviado por el IMFMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687224"
---
# <a name="mevideocapturedevicepreempted-event"></a>Evento MEVideoCaptureDevicePreempted

Enviado por el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha adelantado.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ vacío <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento lo envía el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




