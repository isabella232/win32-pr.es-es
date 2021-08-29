---
description: Se genera cuando un receptor multimedia deja de ser válido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b002ffc47f8a47d9c7b2228a9a4d7ad7441b70aa08d12f74ece7590fe5a7088e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941445"
---
# <a name="mesinkinvalidated-event"></a>Evento MESinkInvalidated

Se genera cuando un receptor multimedia deja de ser válido.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                    | Descripción                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**NODO DE \_ SALIDA \_ DE EVENTOS MF \_**](mf-event-output-node-attribute.md)<br/> | Identifica el nodo de topología para este receptor multimedia.<br/> <br/> |



## <a name="remarks"></a>Comentarios

La sesión multimedia genera este evento si recibe cualquiera de los siguientes eventos del receptor de medios:

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

Un receptor multimedia también puede generar este evento, en cuyo caso la sesión multimedia establece el atributo [**MF \_ EVENT OUTPUT \_ \_ NODE**](mf-event-output-node-attribute.md) en el evento y reenvía el evento a la aplicación.

Si la aplicación recibe este evento, debe volver a crear el receptor multimedia y poner en cola la topología de nuevo.

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

 

 




