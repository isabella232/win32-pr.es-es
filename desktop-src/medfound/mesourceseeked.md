---
description: 'Se genera cuando un origen multimedia busca una nueva posición. Un origen multimedia genera este evento si el origen se está ejecutando o está en pausa y la aplicación llama a IMFMediaSource:: Start con una hora de inicio que no es igual a la posición actual.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715316"
---
# <a name="mesourceseeked-event"></a>Evento MESourceSeeked

Se genera cuando un origen multimedia busca una nueva posición. Un origen multimedia genera este evento si el origen se está ejecutando o está en pausa y la aplicación llama a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con una hora de inicio que no es igual a la posición actual.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ i8<br/> | La nueva posición inicial, en unidades de 100-nanosegundos.<br/> <br/> |



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

 

 




