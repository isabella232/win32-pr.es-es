---
description: Lo genera un origen multimedia que proporciona topologías a través de la interfaz IMFMediaSourceTopologyProvider, como el origen del secuenciador. El origen genera el evento cuando tiene una nueva presentación. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2adec5b3dbb8544e537bdcc8f5c724130175b3167f9c51dc005112fdbd9a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228885"
---
# <a name="menewpresentation-event"></a>Evento MENewPresentation

Lo genera un origen multimedia que proporciona topologías a través de la interfaz [**IMFMediaSourceTopologyProvider,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) como el origen del secuenciador. El origen genera el evento cuando tiene una nueva presentación. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE                | Descripción                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descriptor de presentación para la nueva presentación.<br/> <br/> |



## <a name="remarks"></a>Observaciones

La aplicación puede obtener la topología correspondiente al descriptor de presentación llamando a [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) en el origen multimedia. A continuación, la aplicación puede poner en cola la nueva topología en la sesión multimedia llamando a [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 




