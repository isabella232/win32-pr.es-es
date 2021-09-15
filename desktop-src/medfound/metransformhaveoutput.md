---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) cuando hay nuevos datos de salida disponibles desde MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformTransformTransformOutput (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474245"
---
# <a name="metransformhaveoutput-event"></a>Evento METransformTransformTransformOutput

Enviado por una transformación de Media Foundation asincrónica (MFT) cuando hay nuevos datos de salida disponibles desde MFT.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> |



## <a name="attributes"></a>Atributos

No hay atributos definidos para este evento.

## <a name="remarks"></a>Observaciones

Las MTA asincrónicas envían este evento a través [**de la interfaz DEFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Los MFT sincrónicos nunca envían este evento.

Cuando el cliente de MFT recibe este evento, debe llamar a [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener la salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> </dl>

 

 




