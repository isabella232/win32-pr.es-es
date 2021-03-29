---
description: La inicia la sesión de medios cuando cambia el estado de una topología.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001515"
---
# <a name="mesessiontopologystatus-event"></a>Evento MESessionTopologyStatus

La inicia la sesión de medios cuando cambia el estado de una topología.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ desconocido<br/> | Puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                            | Descripción                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**Estado de la \_ topología de eventos MF \_ \_**](mf-event-topology-status-attribute.md)<br/> | Especifica el nuevo estado de la topología.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Para obtener un ejemplo de código que recupera el puntero [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) del evento, vea el evento [MESessionTopologySet](mesessiontopologyset.md) .

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

 

 




