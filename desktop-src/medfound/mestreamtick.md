---
description: Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715307"
---
# <a name="mestreamtick-event"></a>Evento MEStreamTick

Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ i8<br/> | Hora a la que se produce la brecha, en unidades de 100-nanosegundos.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento señala una brecha en los datos. El evento notifica a los componentes de nivel inferior que no esperan ningún dato en el momento especificado.

El evento debe ser enviado por cualquier objeto que genere las marcas de tiempo para los ejemplos de medios de la secuencia. Dependiendo del formato de los datos, se puede:

-   El flujo de medios en el origen de medios (interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) o
-   La transformación del descodificador (interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).

Durante el intervalo, el objeto debe enviar el evento con la frecuencia con la que generaría normalmente ejemplos. Para vídeo, envíe un evento por cada fotograma que falta. En el caso de audio, envíe el evento al menos una vez por segundo durante el intervalo. El valor del evento es la marca de tiempo del ejemplo que falta. Envíe tantos eventos MEStreamTick como sea necesario para completar la brecha en los datos.

Si un origen multimedia tiene varios flujos y hay un hueco en más de un flujo, cada flujo debe enviar eventos MEStreamTick. Por ejemplo, si hay una brecha en los datos de audio y vídeo, ambos flujos envían el evento.

El evento MEStreamTick no completa una solicitud [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) . El origen multimedia todavía debe enviar un evento [MEMediaSample](memediasample.md) para cada llamada a **RequestSample**.

Los receptores de medios no pueden consumir este evento directamente. Para indicar una brecha en el flujo en un receptor de multimedia, llame a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcador de **\_ \_ paso de marcador MFSTREAMSINK** . La canalización Media Foundation convierte los eventos MEStreamTick en marcadores de **\_ \_ graduación del marcador MFSTREAMSINK** cuando sea necesario.

No establezca el atributo [**\_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en el siguiente ejemplo de medio después de un evento MEStreamTick. El **atributo \_ discontinuidad de MFSampleExtension** implica que la marca de tiempo es descontinuada con las marcas de tiempo anteriores, mientras que MEStreamTick implica que las marcas de tiempo son continuas pero faltan algunos datos.

> [!Note]  
> Una versión anterior de la documentación indicó incorrectamente que el ejemplo después de un evento MEStreamTick debe tener el [**atributo \_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .

 

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

 

 




