---
description: Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546163"
---
# <a name="meupdatedstream-event"></a>Evento MEUpdatedStream

Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.

Cuando se llama al método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen multimedia envía un evento para cada flujo seleccionado:

-   El origen envía el evento [MENewStream](menewstream.md) si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), o esta es la primera llamada a **Start** en este origen multimedia.

-   El origen envía el evento MEUpdatedStream si la secuencia ya se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

No se envía ningún evento para flujos no seleccionados.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ desconocido<br/> | Puntero a la interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) de la secuencia.<br/> <br/> |



## <a name="remarks"></a>Observaciones

En la primera llamada a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en la que se activa una secuencia, el origen multimedia envía un evento [MENewStream](menewstream.md) para la secuencia. En las llamadas posteriores a **Start**, el origen multimedia envía un evento MEUpdatedStream, hasta que se anule la selección de la secuencia.

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

 

 




