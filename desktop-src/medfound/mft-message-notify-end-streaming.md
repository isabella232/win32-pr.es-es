---
description: Solicita que una transformación de Media Foundation (MFT) a ese streaming esté a punto de finalizar.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543910"
---
# <a name="mft_message_notify_end_streaming"></a>\_fin de \_ notificación de mensaje \_ de MFT \_

Solicita que una transformación de Media Foundation (MFT) a ese streaming esté a punto de finalizar.

## <a name="message-parameter"></a>Parámetro de mensaje

Ninguno.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

No es necesario que el cliente envíe este mensaje, incluso si el cliente envió anteriormente el **mensaje de MFT \_ \_ Notify \_ Begin \_ streaming** .

### <a name="implementation"></a>Implementación

La MFT puede responder a este mensaje liberando búferes y otros recursos. MFT no vacía los datos de entrada ni restablece los tipos de medios en respuesta a este mensaje. No se requiere una MFT para responder a este mensaje.

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

 

 




