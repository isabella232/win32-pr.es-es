---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) en respuesta a un \_ mensaje de marcador de comando de mensaje MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677593"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Enviado por una transformación de Media Foundation asincrónica (MFT) en respuesta a un mensaje de **\_ marcador de \_ comando \_ de mensaje MFT** .

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                      | Descripción                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ contexto MFT del evento MF \_](mf-event-mft-context.md)<br/> | El valor del parámetro *ulParam* del mensaje del **\_ marcador de \_ comando \_ del mensaje de MFT** .<br/>*Desee*<br/> |



## <a name="remarks"></a>Observaciones

Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Los MFTs sincrónicos nunca envían este evento.

El cliente de un MFT asincrónico puede colocar un marcador en la secuencia mediante una llamada a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje del marcador de comando del mensaje de **MFT \_ \_ \_** . El parámetro *ulParam* contiene datos definidos por la aplicación.

Cuando el MFT finaliza el procesamiento de todos los datos de entrada que estaban disponibles en el momento de la llamada a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , el MFT pone en cola un evento METransformMarker. El atributo de [ \_ \_ \_ contexto MFT del evento MF](mf-event-mft-context.md) del evento contiene el valor del parámetro *ulParam* . Para obtener más información, consulte [MFTs asincrónico](asynchronous-mfts.md).

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

 

 




