---
description: Lo genera un receptor de flujo cuando el flujo ha recibido suficientes datos previos al lanzamiento para comenzar la representación. Este evento se genera mediante receptores multimedia que admiten la interfaz IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d46c4c4e076651cb38318bb908df280c503c0880a256087f4192433ecdb5406a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464805"
---
# <a name="mestreamsinkprerolled-event"></a>Evento MEStreamSinkPrerolled

Lo genera un receptor de flujo cuando el flujo ha recibido suficientes datos previos al lanzamiento para comenzar la representación. Este evento se genera mediante receptores multimedia que admiten la [**interfaz IMFMediaSinkPreroll.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



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

 

 




