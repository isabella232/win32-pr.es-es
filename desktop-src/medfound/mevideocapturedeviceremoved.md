---
description: Enviado por el IMFMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha quitado.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678161"
---
# <a name="mevideocapturedeviceremoved-event"></a>Evento MEVideoCaptureDeviceRemoved

Enviado por el [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha quitado.

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

 

 




