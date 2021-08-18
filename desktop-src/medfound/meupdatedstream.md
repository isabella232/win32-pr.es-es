---
description: Lo genera un origen multimedia cuando reinicia o busca una secuencia que ya está activa.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5746b619f885ab7648110cbe58b66b7897c839031202d811becd33e1c84991a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974024"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Lo genera un origen multimedia cuando reinicia o busca una secuencia que ya está activa.

Cuando se [**llama al método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen de medios envía un evento para cada secuencia seleccionada:

-   El origen envía el [evento MENewStream](menewstream.md) si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)o esta es la primera llamada a **Start** en este origen multimedia.

-   El origen envía el evento MEUpdatedStream si la secuencia ya estaba seleccionada en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

No se envía ningún evento para secuencias no elegidas.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntero a la interfaz [**DESTREAMMEDIASTREAM de la**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) secuencia.<br/> <br/> |



## <a name="remarks"></a>Comentarios

En la primera llamada a [**Start en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) la que una secuencia se activa, el origen del medio envía un [evento MENewStream](menewstream.md) para la secuencia. En las llamadas posteriores **a Start**, el origen del medio envía un evento MEUpdatedStream, hasta que se deselecciona la secuencia.

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

 

 




