---
description: Generado por una secuencia de medios cuando finaliza la secuencia.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Evento MEEndOfStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908475"
---
# <a name="meendofstream-event"></a>Evento MEEndOfStream

Generado por una secuencia de medios cuando finaliza la secuencia.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Cuando la [sesión multimedia](media-session.md) recibe el evento MEEndOfStream, llama a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) en el receptor multimedia correspondiente, con el tipo de marcador **\_ \_ ENDOFSEGMENT de marcador de MFSTREAMSINK** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




