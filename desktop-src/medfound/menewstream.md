---
description: Lo genera un origen multimedia cuando inicia una nueva secuencia.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696768"
---
# <a name="menewstream-event"></a>Evento MENewStream

Lo genera un origen multimedia cuando inicia una nueva secuencia.

Cuando se llama al método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen multimedia envía un evento para cada flujo seleccionado:

-   El origen envía el evento MENewStream si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), o esta es la primera llamada a **Start** en este origen multimedia.

-   El origen envía el evento [MEUpdatedStream](meupdatedstream.md) si la secuencia ya se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

No se envía ningún evento para flujos no seleccionados.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE                | Descripción                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ desconocido<br/> | Contiene un puntero a la interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) de la secuencia.<br/> <br/> |



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

 

 




