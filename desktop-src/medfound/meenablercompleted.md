---
description: Lo genera un objeto habilitador de contenido cuando se completa la acción de habilitación de objetos.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2983cbcf3927626da88432c0cc04f28e2fc5d3e866d161b514dcbe5108bcf92a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013805"
---
# <a name="meenablercompleted-event"></a>Evento MEEnablerCompleted

Lo genera un objeto habilitador de contenido cuando se completa la acción de habilitación del objeto. Los objetos que exponen [**la interfaz IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pueden generar este evento. El evento se genera si se produce alguna de las siguientes situaciones:

-   El [**método IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se completa de forma asincrónica.
-   La aplicación llama [**a IMFContentEnabler::MonitorEnable y,**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)a continuación, la aplicación completa la solicitud HTTP POST, como se describe en **el método MonitorEnable.**

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

El código de estado del evento puede contener uno de los siguientes valores.



| Valor                                     | Descripción                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ OK**                            | La operación se realizó correctamente.                                                                                                                                                        |
| **NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED** | No se adquirió la licencia DRM. Si el intento anterior [**usó AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), la aplicación debe intentar la adquisición no silenciosa. |
| **MONITOR DRM DE NS \_ \_ \_ \_ CANCELADO**   | Se canceló la operación [**MonitorEnable.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)                                                                                            |



 

Para recibir este evento, consulte la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para la [**interfaz IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) A [**continuación, llame a IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), como se describe en el tema [Generadores de eventos multimedia](media-event-generators.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Generadores de eventos multimedia](media-event-generators.md)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




