---
description: Se produjo un error no irrecuperable durante el streaming.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360523"
---
# <a name="menonfatalerror-event"></a>Evento MENonFatalError

Se produjo un error no irrecuperable durante el streaming. Cualquier componente de Media Foundation puede enviar este evento en cualquier momento.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE            | Descripción                                                        |
|--------------------|--------------------------------------------------------------------|
| VT \_ UI4<br/> | Valor **HRESULT** que describe el error.<br/> <br/> |



## <a name="attributes"></a>Atributos

No hay atributos definidos para este evento.

## <a name="remarks"></a>Observaciones

Este evento indica un error inesperado pero recuperable durante el streaming. Por ejemplo, un origen multimedia podría enviar este evento si quita un paquete.

No envíe este evento para indicar que se produjo un error en un método asincrónico. Si se produce un error en un método asincrónico, se devuelve el código de error en el evento normal para ese método.

Si se produce un error de streaming no recuperable, envíe el evento [MEError](meerror.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




