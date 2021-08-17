---
description: Lo genera una salida de confianza si se produce un error al aplicar la directiva de salida.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1f0d05b73ea295ea3282af5950d4a9a61f833f61463cd095848563e3858c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877552"
---
# <a name="mepolicyerror-event"></a>Evento MEPolicyError

Lo genera una salida de confianza si se produce un error al aplicar la directiva de salida.

Si la sesión multimedia recibe este evento, detiene la reproducción y reenvía el evento a la aplicación.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Los valores posibles recuperados [**de IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) incluyen lo siguiente.



| Value                      | Descripción                                                    |
|----------------------------|----------------------------------------------------------------|
| DIRECTIVA \_ MF E NO \_ \_ ADMITIDA | La salida de confianza no admite la directiva de salida actual. |



 

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

 

 




