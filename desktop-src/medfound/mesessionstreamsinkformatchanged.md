---
description: Lo genera la sesión multimedia cuando cambia el formato en un receptor multimedia.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08d086d5966e0fc1f6ce4b4b3d639b40d795a4e05799f3928f61afa9abddf4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268595"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>Evento MESessionStreamSinkFormatChanged

Lo genera la sesión multimedia cuando cambia el formato en un receptor multimedia.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                    | Descripción                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**NODO DE \_ SALIDA \_ DE EVENTOS MF \_**](mf-event-output-node-attribute.md)<br/> | Identifica el nodo de topología para el receptor de medios cuyo formato ha cambiado.<br/> <br/> |



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

 

 




