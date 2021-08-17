---
description: Lo genera la sesión multimedia cuando el método IMFMediaSession::ClearTopologies se completa de forma asincrónica.
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Evento MESessionTopologiesCleared (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6b9107f6584de3f9621aeaecc95ffb6bf7bbb8741e59d5e32d3efe33d5ae6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357125"
---
# <a name="mesessiontopologiescleared-event"></a>Evento MESessionTopologiesCleared

Lo genera la sesión multimedia cuando el [**método IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se completa de forma asincrónica.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



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
</dt> </dl>

 

 




