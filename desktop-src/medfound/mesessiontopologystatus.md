---
description: Lo genera la sesión multimedia cuando cambia el estado de una topología.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42adfd1a86319f65077e87925eb23807253f12b06e977ee1eb9e494a4c7df180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723725"
---
# <a name="mesessiontopologystatus-event"></a>Evento MESessionTopologyStatus

Lo genera la sesión multimedia cuando cambia el estado de una topología.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE                | Descripción                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntero a [**la interfaz DETOPOLOGY**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                            | Descripción                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**ESTADO \_ DE LA TOPOLOGÍA DE EVENTOS \_ \_ MF**](mf-event-topology-status-attribute.md)<br/> | Especifica el nuevo estado de la topología.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Para obtener un ejemplo de código que recupera el puntero [**DETOPOLOGY**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) del evento, vea [EVENTO MESessionTopologySet.](mesessiontopologyset.md)

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

 

 




