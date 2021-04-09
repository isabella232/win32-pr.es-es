---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154652"
---
# <a name="metransformneedinput-event"></a>Evento METransformNeedInput

Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                        | Descripción                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_identificador de \_ flujo de entrada de MFT de evento MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificador de la secuencia que necesita datos de entrada.<br/>*Desee*<br/> |



## <a name="remarks"></a>Observaciones

Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Los MFTs sincrónicos nunca envían este evento.

Cuando el cliente del MFT recibe este evento, debe llamar a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para ofrecer el ejemplo siguiente. El atributo de [identificador de flujo de entrada de \_ MFT del evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) del objeto de evento especifica qué flujo de entrada requiere datos.

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

 

 




