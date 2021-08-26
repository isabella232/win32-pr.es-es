---
description: Señala el progreso de un objeto habilitador de contenido. Los objetos que exponen la interfaz IMFContentEnabler pueden generar este evento para notificar a la aplicación el progreso de las acciones de habilitadores de contenido.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9772a076e1d9de0cff2336b4c6d6b9b068f11e4fc572b44f0f914a8353f651bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013765"
---
# <a name="meenablerprogress-event"></a>Evento MEEnablerProgress

Señala el progreso de un objeto habilitador de contenido. Los objetos que exponen [**la interfaz IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pueden generar este evento para notificar a la aplicación el progreso de las acciones del habilitador de contenido.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE               | Descripción                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Cadena de caracteres anchos que describe el progreso.<br/> <br/> |



## <a name="remarks"></a>Comentarios

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

 

 




