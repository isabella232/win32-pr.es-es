---
description: Lo genera un origen multimedia cuando finaliza una presentación. Este evento indica que todas las secuencias de la presentación están completas. La sesión multimedia reenvía este evento a la aplicación.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941465"
---
# <a name="meendofpresentation-event"></a>Evento MEEndOfPresentation

Lo genera un origen multimedia cuando finaliza una presentación. Este evento indica que todas las secuencias de la presentación están completas. La sesión multimedia reenvía este evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                               | Descripción                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**TOPOLOGÍA \_ DE ORIGEN DE EVENTOS MF \_ \_ \_ CANCELADA**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica si el origen del secuenciador canceló esta presentación.<br/> <br/> |



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

 

 




