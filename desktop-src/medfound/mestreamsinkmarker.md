---
description: Lo genera un receptor de flujo después de llamar al método IMFStreamSink::P laceMarker.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Evento MEStreamSinkMarker (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd6866e8ef1633e4c743d466bb261e194c6ae7253924e34e8c30501b092f415a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228615"
---
# <a name="mestreamsinkmarker-event"></a>Evento MEStreamSinkMarker

Lo genera un receptor de flujo después de llamar al método [**IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE            | Descripción                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| >Cualquiera<br/> | El valor del evento es una copia de **PROPVARIANT** que el autor de la llamada especificó en el *parámetro pvarContextValue* del [**método PlaceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)<br/> <br/> |



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

[Receptores de medios](media-sinks.md)
</dt> </dl>

 

 




