---
description: Enviado por ELSOURCEMediaSource que encapsula el dispositivo para indicar que el dispositivo se ha quitado.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f209dc4be6e8f45639b060de1328cb04c932463f6b76355b7538b5649a69634e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013485"
---
# <a name="mevideocapturedeviceremoved-event"></a>Evento MEVideoCaptureDeviceRemoved

Enviado por [**ELSOURCEMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula el dispositivo para indicar que el dispositivo se ha quitado.

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

 

 




