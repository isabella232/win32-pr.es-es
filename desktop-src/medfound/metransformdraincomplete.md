---
description: Enviado por una transformación de Media Foundation (MFT) asincrónica cuando se completa una operación de purga.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974034"
---
# <a name="metransformdraincomplete-event"></a>Evento METransformDrainComplete

Enviado por una transformación de Media Foundation (MFT) asincrónica cuando se completa una operación de purga.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                        | Descripción                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ID. \_ DE FLUJO DE ENTRADA DE \_ MFT DE EVENTO \_ \_ \_ MF](mf-event-mft-input-stream-id.md)<br/> | Identificador de la secuencia que se ha purgado.<br/>*(Obligatorio)*<br/> |



## <a name="remarks"></a>Comentarios

Las MTA asincrónicas envían este evento [**a través de la interfaz DESEDMEDIAEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Las MTA sincrónicas nunca envían este evento.

Para purgar un MFT, llame [**a IMFTransform::P rocessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) el mensaje DE PURGA **DEL COMANDO \_ \_ MFT \_ MESSAGE.** Especifique el flujo de entrada que se va a purgar *en el parámetro ulParam.* Cuando se completa la operación de purga, un MFT asincrónico envía el evento METransformDrainComplete. El [atributo MF EVENT \_ \_ MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) del evento contiene el identificador de flujo especificado en *el parámetro ulParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> </dl>

 

 




