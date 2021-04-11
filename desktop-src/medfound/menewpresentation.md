---
description: Generado por un origen multimedia que proporciona topologías a través de la interfaz IMFMediaSourceTopologyProvider, como el origen del secuenciador. El origen provoca el evento cuando tiene una presentación nueva. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275974"
---
# <a name="menewpresentation-event"></a>Evento MENewPresentation

Generado por un origen multimedia que proporciona topologías a través de la interfaz [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , como el origen del secuenciador. El origen provoca el evento cuando tiene una presentación nueva. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ desconocido<br/> | Puntero a la interfaz [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación de la nueva presentación.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La aplicación puede obtener la topología que corresponde al descriptor de presentación mediante una llamada a [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen del medio. A continuación, la aplicación puede poner en cola la nueva topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




