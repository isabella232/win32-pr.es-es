---
description: Lo genera un origen multimedia cuando cambian las características de los orígenes.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd69be00727ec3f1f635b82fb6c8e29c4016959ced480be4e9de6b8a83cfe8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877373"
---
# <a name="mesourcecharacteristicschanged-event"></a>Evento MESourceCharacteristicsChanged

Lo genera un origen multimedia cuando cambian las características del origen.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                                   | Descripción                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CARACTERÍSTICAS DE \_ ORIGEN \_ DE EVENTOS MF \_**](mf-event-source-characteristics-attribute.md)<br/>          | Nuevas características del origen multimedia.<br/> <br/>      |
| [**CARACTERÍSTICAS ANTIGUAS \_ DEL ORIGEN DE EVENTOS \_ \_ \_ MF**](mf-event-source-characteristics-old-attribute.md)<br/> | Características anteriores del origen de medios.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




