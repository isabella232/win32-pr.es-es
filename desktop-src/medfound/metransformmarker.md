---
description: Enviado por una transformación Media Foundation (MFT) asincrónica en respuesta a un mensaje DE MARCADOR DE COMANDO DE MENSAJE \_ de MFT. \_ \_
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474244"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Enviado por una transformación de Media Foundation (MFT) asincrónica en respuesta a un **mensaje DE MARCADOR DE COMANDO DE MENSAJE \_ \_ \_ de MFT.**

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                      | Descripción                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CONTEXTO \_ \_ MFT DEL EVENTO \_ MF](mf-event-mft-context.md)<br/> | Valor del parámetro *ulParam* del **mensaje \_ MFT MESSAGE \_ COMMAND \_ MARKER.**<br/>*(Obligatorio)*<br/> |



## <a name="remarks"></a>Observaciones

Las MTA asincrónicas envían este evento [**a través de la interfaz DESEDMEDIAEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Las MTA sincrónicas nunca envían este evento.

El cliente de un MFT asincrónico puede colocar un marcador en la secuencia mediante una llamada a [**IMFTransform::P rocessMessage con**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) el mensaje **MFT \_ MESSAGE COMMAND \_ \_ MARKER.** El *parámetro ulParam* contiene datos definidos por la aplicación.

Cuando MFT termina de procesar todos los datos de entrada disponibles en el momento de la llamada a [**ProcessMessage,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) MFT pone en cola un evento METransformMarker. El [atributo MF EVENT \_ \_ MFT \_ CONTEXT](mf-event-mft-context.md) del evento contiene el valor del *parámetro ulParam.* Para obtener más información, vea [MFT asincrónicas.](asynchronous-mfts.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> </dl>

 

 




