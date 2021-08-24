---
description: Lo genera un origen multimedia cuando inicia una nueva secuencia.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499b7899c499e87a45e9b7f043db94724b41d729d3b836e7c9f8d71d83616841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228775"
---
# <a name="menewstream-event"></a>Evento MENewStream

Lo genera un origen multimedia cuando inicia una nueva secuencia.

Cuando se [**llama al método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen de medios envía un evento para cada secuencia seleccionada:

-   El origen envía el evento MENewStream si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)o esta es la primera llamada a **Start** en este origen multimedia.

-   El origen envía el [evento MEUpdatedStream](meupdatedstream.md) si la secuencia ya estaba seleccionada en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).

No se envían eventos para secuencias no elegidas.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Contiene un puntero a la interfaz [**DESTREAMMEDIASTREAM de la**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) secuencia.<br/> <br/> |



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

 

 




