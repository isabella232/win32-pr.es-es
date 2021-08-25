---
description: Lo genera una secuencia de medios cuando cambia el tipo de medio de la secuencia.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762f65beb26f5095c9e89be845f468e3ca53c9b5cd227916bb7cc38417626c60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957275"
---
# <a name="mestreamformatchanged-event"></a>Evento MEStreamFormatChanged

Lo genera una secuencia de medios cuando cambia el tipo de medio de la secuencia.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE                | Descripción                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) del nuevo tipo de medio.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Use este evento para indicar cambios de formato en la secuencia.

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

 

 




