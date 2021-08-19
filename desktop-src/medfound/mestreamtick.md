---
description: Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b72a61964e296ac5f7aa69eb2be6773b622f7b44df8300affa0150af2f8a77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974064"
---
# <a name="mestreamtick-event"></a>Evento MEStreamTick

Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE           | Descripción                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | Hora a la que se produce la brecha, en unidades de 100 nanosegundos.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este evento indica una brecha en los datos. El evento notifica a los componentes de nivel inferior que no esperen ningún dato en el momento especificado.

El evento debe enviarse por cualquier objeto que genere las marcas de tiempo para los ejemplos multimedia de la secuencia. Dependiendo del formato de los datos, esto es:

-   La secuencia multimedia en el origen de medios [**(interfaz DEOMEDIASTREAM)**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) o
-   Transformación del descodificador [**(interfaz DETRANSFORMTRANSFORM).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Durante la separación, el objeto debe enviar el evento con tanta frecuencia como normalmente produciría muestras. En el caso del vídeo, envíe un evento para cada fotograma que falta. Para el audio, envíe el evento al menos una vez por segundo durante la separación. El valor del evento es la marca de tiempo de la muestra que falta. Envíe tantos eventos MEStreamTick como sea necesario para rellenar el espacio en los datos.

Si un origen multimedia tiene varias secuencias y hay una brecha en más de una secuencia, cada secuencia debe enviar eventos MEStreamTick. Por ejemplo, si hay una brecha en los datos de audio y vídeo, ambas secuencias envían el evento.

El evento MEStreamTick no completa una [**solicitud IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) El origen de medios todavía debe enviar un [evento MEMediaSample](memediasample.md) para cada llamada a **RequestSample**.

Los receptores multimedia no pueden consumir este evento directamente. Para señalar una brecha en la secuencia a un receptor multimedia, llame a [**MFStreamSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcador **TICK DE MFSTREAMSINK \_ MARKER. \_** La Media Foundation convierte los eventos MEStreamTick en marcadores **TICK de MFSTREAMSINK \_ MARKER \_** cuando es necesario.

No establezca el atributo [**MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) en el siguiente ejemplo multimedia después de un evento MEStreamTick. El **atributo MFSampleExtension \_ Discontinuity** implica que la marca de tiempo es discontinua con las marcas de tiempo anteriores, mientras que MEStreamTick implica que las marcas de tiempo son continuas, pero faltan algunos datos.

> [!Note]  
> Una versión anterior de la documentación indicaba incorrectamente que el ejemplo después de un evento MEStreamTick debe tener el atributo [**MFSampleExtension \_ Discontinuity.**](mfsampleextension-discontinuity-attribute.md)

 

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

 

 




