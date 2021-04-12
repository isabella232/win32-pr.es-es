---
description: Lo envía una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361348"
---
# <a name="metransformdraincomplete-event"></a>Evento METransformDrainComplete

Lo envía una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                        | Descripción                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [\_identificador de \_ flujo de entrada de MFT de evento MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificador de la secuencia que se ha purgado.<br/>*Desee*<br/> |



## <a name="remarks"></a>Observaciones

Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Los MFTs sincrónicos nunca envían este evento.

Para purgar un MFT, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de **agotamiento del comando de mensaje de MFT \_ \_ \_** . Especifique el flujo de entrada que se va a purgar en el parámetro *ulParam* . Cuando se completa la operación de purga, un MFT asincrónico envía el evento METransformDrainComplete. El atributo de [identificador de flujo de entrada de \_ MFT del evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) del evento contiene el identificador de flujo proporcionado en el parámetro *ulParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> </dl>

 

 




