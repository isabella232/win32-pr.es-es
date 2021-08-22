---
description: Lo genera la sesión multimedia cuando cambian las funcionalidades de la sesión.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464875"
---
# <a name="mesessioncapabilitieschanged-event"></a>Evento MESessionCapabilitiesChanged

Lo genera la sesión multimedia cuando cambian las funcionalidades de la sesión.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

El evento contiene los atributos siguientes.



| Atributo                                                                     | Descripción                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ EVENT \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)              | Nuevas marcas de funcionalidades de sesión.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md) | Indica qué marcas de funcionalidad han cambiado. |



 

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

 

 




