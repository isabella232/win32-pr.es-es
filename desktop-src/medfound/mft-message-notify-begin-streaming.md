---
description: Notifica a una transformación de Media Foundation (MFT) que la transmisión por secuencias está a punto de comenzar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275841"
---
# <a name="mft_message_notify_begin_streaming"></a>la \_ notificación del mensaje de MFT \_ comienza el \_ \_ streaming

Notifica a una transformación de Media Foundation (MFT) que la transmisión por secuencias está a punto de comenzar.

## <a name="message-parameter"></a>Parámetro de mensaje

Ninguno.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

No es necesario que el cliente envíe este mensaje. Si el cliente envía este mensaje, debe hacerlo después de establecer todos los tipos de medios en la MFT y antes de llamar a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). La MFT puede responder mediante la asignación de búferes u otros recursos. Si el cliente no envía este mensaje, la MFT asigna recursos en la primera llamada a **ProcessInput**. Por lo tanto, el envío de este mensaje puede reducir la latencia inicial cuando se inicia la transmisión por secuencias.

### <a name="implementation"></a>Implementación

No se requiere una MFT para responder a este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de mensaje de MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




