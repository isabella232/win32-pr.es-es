---
description: 'Se genera cuando el método IMFMediaSession:: Close se completa de forma asincrónica.'
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: Evento MESessionClosed (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705993"
---
# <a name="mesessionclosed-event"></a>Evento MESessionClosed

Se genera cuando el método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) se completa de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



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

 

 




