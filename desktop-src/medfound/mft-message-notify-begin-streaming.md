---
description: Notifica a una Media Foundation transformación de datos (MFT) que el streaming está a punto de comenzar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491f84ee2dee752cccc251187c43bd497723a64ae6601954051f2aebab34ef85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848074"
---
# <a name="mft_message_notify_begin_streaming"></a>NOTIFICACIÓN DE MENSAJE DE MFT \_ \_ BEGIN \_ \_ STREAMING

Notifica a una Media Foundation transformación de datos (MFT) que el streaming está a punto de comenzar.

## <a name="message-parameter"></a>Parámetro message

Ninguno.

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

No es necesario que el cliente envíe este mensaje. Si el cliente envía este mensaje, debe hacerlo después de establecer todos los tipos de medios en el MFT y antes de llamar a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). El MFT puede responder asignando búferes u otros recursos. Si el cliente no envía este mensaje, MFT asigna recursos en la primera llamada a **ProcessInput.** Por lo tanto, el envío de este mensaje puede reducir la latencia inicial cuando comienza el streaming.

### <a name="implementation"></a>Implementación

No se requiere un MFT para responder a este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO DE MENSAJE \_ \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




