---
description: Indica un error grave. Cualquier Media Foundation componente puede enviar este evento en cualquier momento. Llame a IMFMediaEvent::GetStatus para obtener el código de error de la operación que produjo un error.
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941475"
---
# <a name="meerror-event"></a>Evento MEError

Indica un error grave. Cualquier Media Foundation componente puede enviar este evento en cualquier momento. Llame [**a IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obtener el código de error de la operación que produjo un error.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este evento solo se debe usar para errores inesperados. No envíe este evento para indicar que se ha produce un error en un método asincrónico. Si se produce un error en un método asincrónico, el código de error se devuelve en el evento normal para ese método.

Si se produce un error recuperable durante el streaming, envíe el [evento MENonFatalError.](menonfatalerror.md)

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

 

 




