---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013505"
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
| [ID. \_ DE FLUJO DE ENTRADA DE \_ MFT DE EVENTO \_ \_ \_ MF](mf-event-mft-input-stream-id.md)<br/> | Identificador del flujo que necesita datos de entrada.<br/>*(Obligatorio)*<br/> |



## <a name="remarks"></a>Comentarios

Las MTA asincrónicas envían este evento [**a través de la interfaz DESEDMEDIAEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Las MTA sincrónicas nunca envían este evento.

Cuando el cliente de MFT recibe este evento, debe llamar a [**ASETransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar el ejemplo siguiente. El [atributo MF EVENT \_ \_ MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) del objeto de evento especifica qué flujo de entrada requiere datos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> </dl>

 

 




