---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474243"
---
# <a name="metransformneedinput-event"></a>Evento METransformNeedInput

Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                        | Descripción                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID. \_ DE FLUJO DE ENTRADA DE MF EVENT \_ MFT \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificador del flujo que necesita datos de entrada.<br/>*(Obligatorio)*<br/> |



## <a name="remarks"></a>Observaciones

Las MTA asincrónicas envían este evento a través [**de la interfaz DEFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Los MFT sincrónicos nunca envían este evento.

Cuando el cliente de MFT recibe este evento, debe llamar a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar el ejemplo siguiente. El [atributo MF EVENT \_ \_ MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) del objeto de evento especifica qué flujo de entrada requiere datos.

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

[MFT asincrónicos](asynchronous-mfts.md)
</dt> </dl>

 

 




