---
description: Lo genera una secuencia de medios cuando finaliza la secuencia.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Evento MEEndOfStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23a2db351d31558a617b72a8640d121b71c866021063d4791d19797108f34819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877778"
---
# <a name="meendofstream-event"></a>Evento MEEndOfStream

Lo genera una secuencia de medios cuando finaliza la secuencia.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Cuando [](media-session.md) la sesión multimedia recibe el evento MEEndOfStream, llama a [**MFStreamSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) en el receptor multimedia correspondiente, con el tipo de marcador **MFSTREAMSINK \_ MARKER \_ ENDOFSEGMENT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




